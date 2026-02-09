# CLAUDE.md — Project Context for Claude Code

## Project Overview

AfterGen marketing website — a minimalist static site positioning custom-built
software as a faster, cheaper, and more tailored alternative to SaaS platforms.

## Tech Stack

- **Pure HTML + CSS + vanilla JS** — no frameworks, no build tools, no package.json
- Google Fonts: Space Grotesk
- Formspree for contact form submissions
- Zero dependencies — serve with any static server (e.g. `python -m http.server`)

## File Structure

```
├── assets/
│   └── styles.css       # All styles, dark theme, responsive (breakpoint: 600px)
├── index.html           # Main single-page site with canvas animation
├── privacy.html         # Simple privacy policy page
├── demo-*.html          # Animation demo pages (pipeline, orchestrator, reasoning, loop)
├── README.md            # Basic run instructions
└── CLAUDE.md            # This file
```

## Pages

### index.html — Main site (minimalist single-page)

- **Background animation**: Canvas-based "reasoning chain" — nodes progress left-to-right through swimlanes, occasionally branching; losing branches are pruned when a path enters a new stage; completed paths fade to ghost trails
- **Swimlanes**: Four labeled stages at top of viewport (Discover → Design → Implement → Refine) that light up as the animation progresses; hidden on mobile
- **Header**: Fixed navbar with brand + "Contact" link (scrolls to form)
- **Hero** (`#top`): Elevator pitch manifesto (two paragraphs) + bold guarantee statement
- **Stats**: Three inline metrics (annualized savings, cost reduction, delivery speed)
- **Contact form** (`#contact`): Email + message textarea, posts to Formspree (`https://formspree.io/f/mdalklwp`)
- **Footer**: Copyright, email, privacy link

Design inspired by [atlas.bio](https://atlas.bio/) — clean, text-focused, generous whitespace.

### privacy.html — Privacy policy

- Simple placeholder policy for a static site with no tracking
- Reuses the same stylesheet and navbar as the main site
- Brand in header is an `<a class="brand">` linking back to index.html

### demo-*.html — Animation prototypes

Standalone demo pages for different animation concepts (not linked from main site):
- `demo-pipeline.html` — Task flow pipeline
- `demo-orchestrator.html` — Central hub with orbiting tools
- `demo-reasoning.html` — Reasoning chain (basis for main site animation)
- `demo-loop.html` — Circular plan/execute/evaluate/refine cycle

## Design System

- Background: `#0a0a0a` (near-black)
- Accent: `#ff7a1a` (orange)
- Text: `#e8e8e8` (light), `#888` (muted)
- Max content width: `720px`
- Typography uses `clamp()` for responsive scaling
- Animation elements use low opacity (~10-12%) to stay subtle behind content
- Minimalist aesthetic — no cards, no glassmorphism, just text and whitespace

## Conventions

- No build step — edit HTML/CSS directly
- Keep it vanilla; do not introduce JS frameworks or bundlers unless explicitly requested
- Shared styles live in `assets/styles.css`; no inline styles unless page-specific
- Animation JS is inline in index.html `<script>` tag
- Use semantic HTML and maintain the existing heading hierarchy
- Company name is **AfterGen** (capital G)
- New pages should reuse the same header/footer structure as index.html

## Git

- Main branch: `main`
- Do not commit the `.idea/` directory or `demo-*.html` files
