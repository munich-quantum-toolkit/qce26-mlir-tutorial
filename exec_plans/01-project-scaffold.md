# 01 — Project Scaffold

## Goal

Create the minimal set of files and folders needed to serve the site
with zero build tooling, as described in `../AGENTS.md`.

## Context

GitHub Pages can serve a plain static directory with no configuration
beyond enabling Pages on a branch. We only need `index.html` plus a
single stylesheet and an optional favicon/asset folder.

## Steps

1. Create the following structure inside `website/`:
   ```
   website/
   ├── index.html
   ├── assets/
   │   ├── css/
   │   │   └── style.css
   │   ├── img/            (empty initially, .gitkeep if needed)
   │   └── favicon.ico     (placeholder or omit until available)
   └── README.md
   ```
2. `index.html`: valid HTML5 boilerplate with:
   - `<html lang="en">`
   - `<head>` with `charset`, `viewport` meta, `<title>`, meta
     description, link to `assets/css/style.css`, favicon link.
   - `<body>` with empty `<header>`, `<nav>`, `<main>` containing three
     placeholder `<section>` elements with ids `about`, `schedule`,
     `organizers`, and a `<footer>`.
3. `assets/css/style.css`: empty file with section header comments
   (`/* Base */`, `/* Layout */`, `/* Navigation */`, `/* About */`,
   `/* Schedule */`, `/* Organizers */`, `/* Footer */`,
   `/* Responsive */`) to be filled in by plan 02.
4. `README.md` (short, for the future standalone repo): one-paragraph
   description of the site, link back to the tutorial, note that it's
   built with plain HTML/CSS and deployed via GitHub Pages, local
   preview instructions (copy from `AGENTS.md`).
5. Verify the page loads correctly via `python3 -m http.server` and
   renders (even if unstyled/empty) without console errors.

## Acceptance Criteria

- [ ] `index.html` validates as HTML5 (e.g., via W3C validator or
      `tidy`), contains the three placeholder sections with correct
      ids.
- [ ] `style.css` exists and is linked correctly from `index.html`.
- [ ] No build tool config files were introduced.
- [ ] Site loads via a simple local HTTP server with no 404s for
      linked assets.
- [ ] `README.md` created with minimal, accurate description.

## Out of Scope

- Actual visual design (colors, typography) — see plan 02.
- Real content — see plans 03–05.
