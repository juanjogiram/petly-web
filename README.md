# petly-web

Commercial landing page for **Petly** — the AI health copilot for your pet.

A single-page static site (HTML + CSS, no build). Audience: new visitors,
potential users and investors. It does not consume the backend.

## Structure

```
petly-web/
├── index.html     ← the whole landing (inline HTML + CSS + JS)
├── qr.png         ← download QR code (REPLACE with the real one)
└── README.md
```

## Run locally

No build needed. Open `index.html` in the browser, or serve the folder:

```bash
npx serve .
# or
python3 -m http.server 8000
```

## Replace the QR

The bundled `qr.png` is a placeholder pointing to the repo. Generate the real
one pointing to the APK download URL (or the Play Store once it exists):

```bash
pip install "qrcode[pil]"
python3 -c "import qrcode; qrcode.make('https://YOUR-DOWNLOAD-URL').save('qr.png')"
```

## Sections

Hero · Problem · Features (3 cards) · AI differentiator (with demo) ·
How it works (3 steps) · About us (team) · Download (QR) · Footer.

## Design

Premium indigo Petly palette: backgrounds `#1A1652 → #221E5C → #15123A`,
violet accent `#8251FD` / `#9D7BFF`, health green `#4ADE80`, aqua `#3FC9D0`.
Fredoka (display) + Nunito (body) typography. Glass cards with blur.
Responsive, accessible (visible focus, reduced-motion respected), basic SEO.

## Deploy

Any static host. Vercel recommended:

```bash
npx vercel --prod
```

Or drag the folder to Netlify Drop. No environment variables required.
