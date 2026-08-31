# Connie Huang — E-Portfolio

A single-page e-portfolio (Home, About, Research, Coursework, CV/Resume, Contact)
built with plain HTML, CSS, and JavaScript — no build step, so it deploys
directly to GitHub Pages.

## What's still a placeholder

Two required assets aren't in this build yet because they weren't uploaded.
Everything else (copy, layout, styling, download button, etc.) is finished
and live-ready.

1. **Headshot** — `assets/img/headshot-placeholder.svg` (a "CH" monogram) is
   standing in for your photo. To swap it in:
   - Add your photo to `assets/img/`, e.g. `headshot.jpg` (fix the sideways
     rotation before you upload it — most Photos/Preview apps have a rotate
     tool, or ask me to rotate it and I'll hand back a corrected file).
   - In `index.html`, find `id="heroPhoto"` and change its `src` from
     `assets/img/headshot-placeholder.svg` to `assets/img/headshot.jpg`.

2. **Résumé/CV PDF** — `assets/resume/Connie_Huang_CV.pdf` is currently a
   one-page placeholder explaining what to do. Export your real CV as a PDF,
   name it exactly `Connie_Huang_CV.pdf`, and drop it in that same folder,
   overwriting the placeholder. Both download buttons already point to that
   filename, so no code changes are needed.

Optional: `assets/img/research-figure.svg` is an illustrative graphic (not
real data) standing in for a chart/figure/photo from your actual project.
Swap in a real image or figure from your NHANES analysis when you have one —
just replace the file and keep the same filename, or update the `src` in the
Research section of `index.html`.

## Folder structure

```
portfolio/
├── index.html
├── css/style.css
├── js/script.js
├── assets/
│   ├── img/
│   │   ├── headshot-placeholder.svg
│   │   └── research-figure.svg
│   └── resume/
│       └── Connie_Huang_CV.pdf
└── README.md
```

## Deploy to GitHub Pages

1. **Create a repository** on GitHub (e.g. `e-portfolio`). Don't initialize
   it with a README — you already have one.

2. **Push this folder to it.** From inside this `portfolio` folder, run:

   ```bash
   git init
   git add .
   git commit -m "Initial e-portfolio"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/e-portfolio.git
   git push -u origin main
   ```

3. **Turn on Pages.** In the repo on GitHub: **Settings → Pages** →
   under "Build and deployment," set **Source** to `Deploy from a branch`,
   **Branch** to `main` and folder to `/ (root)` → **Save**.

4. **Find your URL.** After a minute or two, GitHub shows the live link at
   the top of that same Pages settings screen. It will look like:

   `https://YOUR-USERNAME.github.io/e-portfolio/`

   (If you name the repo `YOUR-USERNAME.github.io` exactly, your site lives
   at the root — `https://YOUR-USERNAME.github.io/` — instead of a
   subfolder.)

5. Re-push (`git add . && git commit -m "update" && git push`) any time you
   swap in your real photo or résumé — Pages redeploys automatically within
   a minute or two of each push.

## Customizing further

- **Colors** live as CSS custom properties at the top of `css/style.css`
  (the `:root` block) — change one value there and it updates everywhere.
- **Nav / section order** — edit the `<ul class="nav-links">` in `index.html`
  and reorder the `<section>` blocks to match.
- **Fonts** — currently Source Serif 4 (headings) + Inter (body), loaded from
  Google Fonts in the `<head>`.
