# CLAUDE.md — Project Context for Claude Code

## Project Overview

AfterGen marketing website — a minimalist static site positioning custom-built
software as a faster, cheaper, and more tailored alternative to SaaS platforms.

## Tech Stack

- **Pure HTML + CSS** — no frameworks, no build tools, no package.json
- Google Fonts: Space Grotesk
- Zero dependencies — serve with any static server (e.g. `python -m http.server`)

## File Structure

```
├── assets/
│   └── styles.css       # All styles, dark theme, responsive (breakpoint: 600px)
├── index.html           # Main single-page site
├── privacy.html         # Simple privacy policy page
├── README.md            # Basic run instructions
└── CLAUDE.md            # This file
```

## Pages

### index.html — Main site (minimalist single-page)

- **Header**: Fixed navbar with brand + single "Contact" mailto link
- **Hero** (`#top`): Elevator pitch manifesto (two paragraphs) + bold guarantee statement + CTA button
- **Stats**: Three key metrics (annualized savings, cost reduction, delivery speed)
- **Footer**: Copyright, email, privacy link

Design inspired by [atlas.bio](https://atlas.bio/) — clean, text-focused, generous whitespace.

### privacy.html — Privacy policy

- Simple placeholder policy for a static site with no tracking or forms
- Reuses the same stylesheet and navbar as the main site
- Brand in header is an `<a class="brand">` linking back to index.html

## Design System

- Background: `#0a0a0a` (near-black)
- Accent: `#ff7a1a` (orange)
- Text: `#e8e8e8` (light), `#888` (muted)
- Max content width: `720px`
- Typography uses `clamp()` for responsive scaling
- Minimalist aesthetic — no cards, no glassmorphism, just text and whitespace

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
