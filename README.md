# portfoliov1

Personal portfolio site for myself, **Prashanta Purkayastha** — Product Manager based in Mumbai.

**Live:** [prashanta.work](https://prashanta.work)

## Overview

A single-page static portfolio, hand-rolled in one `index.html` file. No build step, no framework, no dependencies — just HTML, CSS, and vanilla JS with two webfont families pulled from Google Fonts.

The site is deployed via GitHub Pages with a custom domain (`prashanta.work`), configured through the `CNAME` file.

## Sections

- **Hero** — name, role, one-line pitch, primary CTAs
- **Stats banner** — animated count-up tiles (product roles, stores supported, etc.)
- **Experience** — timeline of product roles with bulleted highlights
- **Skills** — categorised tag clouds (Space Mono pills)
- **Achievements / Wins** — three-up grid of notable accomplishments
- **Education**
- **Contact** — direct links (email, LinkedIn, etc.)

## Design

- **Palette** — near-black background (`#0a0a0f`), warm off-white text (`#f0efe9`), gold accent (`#e8c547`)
- **Typography** — Syne (display), Outfit (body), Space Mono (labels & tags)
- **Texture** — SVG fractal-noise overlay + subtle geometric grid behind content
- **Motion** — fade-up animations on scroll via IntersectionObserver, scroll-progress bar, cursor-following accent glow (desktop only), floating geometric shapes in the hero (desktop only)
- **Responsive** — mobile-first; the layout collapses to single-column under 768px, with a hamburger overlay nav, full-width buttons, and a 2-column stats grid

Accessibility niceties:
- `prefers-reduced-motion` honoured (animations disabled, sections shown without transforms)
- Safe-area insets for notched phones
- Landscape-mobile breakpoint to prevent the hero swallowing the viewport
- `-webkit-tap-highlight-color: transparent` on interactive elements

## Repository layout

```
├── CNAME        # Custom domain (prashanta.work)
└── index.html   # Entire site — markup, styles, scripts
```

## Local preview

No tooling needed — open the file directly, or serve the folder with anything:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

Pushed to `main`, served by GitHub Pages. The `CNAME` file points the Pages output at `prashanta.work`.

## License

No license declared.
