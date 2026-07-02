# P.U.L.S. Privacy Notice

A single static page: the public privacy notice for the P.U.L.S. desktop app.
It exists only to give the app a stable, public URL to link to.

The page is `index.html` — plain HTML, no build step.

## Publish it

1. Create a new **public** GitHub repo and push this folder's contents to `main`:

   ```bash
   git init
   git add .
   git commit -m "Add privacy notice page"
   git branch -M main
   git remote add origin git@github.com:<you>/<repo>.git
   git push -u origin main
   ```

2. In the repo on GitHub: **Settings → Pages → Build and deployment → Source → GitHub Actions**.

   That's the only click. The included workflow (`.github/workflows/deploy.yml`)
   deploys on every push to `main`.

3. Your URL will be `https://<you>.github.io/<repo>/`.

> The published page is **public to the internet** — that's the point. Keep the
> repo public (GitHub Pages needs a paid plan to publish from a private repo).

## Files

- `index.html` — the page (black text, white background, centered column).
- `.nojekyll` — tells Pages to serve files as-is, skipping Jekyll processing.
- `.github/workflows/deploy.yml` — auto-deploy on push.
