# AGENTS.md

Static GitHub Pages site, no build step. Pushes to `main` deploy immediately to `mladenstojanovic.art` / `tntstupido.github.io`.

## File Naming
App pages: `[app-name]-[type].html` (types: `landing`, `privacy-policy`, `account-deletion`, `age-suitability`).

## New Page Checklist
- Add to `sitemap.xml` with `lastmod` (YYYY-MM-DD) and priority: 1.0 (index), 0.9 (landing), 0.5 (privacy), 0.4 (other)
- Update footer policy links in `index.html`

## Key Paths
- `assets/`: Static assets (images, videos, screenshots)
- `CNAME`: Points to `mladenstojanovic.art`
- `sitemap.xml`, `robots.txt`, `manifest.json`: SEO files
