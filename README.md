# Aftergen static site

A single-page static marketing site for Aftergen that highlights operational impact through automation, workflow tools, and pragmatic GenAI.

## Structure
- `index.html` – main page markup with hero, services, approach, case studies, proof points, and contact CTA.
- `styles.css` – design tokens and layout styling inspired by Afterskills aesthetic (purple/orange palette).

## Running locally
Because the site is fully static, you can open `index.html` directly in a browser or serve the folder:

```bash
cd /workspace/aftergen-site
python -m http.server 8000
```
Then visit http://localhost:8000.

## Notes
- External fonts: Space Grotesk + DM Mono from Google Fonts.
- Background images are pulled from Unsplash with gradient overlays; replace with branded assets as needed.
- CTAs use mailto/Calendly links; update to your scheduling links.
