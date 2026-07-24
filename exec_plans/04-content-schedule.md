# 04 — Content: Schedule

## Goal

Write and mark up the **Schedule** section of `index.html` (id
`schedule`), presenting the two tutorial sessions and their timed
content.

## Context

Source content in `main.tex`.

## Steps

1. Add a heading (`<h2>`) "Schedule" plus a one-line intro (e.g., "Two
   90-minute sessions covering fundamentals through advanced
   backend-aware transformations.").
2. For each session, add an `<h3>` (e.g., "Session 1: MLIR
   Fundamentals and Dual‑Dialect Design (90 min)") followed by an
   HTML `<table>` with columns `Time [min]` / `Content`.
3. Add the "Deliverables" note after Session 2 (slide deck, code
   excerpts, links to MQT repository) as a short paragraph or callout
   box.
4. Note: if the tutorial's actual date/time/location has been
   confirmed by the user (see open question in `PLANS.md`), add it as
   a prominent line at the top of the section (e.g., "📅 Date · 🕒
   Time · 📍 Location — QCE'26"). If not yet confirmed, add a `<!--
   TODO: confirm date/time/location -->` HTML comment instead of
   inventing a placeholder date.
5. Style tables minimally: full-width, subtle row separators, header
   row in TUM blue or bold, responsive handling for narrow viewports
   (e.g., horizontal scroll wrapper `<div class="table-scroll">`).
   Add this CSS under `/* Schedule */` in `style.css`.

## Acceptance Criteria

- [ ] Both session tables render correctly and match the timing/
      content in `main.tex` exactly.
- [ ] Tables are responsive (no horizontal overflow breaking layout
      on mobile widths ~360px).
- [ ] Date/time/location either accurately included or explicitly
      marked as TODO — never fabricated.
- [ ] Deliverables note included after the schedule tables.

## Out of Scope

- About and Organizers content (plans 03, 05).
