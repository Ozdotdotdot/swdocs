# Smash Watch Documentation

This repo powers the documentation site for **Smash Watch**, a dashboard that visualizes competitive Super Smash Bros. player performance by state, tournament, and filters.

## Who this is for
- Players and TOs learning how to use the dashboard and filters
- Analysts reviewing how metrics are defined and charted
- Support/ops teams answering product questions

## What’s inside
- `content/` — Markdown docs (homepage, guides, reference)
- `public/` — Static assets
- `nuxt.config.ts` / `app.config.ts` — Docus/Nuxt configuration

## Run locally
```bash
npm install
npm run dev
# site at http://localhost:3000
```

## Contributing
- Edit Markdown in `content/`
- Use front matter `title` and `description` for the page hero
- Let Docus handle prev/next navigation; no manual footer links needed

## Deploy
```bash
npm run build
```
Build output goes to `.output/` for hosting.
