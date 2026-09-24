# Sulvx Omni Suite — V21 PWA

**24 professional tools** for Finance, Business, Education & Health  
+ **Live fiat exchange rates** + **5,000+ crypto prices** (CoinGecko)  
Installable as a **Progressive Web App** on phone & desktop.

## Features

- 24 calculators & tools (loan, BMI, invoice, QR, compound interest, etc.)
- **Fiat converter** — 30+ currencies, live ECB rates (Frankfurter)
- **Crypto converter** — 5,000+ coins via CoinGecko (search + convert)
- Real QR code generator + printable invoices
- Firebase Auth (email + Google) with verification
- Dark / light / system theme
- Offline-capable app shell (Service Worker)
- Install to home screen (Android / iOS / Desktop)

## Quick start (local)

1. Serve the folder over **HTTPS** or `localhost` (required for PWA & install):
   ```bash
   npx serve .
   # or
   python3 -m http.server 8080
   ```
2. Open the URL in Chrome / Edge / Safari
3. Use **Install** / **Add to Home Screen**

## Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `sulvx-app`)
2. Upload **all files** in this folder to the repo root (or a `/docs` folder)
3. Repo → **Settings** → **Pages**
4. Source: Deploy from branch `main` / root (or `/docs`)
5. After a minute, open: `https://YOUR_USERNAME.github.io/sulvx-app/`

> **Important:** Service Worker and install only work on **HTTPS** (GitHub Pages provides this) or localhost.

## Deploy to Netlify / Vercel

- Drag the whole `sulvx-pwa` folder onto [Netlify Drop](https://app.netlify.com/drop)
- Or connect the GitHub repo to Netlify / Vercel

## Firebase

Auth & project already configured: `sulvx-80fc7`  
Owner admin email: `sulvxapp@gmail.com`

## File structure

```
sulvx-pwa/
├── index.html          # Main app
├── manifest.json       # PWA manifest
├── sw.js               # Service worker
├── icons/              # App icons (72–512 + maskable)
└── README.md
```

## Notes

- Crypto list loads from CoinGecko free API (rate limits apply; avoid spam-refreshing)
- Fiat rates from Frankfurter / open.er-api
- QR codes via api.qrserver.com
- For production, consider your own domain + Firebase Hosting

Built with React 18, Tailwind, Firebase.
'''