[phases.setup]
nixPkgs = [
  "python311",
  "chromium",
  "nss",
  "nspr",
  "atk",
  "cups",
  "libdrm",
  "dbus",
  "libxkbcommon",
  "xorg.libX11",
  "xorg.libXcomposite",
  "xorg.libXdamage",
  "xorg.libXext",
  "xorg.libXfixes",
  "xorg.libXrandr",
  "mesa",
  "expat",
  "xorg.libxcb",
  "libxshmfence",
  "pango",
  "cairo",
  "alsa-lib",
]

[phases.install]
cmds = [
  "pip install -r backend/requirements.txt",
  "playwright install chromium",
]

[start]
cmd = "cd backend && python -m uvicorn main:app --host 0.0.0.0 --port $PORT"
