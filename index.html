"""
Arranque correcto para Windows — força ProactorEventLoop ANTES do uvicorn.
Usa:  python run.py
"""
import sys
import asyncio

# CRÍTICO: definir ANTES de qualquer import do uvicorn/fastapi
if sys.platform == "win32":
    asyncio.set_event_loop_policy(asyncio.WindowsProactorEventLoopPolicy())
    loop = asyncio.ProactorEventLoop()
    asyncio.set_event_loop(loop)

import uvicorn

if __name__ == "__main__":
    uvicorn.run(
        "main:app",
        host="0.0.0.0",
        port=8000,
        reload=False,  # reload=True não funciona com ProactorEventLoop
        loop="asyncio",
    )
