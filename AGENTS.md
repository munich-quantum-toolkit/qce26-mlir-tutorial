# AGENTS.md

Guidance for coding agents (and humans) working in this `website/` directory.

## Project Overview

This repository contains the standalone website for the QCE'26 tutorial
*"MLIR for Quantum-Classical Compilation: Building a Future‑Proof Compilation
Framework"*. It is published via GitHub Pages.

The site is a **single HTML page** with three sections, in this order:

1. **About the Tutorial** — abstract and relevance.
2. **Schedule** — the two-session tutorial schedule.
3. **Organizers** — a list of the tutorial organizers.

## Design Goals

- **Minimalistic setup above all else.** No build step, no bundler, no
  package manager, no JS framework, no CSS framework/preprocessor. Plain
  HTML5 + a single CSS file (+ a few lines of vanilla JS only if strictly
  needed for nav/scroll behavior). GitHub Pages must be able to serve the
  directory as-is with zero configuration beyond enabling Pages.
- **Visual style inspired by the TUM corporate design**: TUM blue
  (`#0065BD`), generous white space, clean sans-serif typography, simple
  top navigation bar, restrained use of color/imagery. Do not copy TUM
  assets verbatim — take inspiration from layout, color, and
  typography only.
- **Single page ("mono-page")**: all three sections live on `index.html`
  and are reachable via in-page anchor navigation (`#about`,
  `#schedule`, `#organizers`).
- **Static content only.** No CMS, no server-side code, no analytics.

## Repository / Directory Structure (target)

```
website/
├── AGENTS.md          # this file
├── PLANS.md            # high-level plan, links to exec_plans/
├── exec_plans/         # one file per sub-task, execution-ready
├── index.html          # the entire site (single page)
├── assets/
│   ├── css/
│   │   └── style.css   # single stylesheet
│   ├── img/             # any images (kept minimal)
│   └── favicon.ico
└── README.md           # short repo description
```

Do not introduce additional top-level directories or tooling files
(`package.json`, `node_modules/`, static site generator configs, etc.)
unless a future decision explicitly changes the "no build step" goal.

## Conventions

- Indent HTML/CSS with 2 spaces.
- Use semantic HTML5 elements (`<header>`, `<nav>`, `<main>`, `<section>`,
  `<footer>`) and one `<h1>` per page.
- Keep the CSS in a single file, organized with clear comment headers per
  section (Base, Layout, Navigation, About, Schedule, Organizers, Footer,
  Responsive).
- Prefer CSS variables (custom properties) for colors/spacing so the TUM
  color palette is defined once.

## How to Preview Locally

No build step is required. Any of the following works:

```bash
# Option 1: just open the file
open index.html

# Option 2: simple local server (recommended, avoids file:// quirks)
python3 -m http.server --directory website 8000
# then visit http://localhost:8000
```

## Deployment

This GitHub repository has GitHub Pages enabled on the default
branch, serving from the repository root. See
`exec_plans/07-deployment-github-pages.md` for the concrete steps.

## Working Agreement for Agents

- Follow the plan files in `exec_plans/` in order; update their status
  checkboxes as work completes.
- Do not add dependencies, frameworks, or build tooling without explicit
  user approval — this directly conflicts with the minimalism goal.
- Stop and ask before making structural/design decisions not already
  covered in `PLANS.md` or `exec_plans/`.
