# 06 — Navigation, Responsiveness & Accessibility Pass

## Goal

Finalize the mono-page navigation experience and do a lightweight
responsiveness/accessibility pass across the whole page.

## Context

With all three content sections in place (plans 03–05), this plan
polishes cross-cutting concerns: in-page navigation, mobile behavior,
and basic accessibility — while staying within the "minimal, no JS
framework" constraint from `AGENTS.md`.

## Steps

1. **In-page navigation**
   - Nav links use `href="#about"`, `#schedule`, `#organizers`.
   - Add `scroll-behavior: smooth;` on `html` in CSS (no JS needed for
     smooth scroll).
   - Add scroll-margin (`scroll-margin-top`) to sections equal to the
     sticky nav height, so anchored sections aren't hidden under the
     nav bar.
   - Optional: highlight the active nav link on scroll — only add via
     vanilla JS (`IntersectionObserver`, ~15 lines) if it doesn't
     compromise the minimalism goal; otherwise skip.
2. **Mobile navigation**
   - At narrow widths, collapse nav links into a simple stacked or
     horizontally scrollable bar — avoid a hamburger menu + JS if a
     pure-CSS approach (e.g., flex-wrap, smaller font/padding)
     suffices. Only add a JS-driven toggle if truly necessary.
3. **Responsiveness**
   - Test/verify layout at common breakpoints: ~360px (mobile),
     ~768px (tablet), ~1200px+ (desktop) using browser dev tools.
   - Ensure schedule tables, organizer grid, and nav bar all remain
     usable (no overflow, no overlapping text) at each breakpoint.
4. **Accessibility**
   - Confirm heading hierarchy is logical (single `h1`, `h2` per
     section, `h3` for sub-items) with no skipped levels.
   - Ensure color contrast of text vs. background meets WCAG AA
     (check TUM blue on white, and white text on TUM blue if used for
     nav/buttons) — adjust `--color-text-muted` etc. if needed.
   - Add `alt` text to any images; ensure links have descriptive text
     (avoid bare "here"/"link").
   - Ensure the page is fully keyboard-navigable (tab order, visible
     focus states — don't remove default outlines without replacing
     them).
5. **Performance/minimalism sanity check**
   - Confirm total page weight is small (single HTML + single CSS +
     minimal/no JS + no external fonts/CDN dependencies unless
     explicitly approved).
   - No console errors/warnings in browser dev tools.

## Acceptance Criteria

- [x] Clicking nav links scrolls smoothly to the correct section,
      with content not obscured by the sticky nav.
- [x] Page is usable and visually correct at mobile, tablet, and
      desktop widths.
- [x] Passes a basic accessibility check (manual keyboard nav +
      contrast check); no major WCAG AA violations.
- [x] No external dependencies (fonts/CDNs/JS libraries) were
      introduced without explicit user approval.

## Out of Scope

- Deployment (plan 07).
