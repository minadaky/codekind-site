# CodeKind static site

A minimal, sleek static website for CodeKind — a non‑profit building free or low‑cost open‑source projects that benefit the community.

## Structure
- `index.html` — Home
- `board.html` — Board of Directors
- `contact.html` — Contact and CTA
- `assets/css/styles.css` — Styles
- `assets/js/main.js` — Small JS for mobile nav
- `assets/img/` — Place your `logo.png` here, and optional `board1.jpg`, `board2.jpg`, `board3.jpg`.

## Using your logo
- Save your logo as `assets/img/logo.png` (ideally a square, 512×512 or similar). The site will automatically show it. If the image is missing, the layout gracefully hides the logo image.

## Local preview
You can use any static server. If you have Python installed:

```bash
# macOS / Linux
python3 -m http.server 8080
# then open http://localhost:8080 in your browser
```

Or with Node.js:

```bash
npx serve . -p 8080
```

## Deploy to GitHub Pages
This repo is set up for GitHub Pages via GitHub Actions.

1) Create a Git repo and push:

```bash
git init
git add -A
git commit -m "Initial site"
git branch -M main
git remote add origin git@github.com:<your-username>/<your-repo>.git
git push -u origin main
```

2) In GitHub: Settings → Pages → Build and deployment → Source: choose "GitHub Actions". The included workflow `.github/workflows/deploy-pages.yml` will deploy on each push to `main`.

URLs:
- Project page (recommended): https://<your-username>.github.io/<your-repo>/
- User/org page: https://<your-username>.github.io/ (place this site in that repo). All links here are relative, so both work.

Custom domain (optional):
- Add a `CNAME` file at the repo root containing your domain (e.g., `codekind.net`).
- Point DNS to GitHub Pages per GitHub’s docs (A/AAAA or ALIAS/CNAME records).

## Customize
- Update placeholder text and links in `board.html` and `contact.html`.
- Adjust colors in `assets/css/styles.css` under the `:root` variables.

## License
MIT — feel free to reuse for other non‑profits.
