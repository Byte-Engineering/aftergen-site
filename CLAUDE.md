# CLAUDE.md — Project Context for Claude Code

## Project Overview

AfterGen marketing website — a static site advertising operational improvement
services (automation, GenAI enablement, data platforms, change management).

## Tech Stack

- **Pure HTML + CSS** — no frameworks, no build tools, no package.json
- Google Fonts: Space Grotesk, IBM Plex Mono
- Zero dependencies — serve with any static server (e.g. `python -m http.server`)

## File Structure

```
├── assets/
│   └── styles.css       # All styles, dark theme, responsive (breakpoint: 720px)
├── index.html           # Main single-page site
├── privacy.html         # Simple privacy policy page
├── README.md            # Basic run instructions
└── CLAUDE.md            # This file
```

## Pages

### index.html — Main site (anchor nav)

- `#top` — Hero with value proposition, stats, CTA (discovery call email)
- `#services` — 4 service cards (Automation, GenAI, Data, Adoption)
- `#approach` — Methodology, proof metrics, timeline
- `#process` — 4-step delivery playbook + focus/prioritization cards + solution pillars
- `#cases` — 7 case studies (gov, fintech, retail, consulting)
- `#why` — Differentiators + industry coverage
- `#contact` — CTA panel with discovery call email + back-to-top

### privacy.html — Privacy policy

- Simple placeholder policy for a static site with no tracking or forms
- Reuses the same stylesheet and navbar as the main site
- Brand in header is an `<a class="brand">` linking back to index.html

## Design System

- Background: `#0e0a1f` (dark purple)
- Accent: `#ff7a1a` (orange)
- Text: `#f5f3ff` (light), `#cfc9e6` (muted)
- Cards use semi-transparent white overlays + backdrop blur (glassmorphism)
- Responsive grids with `auto-fit` and `clamp()` typography
- `scroll-padding-top: 80px` on `html` to offset sticky navbar on anchor nav
- Spacing between sibling blocks in `#process` via `#process .split, #process .stacked { margin-top: 24px }`

## Conventions

- No build step — edit HTML/CSS directly
- Keep it vanilla; do not introduce JS frameworks or bundlers unless explicitly requested
- Shared styles live in `assets/styles.css`; no inline styles unless page-specific
- Use semantic HTML and maintain the existing heading hierarchy
- Company name is **AfterGen** (capital G)
- New pages should reuse the same header/footer structure as index.html

## Git

- Main branch: `main`
- Do not commit the `.idea/` directory
