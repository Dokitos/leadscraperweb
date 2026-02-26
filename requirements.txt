"""
Teste isolado do scraper — corre directamente sem FastAPI.
Uso: py -3.11 teste_backend.py
"""
import sys
import asyncio

if sys.platform == "win32":
    asyncio.set_event_loop_policy(asyncio.WindowsProactorEventLoopPolicy())
    loop = asyncio.ProactorEventLoop()
    asyncio.set_event_loop(loop)

async def main():
    from playwright.async_api import async_playwright

    print("A iniciar browser...")
    async with async_playwright() as p:
        browser = await p.chromium.launch(
            headless=False,
            args=["--start-maximized", "--disable-blink-features=AutomationControlled"]
        )
        context = await browser.new_context(
            locale="pt-PT",
            viewport={"width": 1280, "height": 800},
            user_agent="Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/121.0.0.0 Safari/537.36"
        )
        page = await context.new_page()
        print("Browser aberto!")

        # Passo 1 — Google PT
        print("\n[1] A visitar google.pt...")
        await page.goto("https://www.google.pt", wait_until="domcontentloaded")
        await page.wait_for_timeout(2000)
        print(f"    Título: {await page.title()}")

        # Passo 2 — Google Maps
        pesquisa = "remodelacao Lisboa"
        url = f"https://www.google.com/maps/search/{pesquisa.replace(' ', '+')}?hl=pt-PT"
        print(f"\n[2] A pesquisar: {pesquisa}")
        print(f"    URL: {url}")
        await page.goto(url, wait_until="domcontentloaded", timeout=30000)
        await page.wait_for_timeout(4000)
        titulo = await page.title()
        print(f"    Título da página: {titulo}")

        # Passo 3 — Verificar o que está na página
        print("\n[3] A verificar conteúdo da página...")
        feed_existe = await page.evaluate("() => !!document.querySelector('[role=\"feed\"]')")
        print(f"    [role='feed'] existe: {feed_existe}")

        resultados_existe = await page.evaluate("() => !!document.querySelector('div[aria-label]')")
        print(f"    div[aria-label] existe: {resultados_existe}")

        links_count = await page.evaluate("""
            () => document.querySelectorAll('a[href*="/maps/place/"]').length
        """)
        print(f"    Links /maps/place/ encontrados: {links_count}")

        # Screenshot para ver o que está a aparecer
        await page.screenshot(path="debug_maps.png")
        print("\n    Screenshot guardado: debug_maps.png")

        # Passo 4 — Tentar rolar se feed existir
        if feed_existe:
            print("\n[4] A rolar feed...")
            for i in range(4):
                await page.evaluate('document.querySelector(\'[role="feed"]\').scrollTop += 2000')
                await page.wait_for_timeout(1000)
                links = await page.evaluate("() => document.querySelectorAll('a[href*=\"/maps/place/\"]').length")
                print(f"    Após rolagem {i+1}: {links} links")
        else:
            print("\n[4] Feed não encontrado — a tentar tecla End...")
            for i in range(4):
                await page.keyboard.press("End")
                await page.wait_for_timeout(800)
                links = await page.evaluate("() => document.querySelectorAll('a[href*=\"/maps/place/\"]').length")
                print(f"    Após End {i+1}: {links} links")

        # Passo 5 — Recolher links finais
        links = await page.evaluate("""
            () => {
                const s = new Set();
                document.querySelectorAll('a[href*="/maps/place/"]').forEach(el => {
                    const h = el.href || el.getAttribute('href') || '';
                    if (h.includes('/maps/place/'))
                        s.add(h.startsWith('http') ? h : 'https://www.google.com' + h);
                });
                return Array.from(s);
            }
        """)
        print(f"\n[5] Total de links únicos recolhidos: {len(links)}")
        for l in links[:3]:
            print(f"    → {l[:80]}")

        if links:
            # Passo 6 — Testar extracção de 1 empresa
            print(f"\n[6] A extrair dados da 1ª empresa...")
            await page.goto(links[0], wait_until="domcontentloaded", timeout=20000)
            await page.wait_for_timeout(2500)

            nome = await page.evaluate("() => { const h = document.querySelector('h1'); return h ? h.innerText.trim() : 'NÃO ENCONTRADO'; }")
            tel  = await page.evaluate("""
                () => {
                    for (const b of document.querySelectorAll('button[data-item-id^="phone"]')) {
                        const m = (b.getAttribute('data-item-id')||'').match(/phone:tel:(.+)/);
                        if (m) return m[1];
                    }
                    return 'NÃO ENCONTRADO';
                }
            """)
            print(f"    Nome:     {nome}")
            print(f"    Telefone: {tel}")

        print("\n✅ Teste concluído! Verifica o ficheiro debug_maps.png para ver o que o browser encontrou.")
        input("\nPressiona ENTER para fechar o browser...")
        await browser.close()

asyncio.run(main())
