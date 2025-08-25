# Alpath® — Sitio estático listo para deploy (Vercel o Netlify)

## Estructura
- `index.html`
- `nevado-toluca.html`
- `assets/` (imágenes placeholder; reemplázalas por las definitivas)
- `vercel.json` (opcional, para Vercel — rewrites y headers)
- `_redirects` + `netlify.toml` (opcional, para Netlify — rutas bonitas y cache)

## Deploy con Vercel (vía GitHub)
1. Crea un repo y sube estos archivos.
2. Entra a Vercel → **Add New Project** → **Import Git Repository** → selecciona tu repo.
3. Configuración:
   - Framework: **Other** (Static)
   - Build Command: *(vacío)*
   - Output Directory: `/`
4. Deploy. Obtendrás `https://tu-sitio.vercel.app`. Agrega tu dominio en Settings → Domains.

## Deploy con Netlify (vía GitHub)
1. Netlify → **Add new site** → **Import from Git** → elige tu repo.
2. Build command: *(vacío)* · Publish directory: `/`
3. Deploy. Obtendrás `https://tu-sitio.netlify.app`. Agrega dominio en **Domain settings**.

## Rutas sin .html
- Vercel: `vercel.json` ya incluye rewrite de `/nevado-toluca` → `/nevado-toluca.html`
- Netlify: `_redirects` hace lo mismo.

## Reemplaza las imágenes
Sustituye los placeholders por tus archivos reales (mismos nombres) o cambia las variables CSS:
- Landing: `--hero` y `--hero-mobile` en `index.html`
- Nevado: `--hero` y `--hero-mobile` en `nevado-toluca.html`

> Los botones, hero responsivo y lazy-loading ya están listos.
