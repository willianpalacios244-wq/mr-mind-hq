# Mr. Mind (web app)

Stick's pixel-art HQ as an installable phone app (PWA), hosted on GitHub Pages.

- `index.html`: the app (pixel office, cards, notifications button)
- `sw.js`: offline support + push notifications
- `manifest.webmanifest`, `icons/`: home-screen app name and icon
- `data/status.json`: the team data, **encrypted** (AES-GCM). Only phones opened with the setup link can read it.

Mr. Mind updates `data/status.json` and sends the notifications on every report with `Desktop/Mr. Mind/tools/hq_publish.py`.
Secrets (encryption key, notification keys, GitHub token) live only on Stick's Mac in `Desktop/Mr. Mind/app_secrets/`, never in this repo.
