<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LeadScraper — Painel de Controlo</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg:       #0a0c10;
    --surface:  #111318;
    --border:   #1e2230;
    --accent:   #00e5ff;
    --accent2:  #ff4d6d;
    --accent3:  #69ff8a;
    --text:     #e8eaf0;
    --muted:    #4a5068;
    --quente:   #ff4d6d;
    --medio:    #ffb347;
    --frio:     #69ff8a;
    --radius:   8px;
    --mono:     'Space Mono', monospace;
    --sans:     'Syne', sans-serif;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

  /* ── HEADER ── */
  header {
    border-bottom: 1px solid var(--border);
    padding: 1rem 2rem;
    display: flex;
    align-items: center;
    gap: 1rem;
    background: var(--surface);
    position: sticky;
    top: 0;
    z-index: 100;
  }
  .logo {
    font-family: var(--mono);
    font-size: 1.1rem;
    color: var(--accent);
    letter-spacing: -0.02em;
  }
  .logo span { color: var(--text); }
  .status-dot {
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--muted);
    transition: background 0.3s;
    flex-shrink: 0;
  }
  .status-dot.ativo  { background: var(--accent3); box-shadow: 0 0 8px var(--accent3); animation: pulse 2s infinite; }
  .status-dot.pausado { background: var(--medio); }
  .status-dot.erro   { background: var(--quente); }
  @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:0.4} }
  .status-txt { font-family: var(--mono); font-size: 0.7rem; color: var(--muted); }
  header nav { margin-left: auto; display: flex; gap: 0.5rem; }
  .tab-btn {
    background: none; border: 1px solid var(--border);
    color: var(--muted); padding: 0.4rem 1rem;
    border-radius: var(--radius); cursor: pointer;
    font-family: var(--mono); font-size: 0.7rem;
    transition: all 0.2s;
  }
  .tab-btn:hover, .tab-btn.active {
    border-color: var(--accent); color: var(--accent);
    background: rgba(0,229,255,0.05);
  }

  /* ── LAYOUT ── */
  .layout { display: grid; grid-template-columns: 340px 1fr; flex: 1; }

  /* ── SIDEBAR ── */
  .sidebar {
    border-right: 1px solid var(--border);
    padding: 1.5rem;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    overflow-y: auto;
    height: calc(100vh - 57px);
    position: sticky;
    top: 57px;
  }

  .section-title {
    font-family: var(--mono);
    font-size: 0.65rem;
    color: var(--muted);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 0.75rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  label { font-size: 0.78rem; color: var(--muted); display: block; margin-bottom: 0.3rem; }

  select, input[type="number"] {
    width: 100%;
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    color: var(--text);
    padding: 0.5rem 0.75rem;
    font-family: var(--mono);
    font-size: 0.8rem;
    appearance: none;
    outline: none;
    transition: border-color 0.2s;
  }
  select:focus, input:focus { border-color: var(--accent); }

  .chips {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
  }
  .chip {
    padding: 0.3rem 0.7rem;
    border: 1px solid var(--border);
    border-radius: 999px;
    font-family: var(--mono);
    font-size: 0.68rem;
    cursor: pointer;
    color: var(--muted);
    transition: all 0.15s;
    user-select: none;
  }
  .chip.selected {
    border-color: var(--accent);
    color: var(--accent);
    background: rgba(0,229,255,0.08);
  }

  .toggle-row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0.5rem 0;
    border-bottom: 1px solid var(--border);
  }
  .toggle-row:last-child { border-bottom: none; }
  .toggle-label { font-size: 0.78rem; }
  .toggle {
    position: relative;
    width: 36px; height: 20px;
  }
  .toggle input { opacity: 0; width: 0; height: 0; }
  .slider {
    position: absolute; inset: 0;
    background: var(--border);
    border-radius: 999px;
    cursor: pointer;
    transition: background 0.2s;
  }
  .slider::before {
    content: '';
    position: absolute;
    width: 14px; height: 14px;
    background: white;
    border-radius: 50%;
    top: 3px; left: 3px;
    transition: transform 0.2s;
  }
  .toggle input:checked + .slider { background: var(--accent); }
  .toggle input:checked + .slider::before { transform: translateX(16px); }

  .btn-iniciar {
    width: 100%;
    padding: 0.85rem;
    background: var(--accent);
    color: var(--bg);
    border: none;
    border-radius: var(--radius);
    font-family: var(--mono);
    font-size: 0.85rem;
    font-weight: 700;
    cursor: pointer;
    letter-spacing: 0.05em;
    transition: opacity 0.2s, transform 0.1s;
  }
  .btn-iniciar:hover { opacity: 0.85; }
  .btn-iniciar:active { transform: scale(0.98); }
  .btn-iniciar:disabled { opacity: 0.4; cursor: not-allowed; }

  /* ── CONTROLO SESSÃO ── */
  .controlo {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.5rem;
  }
  .btn-ctrl {
    padding: 0.5rem;
    border: 1px solid var(--border);
    background: var(--surface);
    color: var(--text);
    border-radius: var(--radius);
    font-family: var(--mono);
    font-size: 0.7rem;
    cursor: pointer;
    transition: all 0.15s;
  }
  .btn-ctrl:hover { border-color: var(--accent); color: var(--accent); }
  .btn-ctrl.danger:hover { border-color: var(--quente); color: var(--quente); }
  .btn-ctrl.success:hover { border-color: var(--accent3); color: var(--accent3); }

  /* ── STATS ── */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.5rem;
  }
  .stat-card {
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 0.75rem;
    text-align: center;
  }
  .stat-num {
    font-family: var(--mono);
    font-size: 1.4rem;
    font-weight: 700;
    line-height: 1;
  }
  .stat-num.quente { color: var(--quente); }
  .stat-num.medio  { color: var(--medio); }
  .stat-num.frio   { color: var(--frio); }
  .stat-num.total  { color: var(--accent); }
  .stat-label { font-size: 0.65rem; color: var(--muted); margin-top: 0.25rem; }

  /* ── MAIN CONTENT ── */
  .main { display: flex; flex-direction: column; overflow: hidden; }

  /* ── TOOLBAR ── */
  .toolbar {
    padding: 0.75rem 1.5rem;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    gap: 1rem;
    background: var(--surface);
  }
  .toolbar-title { font-family: var(--mono); font-size: 0.75rem; color: var(--muted); }
  .filtro-qualidade {
    display: flex;
    gap: 0.4rem;
    margin-left: auto;
  }
  .fq-btn {
    padding: 0.3rem 0.75rem;
    border: 1px solid var(--border);
    border-radius: 999px;
    background: none;
    font-family: var(--mono);
    font-size: 0.65rem;
    cursor: pointer;
    transition: all 0.15s;
    color: var(--muted);
  }
  .fq-btn.q { border-color: var(--quente); color: var(--quente); }
  .fq-btn.m { border-color: var(--medio);  color: var(--medio);  }
  .fq-btn.f { border-color: var(--frio);   color: var(--frio);   }
  .fq-btn.active { background: rgba(255,255,255,0.05); }
  .btn-export {
    padding: 0.3rem 0.75rem;
    border: 1px solid var(--accent);
    border-radius: var(--radius);
    background: rgba(0,229,255,0.05);
    color: var(--accent);
    font-family: var(--mono);
    font-size: 0.65rem;
    cursor: pointer;
    transition: all 0.15s;
  }
  .btn-export:hover { background: rgba(0,229,255,0.15); }

  /* ── LOG / LEADS TABS ── */
  .content-tabs {
    display: flex;
    border-bottom: 1px solid var(--border);
    padding: 0 1.5rem;
    gap: 1rem;
  }
  .ctab {
    padding: 0.6rem 0;
    font-family: var(--mono);
    font-size: 0.72rem;
    color: var(--muted);
    cursor: pointer;
    border-bottom: 2px solid transparent;
    margin-bottom: -1px;
    transition: all 0.15s;
  }
  .ctab.active { color: var(--accent); border-bottom-color: var(--accent); }

  /* ── LEADS TABLE ── */
  .leads-container {
    flex: 1;
    overflow-y: auto;
    padding: 1rem 1.5rem;
  }
  .leads-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.78rem;
  }
  .leads-table th {
    text-align: left;
    padding: 0.5rem 0.75rem;
    font-family: var(--mono);
    font-size: 0.62rem;
    color: var(--muted);
    letter-spacing: 0.05em;
    text-transform: uppercase;
    border-bottom: 1px solid var(--border);
    position: sticky;
    top: 0;
    background: var(--bg);
  }
  .leads-table td {
    padding: 0.55rem 0.75rem;
    border-bottom: 1px solid rgba(30,34,48,0.5);
    vertical-align: middle;
    max-width: 200px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .leads-table tr:hover td { background: rgba(255,255,255,0.02); }

  .badge {
    display: inline-block;
    padding: 0.15rem 0.5rem;
    border-radius: 999px;
    font-family: var(--mono);
    font-size: 0.62rem;
    font-weight: 700;
  }
  .badge.QUENTE { background: rgba(255,77,109,0.15); color: var(--quente); border: 1px solid rgba(255,77,109,0.3); }
  .badge.MEDIO  { background: rgba(255,179,71,0.15);  color: var(--medio);  border: 1px solid rgba(255,179,71,0.3); }
  .badge.FRIO   { background: rgba(105,255,138,0.15); color: var(--frio);   border: 1px solid rgba(105,255,138,0.3); }

  .tel-link { color: var(--accent); text-decoration: none; font-family: var(--mono); font-size: 0.75rem; }
  .tel-link:hover { text-decoration: underline; }
  .web-link { color: var(--muted); text-decoration: none; font-size: 0.72rem; }
  .web-link:hover { color: var(--text); }
  .sem-web { color: var(--quente); font-family: var(--mono); font-size: 0.65rem; }

  .lead-row { animation: fadeSlide 0.3s ease both; }
  @keyframes fadeSlide {
    from { opacity: 0; transform: translateY(-6px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ── LOG ── */
  .log-container {
    flex: 1;
    overflow-y: auto;
    padding: 1rem 1.5rem;
    font-family: var(--mono);
    font-size: 0.72rem;
    display: none;
  }
  .log-line { padding: 0.2rem 0; border-bottom: 1px solid rgba(30,34,48,0.3); color: var(--muted); }
  .log-line.ok    { color: var(--accent3); }
  .log-line.erro  { color: var(--quente); }
  .log-line.info  { color: var(--accent); }
  .log-line.aviso { color: var(--medio); }
  .log-line .ts   { color: var(--border); margin-right: 0.5rem; }

  /* ── HISTÓRICO ── */
  .historico-panel { display: none; padding: 1.5rem; overflow-y: auto; flex: 1; }
  .hist-card {
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 1rem 1.25rem;
    margin-bottom: 0.75rem;
    display: flex;
    align-items: center;
    gap: 1rem;
    cursor: pointer;
    transition: border-color 0.15s;
    background: var(--surface);
  }
  .hist-card:hover { border-color: var(--accent); }
  .hist-data { font-family: var(--mono); font-size: 0.68rem; color: var(--muted); }
  .hist-sector { font-weight: 600; font-size: 0.9rem; }
  .hist-total { font-family: var(--mono); font-size: 1.1rem; color: var(--accent); margin-left: auto; }
  .hist-estado {
    padding: 0.2rem 0.6rem;
    border-radius: 999px;
    font-family: var(--mono);
    font-size: 0.6rem;
  }
  .hist-estado.concluido { background: rgba(105,255,138,0.1); color: var(--frio); }
  .hist-estado.parado    { background: rgba(255,77,109,0.1);  color: var(--quente); }
  .hist-estado.em_curso  { background: rgba(0,229,255,0.1);   color: var(--accent); }

  /* ── EMPTY ── */
  .empty {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    height: 300px;
    color: var(--muted);
  }
  .empty-icon { font-size: 2.5rem; opacity: 0.3; }
  .empty-txt { font-family: var(--mono); font-size: 0.8rem; }

  /* ── PROGRESS ── */
  .progress-bar {
    height: 2px;
    background: var(--border);
    position: relative;
    overflow: hidden;
  }
  .progress-fill {
    height: 100%;
    background: linear-gradient(90deg, var(--accent), var(--accent3));
    transition: width 0.5s ease;
    width: 0%;
  }
  .progress-scanning {
    position: absolute;
    inset: 0;
    background: linear-gradient(90deg, transparent, var(--accent), transparent);
    animation: scan 1.5s linear infinite;
    display: none;
  }
  @keyframes scan { from { transform: translateX(-100%); } to { transform: translateX(200%); } }
  .progress-scanning.ativo { display: block; }

  /* ── TOAST ── */
  .toast {
    position: fixed;
    bottom: 1.5rem;
    right: 1.5rem;
    background: var(--surface);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent);
    padding: 0.75rem 1.25rem;
    border-radius: var(--radius);
    font-family: var(--mono);
    font-size: 0.75rem;
    z-index: 999;
    animation: toastIn 0.3s ease;
    max-width: 320px;
  }
  @keyframes toastIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
  .toast.erro  { border-left-color: var(--quente); }
  .toast.sucesso { border-left-color: var(--accent3); }

  /* ── SCROLLBAR ── */
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-track { background: transparent; }
  ::-webkit-scrollbar-thumb { background: var(--border); border-radius: 2px; }
</style>
</head>
<body>

<header>
  <div class="logo">lead<span>scanner</span>.pt</div>
  <div class="status-dot" id="statusDot"></div>
  <div class="status-txt" id="statusTxt">Inactivo</div>
  <nav>
    <button class="tab-btn active" onclick="showTab('scraper')">Scraper</button>
    <button class="tab-btn" onclick="showTab('historico')">Histórico</button>
  </nav>
</header>

<div class="layout" id="scraperTab">

  <!-- SIDEBAR -->
  <aside class="sidebar">

    <div>
      <div class="section-title">Configuração</div>

      <div style="margin-bottom:1rem">
        <label>Sector / Público-alvo</label>
        <select id="sector">
          <option value="construcao">🏗️ Construção Civil</option>
          <option value="remodelacao">🔨 Remodelação</option>
          <option value="reabilitacao">🏛️ Reabilitação</option>
          <option value="especialidades">⚡ Especialidades</option>
          <option value="imobiliario">🏠 Imobiliário</option>
          <option value="restauracao">🍽️ Restauração</option>
          <option value="clinicas">🏥 Clínicas / Saúde</option>
        </select>
      </div>

      <div style="margin-bottom:1rem">
        <label>Zonas geográficas</label>
        <div class="chips" id="zonasChips">
          <div class="chip selected" data-zona="Lisboa">Lisboa</div>
          <div class="chip selected" data-zona="Setubal">Setúbal</div>
          <div class="chip selected" data-zona="Almada">Almada</div>
          <div class="chip" data-zona="Barreiro">Barreiro</div>
          <div class="chip" data-zona="Seixal">Seixal</div>
          <div class="chip" data-zona="Montijo">Montijo</div>
          <div class="chip" data-zona="Palmela">Palmela</div>
          <div class="chip" data-zona="Sesimbra">Sesimbra</div>
          <div class="chip" data-zona="Cascais">Cascais</div>
          <div class="chip" data-zona="Sintra">Sintra</div>
          <div class="chip" data-zona="Oeiras">Oeiras</div>
          <div class="chip" data-zona="Amadora">Amadora</div>
        </div>
      </div>

      <div style="margin-bottom:1rem">
        <label>Máx. resultados por pesquisa</label>
        <input type="number" id="maxResultados" value="15" min="5" max="60">
      </div>
    </div>

    <div>
      <div class="section-title">Filtros</div>
      <div class="toggle-row">
        <span class="toggle-label">Só com telefone</span>
        <label class="toggle"><input type="checkbox" id="soTelefone" checked><span class="slider"></span></label>
      </div>
      <div class="toggle-row">
        <span class="toggle-label">Só sem website (leads quentes)</span>
        <label class="toggle"><input type="checkbox" id="soSemWebsite"><span class="slider"></span></label>
      </div>
    </div>

    <div>
      <button class="btn-iniciar" id="btnIniciar" onclick="iniciarSessao()">▶ INICIAR SCRAPING</button>
    </div>

    <div id="controloPanel" style="display:none">
      <div class="section-title">Controlo</div>
      <div class="controlo">
        <button class="btn-ctrl" id="btnPausar" onclick="comando('pausar')">⏸ Pausar</button>
        <button class="btn-ctrl success" onclick="exportarExcel()">📥 Excel</button>
        <button class="btn-ctrl danger" onclick="comando('parar')">⏹ Parar</button>
        <button class="btn-ctrl" onclick="copiarTelefones()">📋 Telefones</button>
      </div>
    </div>

    <div id="statsPanel" style="display:none">
      <div class="section-title">Resultados</div>
      <div class="stats-grid">
        <div class="stat-card">
          <div class="stat-num total" id="statTotal">0</div>
          <div class="stat-label">Total</div>
        </div>
        <div class="stat-card">
          <div class="stat-num quente" id="statQuente">0</div>
          <div class="stat-label">🔴 Quentes</div>
        </div>
        <div class="stat-card">
          <div class="stat-num medio" id="statMedio">0</div>
          <div class="stat-label">🟠 Médios</div>
        </div>
        <div class="stat-card">
          <div class="stat-num frio" id="statFrio">0</div>
          <div class="stat-label">🟢 Frios</div>
        </div>
      </div>
    </div>

  </aside>

  <!-- MAIN -->
  <main class="main">

    <div class="progress-bar">
      <div class="progress-fill" id="progressFill"></div>
      <div class="progress-scanning" id="progressScanning"></div>
    </div>

    <div class="toolbar">
      <span class="toolbar-title" id="toolbarTxt">Configure e inicie uma pesquisa</span>
      <div class="filtro-qualidade">
        <button class="fq-btn q active" onclick="filtrarQualidade('')">Todos</button>
        <button class="fq-btn q" onclick="filtrarQualidade('QUENTE')">🔴 Quente</button>
        <button class="fq-btn m" onclick="filtrarQualidade('MEDIO')">🟠 Médio</button>
        <button class="fq-btn f" onclick="filtrarQualidade('FRIO')">🟢 Frio</button>
      </div>
      <button class="btn-export" onclick="exportarExcel()">📥 Exportar Excel</button>
    </div>

    <div class="content-tabs">
      <div class="ctab active" onclick="showContent('leads')">Leads</div>
      <div class="ctab" onclick="showContent('log')">Log</div>
    </div>

    <!-- LEADS -->
    <div class="leads-container" id="leadsContainer">
      <div class="empty" id="emptyState">
        <div class="empty-icon">🔍</div>
        <div class="empty-txt">Configure uma pesquisa e clique em Iniciar</div>
      </div>
      <table class="leads-table" id="leadsTable" style="display:none">
        <thead>
          <tr>
            <th>Qualidade</th>
            <th>Nome</th>
            <th>Telefone</th>
            <th>Website</th>
            <th>Morada</th>
            <th>Pesquisa</th>
          </tr>
        </thead>
        <tbody id="leadsBody"></tbody>
      </table>
    </div>

    <!-- LOG -->
    <div class="log-container" id="logContainer"></div>

  </main>
</div>

<!-- HISTÓRICO -->
<div id="historicoTab" style="display:none; padding:1.5rem; overflow-y:auto; flex:1;">
  <div class="section-title">Sessões Anteriores</div>
  <div id="historicoLista"></div>
</div>

<script>
// URL da API — local ou produção automático
const API = window.location.hostname === 'localhost' || window.location.hostname === '127.0.0.1'
  ? 'http://localhost:8000'
  : window.location.origin

const WS_BASE = API.replace('https://', 'wss://').replace('http://', 'ws://')
let sessaoId     = null
let ws           = null
let todosLeads   = []
let filtroActivo = ''
let pausado      = false
let progTotal    = 0
let progActual   = 0

// ── Chips de zonas ──────────────────────────────────────────
document.querySelectorAll('.chip').forEach(chip => {
  chip.addEventListener('click', () => chip.classList.toggle('selected'))
})

// ── Tabs ────────────────────────────────────────────────────
function showTab(tab) {
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'))
  event.target.classList.add('active')
  document.getElementById('scraperTab').style.display  = tab === 'scraper'   ? 'grid' : 'none'
  document.getElementById('historicoTab').style.display = tab === 'historico' ? 'block' : 'none'
  if (tab === 'historico') carregarHistorico()
}

function showContent(ct) {
  document.querySelectorAll('.ctab').forEach(t => t.classList.remove('active'))
  event.target.classList.add('active')
  document.getElementById('leadsContainer').style.display = ct === 'leads' ? 'block' : 'none'
  document.getElementById('logContainer').style.display   = ct === 'log'   ? 'block' : 'none'
}

// ── Iniciar sessão ───────────────────────────────────────────
async function iniciarSessao() {
  const zonas = [...document.querySelectorAll('.chip.selected')].map(c => c.dataset.zona)
  if (!zonas.length) { toast('Selecciona pelo menos uma zona', 'erro'); return }

  const sector = document.getElementById('sector').value
  const tipos  = getTiposPorSector(sector)

  const config = {
    sector,
    zonas,
    tipos,
    so_com_telefone: document.getElementById('soTelefone').checked,
    so_sem_website:  document.getElementById('soSemWebsite').checked,
    max_resultados:  parseInt(document.getElementById('maxResultados').value) || 15,
  }

  try {
    const res  = await fetch(`${API}/api/sessao/iniciar`, {
      method: 'POST',
      headers: {'Content-Type': 'application/json'},
      body: JSON.stringify(config)
    })
    const data = await res.json()
    sessaoId   = data.sessao_id

    // Reset UI
    todosLeads = []
    document.getElementById('leadsBody').innerHTML = ''
    document.getElementById('leadsTable').style.display = 'none'
    document.getElementById('emptyState').style.display = 'none'
    document.getElementById('logContainer').innerHTML = ''
    atualizarStats(0, 0, 0, 0)

    // Mostrar controlo
    document.getElementById('controloPanel').style.display = 'block'
    document.getElementById('statsPanel').style.display    = 'block'
    document.getElementById('btnIniciar').disabled = true

    // Progresso
    progTotal  = zonas.length * tipos.length
    progActual = 0
    document.getElementById('progressFill').style.width = '0%'
    document.getElementById('progressScanning').classList.add('ativo')

    // Status
    setStatus('ativo', `A correr — sessão ${sessaoId}`)

    // WebSocket
    conectarWS(sessaoId)
    toast(`Sessão ${sessaoId} iniciada!`, 'sucesso')
  } catch(e) {
    toast('Erro ao ligar ao servidor. Verifica se o backend está a correr.', 'erro')
  }
}

function getTiposPorSector(sector) {
  const mapa = {
    construcao:     ['construcao civil', 'empresa construcao', 'construcao moradias'],
    remodelacao:    ['remodelacao', 'obras interiores', 'remodelacao casa'],
    reabilitacao:   ['reabilitacao imoveis', 'reabilitacao urbana'],
    especialidades: ['pintura predial', 'canalizacao', 'electricidade predial'],
    imobiliario:    ['agencia imobiliaria', 'mediacao imobiliaria', 'imobiliaria'],
    restauracao:    ['restaurante', 'cafe', 'pastelaria'],
    clinicas:       ['clinica dentaria', 'fisioterapia', 'clinica medica'],
  }
  return mapa[sector] || ['empresa ' + sector]
}

// ── WebSocket ────────────────────────────────────────────────
function conectarWS(sid) {
  ws = new WebSocket(`${WS_BASE}/ws/${sid}`)

  ws.onmessage = e => {
    const msg = JSON.parse(e.data)
    if (msg.tipo === 'ping') return

    adicionarLog(msg)

    if (msg.tipo === 'lead') {
      adicionarLead(msg.lead)
      const t = msg.total
      document.getElementById('statTotal').textContent = t

      progActual++
      document.getElementById('progressFill').style.width =
        Math.min(100, Math.round(progActual / Math.max(progTotal * 5, 1) * 100)) + '%'

      const q = todosLeads.filter(l => l.qualidade === 'QUENTE').length
      const m = todosLeads.filter(l => l.qualidade === 'MEDIO').length
      const f = todosLeads.filter(l => l.qualidade === 'FRIO').length
      atualizarStats(t, q, m, f)
    }

    if (msg.tipo === 'pesquisa') {
      document.getElementById('toolbarTxt').textContent =
        `[${msg.idx}/${msg.total}] ${msg.pesquisa}`
    }

    if (msg.tipo === 'concluido') {
      setStatus('', 'Concluído')
      document.getElementById('progressScanning').classList.remove('ativo')
      document.getElementById('progressFill').style.width = '100%'
      document.getElementById('btnIniciar').disabled = false
      document.getElementById('btnIniciar').textContent = '▶ NOVA PESQUISA'
      document.getElementById('toolbarTxt').textContent = msg.mensagem
      toast(msg.mensagem, 'sucesso')
    }

    if (msg.tipo === 'erro') {
      setStatus('erro', 'Erro')
      toast(msg.mensagem, 'erro')
    }
  }

  ws.onerror = () => {
    setStatus('erro', 'Sem ligação ao servidor')
  }
}

// ── Leads ────────────────────────────────────────────────────
function adicionarLead(lead) {
  todosLeads.push(lead)
  if (filtroActivo && lead.qualidade !== filtroActivo) return
  renderLead(lead)
}

function renderLead(lead) {
  const table = document.getElementById('leadsTable')
  if (table.style.display === 'none') {
    table.style.display = 'table'
    document.getElementById('emptyState').style.display = 'none'
  }

  const tr = document.createElement('tr')
  tr.className = 'lead-row'
  const web = lead.website === 'SEM WEBSITE'
    ? `<span class="sem-web">SEM WEBSITE</span>`
    : `<a class="web-link" href="${lead.website}" target="_blank" title="${lead.website}">
        ${lead.website.replace(/^https?:\/\//, '').slice(0, 25)}...
       </a>`

  tr.innerHTML = `
    <td><span class="badge ${lead.qualidade}">${lead.qualidade}</span></td>
    <td title="${lead.nome}">${lead.nome.slice(0, 30)}${lead.nome.length > 30 ? '…' : ''}</td>
    <td>${lead.telefone ? `<a class="tel-link" href="tel:${lead.telefone}">${lead.telefone}</a>` : '<span style="color:var(--muted)">—</span>'}</td>
    <td>${web}</td>
    <td title="${lead.morada}" style="color:var(--muted)">${(lead.morada||'').slice(0,25)}${(lead.morada||'').length > 25 ? '…' : ''}</td>
    <td style="color:var(--muted);font-family:var(--mono);font-size:0.65rem">${lead.pesquisa}</td>
  `
  document.getElementById('leadsBody').prepend(tr)
}

function filtrarQualidade(q) {
  filtroActivo = q
  document.querySelectorAll('.fq-btn').forEach(b => b.classList.remove('active'))
  event.target.classList.add('active')

  const body = document.getElementById('leadsBody')
  body.innerHTML = ''
  const filtrados = q ? todosLeads.filter(l => l.qualidade === q) : todosLeads
  filtrados.forEach(renderLead)

  if (filtrados.length === 0) {
    document.getElementById('leadsTable').style.display = 'none'
    document.getElementById('emptyState').style.display = 'flex'
  } else {
    document.getElementById('leadsTable').style.display = 'table'
    document.getElementById('emptyState').style.display = 'none'
  }
}

// ── Log ─────────────────────────────────────────────────────
function adicionarLog(msg) {
  const container = document.getElementById('logContainer')
  const div = document.createElement('div')
  const tipo = msg.tipo
  div.className = `log-line ${tipo === 'lead' ? 'ok' : tipo === 'erro' ? 'erro' : tipo === 'pesquisa' ? 'info' : ''}`
  const ts = new Date().toTimeString().slice(0,8)
  const txt = msg.mensagem || (msg.lead ? `Lead: ${msg.lead.nome}` : msg.pesquisa || JSON.stringify(msg))
  div.innerHTML = `<span class="ts">${ts}</span>${txt}`
  container.prepend(div)
}

// ── Comandos ─────────────────────────────────────────────────
async function comando(cmd) {
  if (!sessaoId) return
  await fetch(`${API}/api/sessao/${sessaoId}/comando`, {
    method: 'POST',
    headers: {'Content-Type': 'application/json'},
    body: JSON.stringify({comando: cmd})
  })

  if (cmd === 'pausar') {
    pausado = true
    document.getElementById('btnPausar').textContent = '▶ Continuar'
    document.getElementById('btnPausar').onclick = () => comando('continuar')
    setStatus('pausado', 'Pausado')
    document.getElementById('progressScanning').classList.remove('ativo')
  } else if (cmd === 'continuar') {
    pausado = false
    document.getElementById('btnPausar').textContent = '⏸ Pausar'
    document.getElementById('btnPausar').onclick = () => comando('pausar')
    setStatus('ativo', `A correr — sessão ${sessaoId}`)
    document.getElementById('progressScanning').classList.add('ativo')
  } else if (cmd === 'parar') {
    setStatus('', 'Parado')
    document.getElementById('progressScanning').classList.remove('ativo')
    document.getElementById('btnIniciar').disabled = false
    toast('Scraper parado.', '')
  }
}

async function exportarExcel() {
  if (!sessaoId) { toast('Inicia uma sessão primeiro', 'erro'); return }
  window.open(`${API}/api/sessao/${sessaoId}/exportar/excel`, '_blank')
}

function copiarTelefones() {
  const tels = todosLeads.map(l => l.telefone).filter(Boolean)
  navigator.clipboard.writeText(tels.join('\n'))
  toast(`${tels.length} telefones copiados!`, 'sucesso')
}

// ── Stats ────────────────────────────────────────────────────
function atualizarStats(t, q, m, f) {
  document.getElementById('statTotal').textContent  = t
  document.getElementById('statQuente').textContent = q
  document.getElementById('statMedio').textContent  = m
  document.getElementById('statFrio').textContent   = f
}

// ── Status ───────────────────────────────────────────────────
function setStatus(tipo, txt) {
  const dot = document.getElementById('statusDot')
  dot.className = 'status-dot ' + tipo
  document.getElementById('statusTxt').textContent = txt
}

// ── Histórico ────────────────────────────────────────────────
async function carregarHistorico() {
  const lista = document.getElementById('historicoLista')
  lista.innerHTML = '<div class="empty"><div class="empty-txt">A carregar...</div></div>'
  try {
    const res  = await fetch(`${API}/api/historico`)
    const data = await res.json()

    if (!data.length) {
      lista.innerHTML = '<div class="empty"><div class="empty-icon">📭</div><div class="empty-txt">Nenhuma sessão anterior</div></div>'
      return
    }

    lista.innerHTML = data.map(s => {
      const zonas = JSON.parse(s.zonas || '[]').join(', ')
      const data_ = new Date(s.criado_em).toLocaleString('pt-PT')
      return `
        <div class="hist-card" onclick="verSessao('${s.id}')">
          <div>
            <div class="hist-sector">${s.sector}</div>
            <div class="hist-data">${data_} · ${zonas}</div>
          </div>
          <span class="hist-estado ${s.estado}">${s.estado}</span>
          <div class="hist-total">${s.total_leads} leads</div>
        </div>
      `
    }).join('')
  } catch(e) {
    lista.innerHTML = '<div class="empty"><div class="empty-txt">Erro ao carregar histórico</div></div>'
  }
}

async function verSessao(sid) {
  showTab('scraper')
  document.querySelector('.tab-btn').classList.add('active')

  sessaoId = sid
  todosLeads = []
  document.getElementById('leadsBody').innerHTML = ''

  const res  = await fetch(`${API}/api/sessao/${sid}/leads?por_pagina=500`)
  const data = await res.json()
  data.leads.forEach(l => {
    todosLeads.push(l)
    renderLead(l)
  })

  const stats = await (await fetch(`${API}/api/sessao/${sid}/stats`)).json()
  atualizarStats(stats.total, stats.quentes, stats.medios, stats.frios)
  document.getElementById('statsPanel').style.display    = 'block'
  document.getElementById('controloPanel').style.display = 'block'
  setStatus('', `Sessão ${sid} (histórico)`)
}

// ── Toast ────────────────────────────────────────────────────
function toast(msg, tipo = '') {
  const el = document.createElement('div')
  el.className = `toast ${tipo}`
  el.textContent = msg
  document.body.appendChild(el)
  setTimeout(() => el.remove(), 4000)
}
</script>
</body>
</html>
