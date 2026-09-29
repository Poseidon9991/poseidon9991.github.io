# Hoeng Reaksa — Portfolio

Personal portfolio built with [Astro](https://astro.build), deployed on GitHub Pages.

Live at **https://poseidon9991.github.io**

## Local development

```bash
npm install
npm run dev      # dev server at localhost:4321
npm run build    # static build to dist/
```

## Editing content

All page content (experience, stack, case studies, education, contact links)
lives in `src/pages/index.astro` — search for the section you want to change.

## Deploy

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the
site and publishes it to GitHub Pages. In repo settings, Pages must be set to
**Source: GitHub Actions** (Settings → Pages).
