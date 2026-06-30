# petly-web

Landing comercial de **Petly** — el copiloto de salud con IA para tu mascota.

Sitio estático de una sola página (HTML + CSS, sin build). Público: visitantes
nuevos, potenciales usuarios e inversores. No consume el backend.

## Estructura

```
petly-web/
├── index.html     ← toda la landing (HTML + CSS + JS inline)
├── qr.png         ← código QR de descarga (REEMPLAZAR por el real)
└── README.md
```

## Ver en local

No necesita build. Abre `index.html` en el navegador, o sirve la carpeta:

```bash
npx serve .
# o
python3 -m http.server 8000
```

## Reemplazar el QR

El `qr.png` incluido es un placeholder que apunta al repo. Genera el real
apuntando a la URL de descarga del APK (o a la Play Store cuando exista):

```bash
pip install "qrcode[pil]"
python3 -c "import qrcode; qrcode.make('https://TU-URL-DE-DESCARGA').save('qr.png')"
```

## Secciones

Hero · Problema · Funciones (3 tarjetas) · Diferenciador IA (con demo) ·
Cómo funciona (3 pasos) · Quiénes somos (equipo) · Descarga (QR) · Footer.

## Diseño

Paleta índigo premium de Petly: fondos `#1A1652 → #221E5C → #15123A`,
acento violeta `#8251FD` / `#9D7BFF`, verde salud `#4ADE80`, aqua `#3FC9D0`.
Tipografía Fredoka (display) + Nunito (cuerpo). Tarjetas glass con blur.
Responsive, accesible (focus visible, reduced-motion respetado), SEO básico.

## Deploy

Cualquier hosting estático. Recomendado Vercel:

```bash
npx vercel --prod
```

O arrastra la carpeta a Netlify Drop. No requiere variables de entorno.
