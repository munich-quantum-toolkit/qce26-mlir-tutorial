# PLANS.md

High-level plan for building the QCE'26 tutorial website. This file
tracks overall status; each sub-task has a detailed, execution-ready
plan file under `exec_plans/`.

## Goal

Ship a minimalistic, single-page (mono-page) static website with three
sections — **About the Tutorial**, **Schedule**, **Organizers** — styled
in the spirit of the TUM corporate design, ready to be published via
GitHub Pages from its own repository.

## Non-Goals

- No build tooling, static site generators, or JS frameworks.
- No multi-page navigation — everything lives on one `index.html`.
- No CMS or dynamic backend.
- No pixel-perfect TUM branding clone — inspiration only (colors,
  typography, layout restraint), not asset reuse.

## Source Material

- `main.tex` — tutorial proposal (abstract, summary, target audience,
  relevance, format, contents/schedule, instructor bios).
- TUM website (`https://www.tum.de`) — visual/design reference only.

## Milestones & Execution Plans

Execute in order. Each item links to a plan file in `exec_plans/` with
detailed steps and acceptance criteria.

| # | Plan file | Description                                                                         | Status |
|---|-----------|-------------------------------------------------------------------------------------|--------|
| 1 | [`exec_plans/01-project-scaffold.md`](exec_plans/01-project-scaffold.md) | Minimal directory/file scaffold (`index.html`, `assets/css/style.css`, `README.md`) | ☐ Not started |
| 2 | [`exec_plans/02-design-system.md`](exec_plans/02-design-system.md) | TUM-inspired color palette, typography, spacing, base layout, nav bar               | ☐ Not started |
| 3 | [`exec_plans/03-content-about.md`](exec_plans/03-content-about.md) | "About the Tutorial" section content + markup                                       | ☐ Not started |
| 4 | [`exec_plans/04-content-schedule.md`](exec_plans/04-content-schedule.md) | "Schedule" section content + markup (two-session tables)                            | ☐ Not started |
| 5 | [`exec_plans/05-content-organizers.md`](exec_plans/05-content-organizers.md) | "Organizers" section content + markup (instructor bios)                             | ☐ Not started |
| 6 | [`exec_plans/06-navigation-accessibility.md`](exec_plans/06-navigation-accessibility.md) | Sticky nav, smooth scroll, mobile menu, responsive & accessibility pass             | ☐ Not started |

Status legend: ☐ Not started · ◐ In progress · ☑ Done

## Review Checkpoints

- **Checkpoint A** (after scaffold + design system): confirm look & feel
  direction before writing final content markup.
- **Checkpoint B** (after all three content sections): confirm semantic
  accuracy against `main.tex`.

## Open Questions (resolve with user before/at relevant milestone)

- Final tutorial date/time/location for the Schedule section header
  (not yet confirmed in `main.tex`).
- Whether a custom domain will be used for GitHub Pages, or the default
  `<user>.github.io/<repo>` URL.
- Whether to include presenter photos in the Organizers section (adds
  image assets; keep in mind minimalism goal).
