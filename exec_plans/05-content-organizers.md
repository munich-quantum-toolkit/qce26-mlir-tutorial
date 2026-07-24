# 05 — Content: Organizers

## Goal

Write and mark up the **Organizers** section of `index.html` (id
`organizers`), presenting the instructor team.

## Context

Source content in `main.tex`, `\section{Instructor(s) bio(s)}`:
Yannick Stade (lead presenter), Lukas Burgholzer, Matthias Reumann,
Daniel Haag, Damian Rovara, Patrick Hopf, Robert Wille. Each has a bio
of varying length; some include a personal page link
(`\href{...}{www.cda.cit.tum.de/team/...}`).

## Steps

1. Add a heading (`<h2>`) "Organizers" plus a one-line intro (e.g.,
   "Meet the team behind the tutorial.").
2. Mark up each organizer as a simple card/list item containing:
   - Name (`<h3>`), with "Lead Presenter" badge/label for Yannick
     Stade.
   - Condensed bio (2–4 sentences — trim the longer LaTeX bios for
     web readability; preserve key facts: affiliation, role, research
     focus, notable achievements).
   - "More information" link where available (external link, `target
     ="_blank" rel="noopener"`).
3. Use a simple responsive grid or stacked list (CSS Grid/Flexbox,
   no framework) — e.g., 2–3 columns on wide viewports, 1 column on
   mobile. Add this under `/* Organizers */` in `style.css`.
4. Decide (confirm with user per `PLANS.md` open question) whether to
   include photos:
   - If yes: add `assets/img/organizers/<name>.jpg` placeholders and
     `<img>` tags with proper `alt` text; keep file sizes small.
   - If no: proceed with text-only cards (keeps minimalism goal
     intact, zero image assets).
5. Keep affiliations consistent (TUM / Munich Quantum Software Company)
   and avoid duplicating the full contact block from the LaTeX author
   list (that's for the paper, not the web bios).

## Acceptance Criteria

- [x] All seven organizers listed with accurate, condensed bios
      matching `main.tex` facts (no invented achievements/titles).
- [x] Lead presenter clearly indicated.
- [x] "More information" links work and open in a new tab where
      present in the source.
- [x] Layout is responsive and readable at mobile widths.
- [x] Text-only cards were used, so no organizer image assets were added.

## Out of Scope

- About and Schedule content (plans 03, 04).
