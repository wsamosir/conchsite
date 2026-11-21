# Conch

Single-page scrolling site for the band Conch, built with Svelte 5 and Vite.

## Develop

```bash
npm install
npm run dev
```

## Build and preview

```bash
npm run build     # outputs static files to dist/
npm run preview   # serves dist/ locally
```

Deploy the contents of `dist/` to any static host (Netlify, Vercel, Cloudflare Pages, GitHub Pages).

## Structure

- `src/App.svelte` – page layout; the `sections` array drives both the nav and the page sections
- `src/lib/Header.svelte` – sticky header with nav links
- `src/lib/Section.svelte` – full-height section wrapper
- `src/app.css` – global styles and color tokens
