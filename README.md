# Minesweeper (web app)

Static files only: no server code, no tracking, works offline after the first load.

## Host on GitHub Pages
1. Create a public repo (e.g. `minesweeper`) and upload these files to its root.
2. Repo → Settings → Pages → Source: "Deploy from a branch" → `main` / `(root)` → Save.
3. After a minute it's live at `https://<your-username>.github.io/minesweeper/`.

## Host on your own server
Serve this folder over HTTPS with any static web server (Caddy, nginx, etc.).
Offline mode (the service worker) only works over HTTPS.

## Add to iPhone
Open the URL in Safari → Share → Add to Home Screen. Launch it once while online
so it caches itself; after that it works with no connection.

Note: the Home Screen app keeps its own storage, separate from Safari,
so best times start fresh there.

## Updating
If you change any file, bump `CACHE` in `sw.js` (e.g. `minesweeper-v2`) so phones pick up the new version.
