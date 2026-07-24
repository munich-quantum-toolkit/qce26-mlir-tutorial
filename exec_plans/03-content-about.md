# 03 — Content: About the Tutorial

## Goal

Write and mark up the **About the Tutorial** section of `index.html`
(the first section, id `about`).

## Context

Source content lives in `main.tex`:
- `\title{...}` — tutorial title.
- `\begin{abstract}...\end{abstract}` — public-facing abstract
  (~200–250 words).
- `\section{Summary}` — 1–2 sentence learning summary.
- `\section{Contents Level}` — beginner/intermediate/advanced split.
- `\section{Target Audience}` — expected background/prerequisites.
- `\section{Relevance}` — why it matters to QCE attendees (can be
  condensed; the full text is dense/proposal-oriented — trim for a
  public web audience).
- theres no need to stick word by word to the original text, rather improve on the
  original text.

## Steps

1. Add an `<h1>` with the tutorial title at the top of `<header>` or
   at the start of `#about` (decide placement based on plan 02 layout;
   title should appear once, prominently, above the nav or as a hero).
2. Populate `#about` with:
   - Short abstract/summary (adapted from the LaTeX abstract — trim
     citation-style phrasing like "\eg" to plain English "e.g.").
   - Include also the information of the sections "Who should attend" subsection from Target Audience.
   - "Contents level" as a simple visual breakdown (list or small
     bar), e.g. Beginner 30% / Intermediate 50% / Advanced 20%.
   - Optionally, a condensed "Why this matters" pulled from Relevance
     (2–3 sentences max — keep the page skimmable, not proposal-length).
3. Keep wording web-appropriate: shorter sentences than the LaTeX
   proposal, no LaTeX-specific escaping (`\mbox`, `\emph`, `~`), use
   `<em>`/`<strong>` instead of `\emph`/`\textbf`.
4. Link the presenters/organizers mention to the Organizers section
   anchor (`#organizers`) if referenced.
5. Add any section-specific CSS needed (e.g., styling for the
   contents-level breakdown) to `style.css` under the `/* About */`
   comment block.

## Acceptance Criteria

- [x] `#about` section contains title, abstract/summary, target
      audience, and contents-level breakdown, all in accurate,
      web-appropriate prose derived from `main.tex`.
- [x] No leftover LaTeX syntax or escaped characters in rendered text.
- [x] Section is legible and scannable (not a wall of text) —
      subheadings and/or short paragraphs used.
- [x] Content cross-checked against `main.tex` for factual accuracy
      (this is **Checkpoint B** material — flag for user review before
      finalizing across all three content sections).

## Out of Scope

- Schedule and Organizers content (plans 04, 05).
