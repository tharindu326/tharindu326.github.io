# Tharindu Ekanayake — Personal Homepage

A clean, fast, responsive academic personal homepage (light/dark theme, no build step).
Pure HTML/CSS/JS — works on GitHub Pages out of the box.

## Structure

```
.
├── index.html        # all page content
├── style.css         # theme + layout
├── script.js         # theme toggle, mobile menu, scroll-spy
├── .nojekyll         # tells GitHub Pages to serve files as-is
└── assets/
    ├── profile.jpg                 # portrait (extracted from CV)
    ├── Tharindu_Ekanayake_CV.pdf   # downloadable CV
    ├── favicon.svg
    ├── goava.png   (optional)      # company logo — see below
    ├── oulu.png    (optional)      # university logo
    ├── pub-3dpcnet.jpg (optional)  # publication teaser images
    ├── pub-scia.jpg    (optional)
    └── pub-thesis.jpg  (optional)
```

## Preview locally

Just open `index.html` in a browser, or run a tiny server:

```powershell
python -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a new public repo named **`<your-username>.github.io`** (a user site),
   or any repo name (a project site at `https://<user>.github.io/<repo>/`).
2. From this folder:

   ```powershell
   git init
   git add .
   git commit -m "Add personal homepage"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   select branch **`main`** and folder **`/ (root)`**. Save.
4. Your site goes live at `https://<your-username>.github.io/` in ~1 minute.

## Customizing

- **Optional logos / teaser images** — drop `goava.png`, `oulu.png`, or the `pub-*.jpg`
  files into `assets/`. They appear automatically; if a file is missing, the page falls
  back to a styled monogram / gradient, so nothing breaks.
- **GitHub link** — update the GitHub URL in `index.html` (search for `id="githubLink"`)
  once you have a profile/repo to point to.
- **Content** — all text lives in `index.html`; colors and spacing in `style.css`
  (CSS variables at the top of the file).
