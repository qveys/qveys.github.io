# qveys.github.io

Personal home page of Quentin Veys, served at <https://qveys.github.io/>.

## Structure

- `index.html` — the whole site: a single static page with inline CSS (light/dark theme via `prefers-color-scheme`), no build step.
- `og.png` — 1200×630 social preview image referenced by the `og:image` tag; regenerate it if the hero text changes.
- `.github/workflows/pages.yml` — deploys the repository root to GitHub Pages on every push to `main` (or manually via *Run workflow*).
- `.nojekyll` — disables Jekyll processing.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deployment

Pages source must be set to **GitHub Actions** (Settings → Pages), and the `github-pages` environment must allow deployments from `main` (Settings → Environments → `github-pages` → Deployment branches and tags).

To update the site, edit `index.html` and push to `main`; the workflow publishes it within a minute or two.
