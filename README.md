# Wingman Streak Vault (public)

Static GitHub Pages site that serves **encrypted** streak-card soft copies.

- `index.html` + `app.js` — the decrypt page (runs AES-256-GCM in the browser via Web Crypto).
- `enc/<token>.bin` — one encrypted card per rider. Ciphertext only; useless without the rider's ID **and** the secret carried in their QR.

This repo is intentionally **public** so GitHub Pages works on the free plan. Nothing here is sensitive: it is all ciphertext plus a static page. The private generator, `manifest.csv` (secrets) and `qr/` live in the separate **private** `streak-calendar` repo and must never be committed here.

Encrypted files are produced by `tools/encrypt_images.py` in the private repo and copied into `enc/`.
