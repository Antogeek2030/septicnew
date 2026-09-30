# Septic Pumping Niagara Falls NY

Astro.js website for **septicpumpingniagarafallsny.com** — professional septic tank pumping, inspection, repair, and emergency service serving Niagara Falls, Wilson, and Western New York.

## Features

- Responsive, mobile-friendly design
- Home, services (5 pages), service areas (with Google Maps embed for 3035 Daniels Rd, Wilson, NY 14172), contact, and blog
- Sitemap via `@astrojs/sitemap`
- `robots.txt`
- Cloudflare-ready (`@astrojs/cloudflare` adapter + Wrangler)

## Local development

```bash
npm install
npm run dev
```

## Build & deploy (Cloudflare Pages / Workers)

```bash
npm run build
npm run deploy   # or connect the repo to Cloudflare Pages
```

**Cloudflare Pages settings (recommended):**

- Build command: `npm run build`
- Build output directory: `dist`
- Node version: 22+

Or use the existing Wrangler setup:

```bash
npm run preview
npm run deploy
```

## Customize before launch

1. Update phone, email, and Formspree (or other form) endpoint in `src/consts.ts` and `src/pages/contact.astro`
2. Replace placeholder testimonials if desired
3. Add real photos under `public/` as needed

## Project structure

- `src/pages/` — routes (home, contact, service-areas, services/*, blog)
- `src/components/` — Header, Footer, BaseHead
- `src/layouts/Layout.astro` — shared layout
- `src/content/blog/` — markdown blog posts
- `public/robots.txt` — robots file
- Sitemap generated at build time to `/sitemap-index.xml`
