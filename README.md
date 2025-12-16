# umbrella — Eleventy site scaffold

This repository contains a minimal Eleventy (11ty) scaffold. The source templates live in the `site/` folder and the build output is written to `_site/`.

Quick start (locally):

1. Install dependencies:

   npm ci

2. Start a local dev server with live-reload:

   npm start

3. Build the static site:

   npm run build

How to change templates:

- Edit files under `site/`. Layouts are under `site/_layouts`, includes go in `site/_includes`.
- If your templates are in a different subfolder, update the `input` value in `.eleventy.js` to point to the folder where your template root lives.

Deployment:

- A GitHub Actions workflow builds the site on pushes to `main` and deploys the resulting `_site/` to GitHub Pages using the official Pages actions.

Notes:

- The scaffold does not commit build artifacts; the workflow builds on CI and publishes the site.
- To change the branch or other workflow behavior, edit `.github/workflows/deploy.yml`.