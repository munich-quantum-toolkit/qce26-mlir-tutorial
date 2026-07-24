# 02 — Design System (TUM-Inspired, Minimal)

## Goal

Define a small, consistent visual design system — colors, typography,
spacing, base layout, and navigation bar — inspired by the TUM
corporate design, implemented purely in `assets/css/style.css` using
CSS custom properties.

## Context

TUM's public website uses a restrained palette anchored on "TUM Blue"
with white backgrounds, generous whitespace, and a clean sans-serif
typeface. We are not copying TUM assets or exact CSS — only taking
inspiration from color, spacing, and typographic restraint, per
`AGENTS.md`.

## Steps

1. Define CSS custom properties in `:root` in `style.css`:
   - `--color-primary: #0065BD;` (TUM blue)
   - `--color-primary-dark: #004a91;` (hover/active states)
   - `--color-accent: #64A0C8;` (lighter blue accent, optional)
   - `--color-bg: #ffffff;`
   - `--color-bg-alt: #f5f6f7;` (subtle section alternation)
   - `--color-text: #1c1c1c;`
   - `--color-text-muted: #555555;`
   - `--font-sans: -apple-system, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;`
   - spacing scale (`--space-1` … `--space-6`), max content width
     (`--content-max-width: 960px;`).
2. Base styles: reset margins, `box-sizing: border-box`, base font
   size (16px), line-height (~1.6), body background/text colors.
3. Layout: centered content container with `max-width` and horizontal
   padding; consistent vertical rhythm between sections
   (`section { padding: var(--space-6) 0; }`), alternating background
   (`--color-bg` / `--color-bg-alt`) between sections for subtle
   separation.
4. Navigation bar: fixed/sticky top bar, TUM-blue background or white
   background with a TUM-blue bottom border, site title on the left,
   three anchor links (About, Schedule, Organizers) on the right,
   hover/active underline in TUM blue.
5. Typography: clear heading hierarchy (`h1`–`h3`), consistent link
   styling (TUM blue, underline on hover), readable body text width
   (~70ch max within sections).
6. Footer: simple, muted, small text (e.g., copyright/contact link),
   centered.
7. Keep everything in the single `style.css` file — no additional
   stylesheets or preprocessors.

## Acceptance Criteria

- [x] All colors/spacing/fonts are defined once via CSS custom
      properties and reused (no hard-coded hex values scattered
      throughout).
- [x] Nav bar is visible, sticky, and visually distinct from content.
- [x] Typography renders legibly with clear visual hierarchy between
      `h1`/`h2`/`h3` and body text.
- [x] Page contains the full visual treatment in the same single-page structure from plan 01.
- [x] Design system implemented in the final page without adding external dependencies.

## Out of Scope

- Section-specific content markup (tables, bio cards, etc.) — later
  plans may add minor section-specific CSS, but the core system is
  defined here.
