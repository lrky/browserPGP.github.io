OpenPGP.js v6.2.0 (LOCAL) — Offline Setup
========================================

This site now uses a dedicated worker (js/pgp.worker.js) that loads OpenPGP.js **from a local file**
so everything works offline.

Steps:
1) Download OpenPGP.js v6.2.0 UMD build:
   - From npm:   `npm i openpgp@6.2.0`
     The file will be at: `node_modules/openpgp/dist/openpgp.min.js`
   - Or from a CDN when you *are online* (for one-time download), e.g.:
     `https://unpkg.com/openpgp@6.2.0/dist/openpgp.min.js`
2) Place that file at: `js/openpgp.min.js`
3) Serve the site over HTTPS (WebCrypto requires secure context). If testing locally, use `http://localhost`.

No other changes required. The pages communicate with the worker via `js/pgp-client.js`.
