# ash-portfolio

## Commands
- Serve locally: `python3 -m http.server 8000`
- Deploy preview: `npx vercel` · production: `npx vercel --prod`

## Architecture
- One self-contained `index.html`: CSS tokens at the top, markup, then one IIFE script.
- Themes: night is always the default and the OS setting is ignored. Day mode only comes from the switch (`localStorage['gotham-theme']`), and every color is a `:root` token.
- Hero: a canvas colony of bats forms the name. Scroll down plays a camera fly-through, and scroll up plays a homecoming dive (`sDir`, `cub()` in `draw`).
- Contact `#ra`: a canvas rooftop searchlight that follows the pointer. The `sent` class on `#ra` replays the emblem flicker.
- Contact form: `CF_ENDPOINT` (Formspree URL; empty = the visitor's email app). FormSubmit was dropped on 2026-11-05 because it returned 522 errors.

## Conventions
- Bat silhouette path: reuse the existing `M50 13L52.8…` path everywhere.
- Every animation respects `prefers-reduced-motion`. Canvas loops pause when offscreen.
