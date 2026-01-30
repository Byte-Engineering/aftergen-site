# CLAUDE.md — Project Context for Claude Code

## Project Overview

Aftergen marketing website — a single-page static site advertising operational
improvement services (automation, GenAI enablement, data platforms, change management).

## Tech Stack

- **Pure HTML + CSS** — no frameworks, no build tools, no package.json
- Google Fonts: Space Grotesk, IBM Plex Mono
- Zero dependencies — serve with any static server (e.g. `python -m http.server`)

## File Structure

```
├── assets/
│   └── styles.css       # All styles, dark theme, responsive (breakpoint: 720px)
├── index.html           # Entire single-page site
├── README.md            # Basic run instructions
└── CLAUDE.md            # This file
```

## Page Sections (anchor nav)

- `#top` — Hero with value proposition, stats, CTAs
- `#services` — 4 service cards
- `#approach` — Methodology, proof metrics, timeline
- `#process` — 4-step delivery playbook
- `#cases` — 7 case studies (gov, fintech, retail, consulting)
- `#why` — Differentiators
- `#contact` — CTA panel with Calendly + email

## Design System

- Background: `#0e0a1f` (dark purple)
- Accent: `#ff7a1a` (orange)
- Text: `#f5f3ff` (light), `#cfc9e6` (muted)
- Cards use semi-transparent white overlays + backdrop blur (glassmorphism)
- Responsive grids with `auto-fit` and `clamp()` typography

## Conventions

- No build step — edit HTML/CSS directly
- Keep it vanilla; do not introduce JS frameworks or bundlers unless explicitly requested
- All content lives in index.html; styles in assets/styles.css
- Use semantic HTML and maintain the existing heading hierarchy

## Git

- Main branch: `main`
- Do not commit the `.idea/` directory
