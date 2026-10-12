# Coffea — Landing page (HTML5 + CSS3)

TP4 · Diseño UX-UI · LSI FCyT UADER. Sitio estático sin JavaScript.

## Estructura
`index.html`, `404.html`, `css/` (capas con `@layer`: tokens, base, layout, components, utilities), `assets/{img,icons}`, `netlify.toml`.

## Levantar en local
Abrir `index.html` o correr `python3 -m http.server 8000`.

## Deploy (Netlify)
1. Subir el repo a GitHub/GitLab y conectarlo en Netlify.
2. Build command: vacío · Publish directory: `.`
3. `main` publica a producción; cada PR genera un Deploy Preview.

## CSS
- Fuente de verdad: `css/main.css` (capas con `@layer`) y sus módulos en `css/components/`.
- Producción: `css/styles.css` es el build minificado de esos módulos; `index.html` lo lleva en línea en un `<style>` para no bloquear el render (Lighthouse). `404.html` lo enlaza.
- Fuentes autoalojadas en `assets/fonts/` (Google Fonts, licencia OFL).

## Estado
- Imágenes: todas exportadas del Figma (hero, cafés, postres, granos, avatares) en WebP + JPG de respaldo vía `<picture>`.
- Íconos: SVG exportados del Figma.
- Publicado en Netlify: https://joyful-pithivier-1c2679.netlify.app
- Pendiente: confirmar la licencia de la foto de granos (`promo-beans`, origen iStock) antes de un uso comercial.
