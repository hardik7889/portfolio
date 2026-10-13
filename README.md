# Rahul Sharma — Portfolio

Personal portfolio website — 3D holographic "Holo Prism" design.

**Live:** https://rahul-sharma-dev.netlify.app

## About

Web developer portfolio built as a single self-contained HTML page — no build step,
no framework, no dependencies. Pure HTML + CSS + vanilla JS.

## Features

- **Holo Prism theme** — holographic portrait orb with rotating orbit rings, glow disc and travelling node
- **Portrait bleed** — the photo sits flush against the viewport edge for a cinematic split hero
- **Grayscale → colour** — the portrait wakes up in full colour on hover
- **3D tilt** — mouse-driven perspective tilt on the portrait and project cards
- **Multi-colour hover** — every text element turns bold with a flowing rainbow gradient and neon halo, while staying crisp and readable
- **Typewriter role line** — cycles through titles
- **Scroll reveals** — sections fade and lift into view
- **Marquee ticker** — skills strip along the bottom
- **Responsive** — collapses to a single column under 860px

## Content

Sections: Hero · About · Skills · Experience · Education · Projects · Achievements · Contact

Education includes **MCA (Master of Computer Applications), Amity University Online — completed 2026**.

## Structure

```
index.html                 the live site (Holo Prism)
assets/portrait_cut.webp   optimised portrait (100 KB, primary)
assets/portrait_cut_p8.png palette PNG fallback (144 KB)
assets/portrait_cut.png    original cutout (728 KB, source for future edits)
designs/                   6 alternative themes explored before Holo Prism
  v1-cyber-grid.html
  v2-neural-sphere.html
  v3-warp-tunnel.html
  v4-holo-globe.html
  v5-holo-prism.html
  v6-aurora-glass.html
```

## Design variants

Six themes were built and compared; Holo Prism was chosen. All variants are kept in
`designs/` and each is standalone — open any of them directly in a browser. They share
the same content and the same hover/multi-colour system, differing only in layout,
typography and background treatment.

## Running locally

No tooling required:

```bash
# just open it
start index.html        # Windows
open index.html         # macOS
```

Or serve it:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Hosted on Netlify (static drop deploy). To update, replace `index.html` and the
`assets/` files and redeploy.

## Notes

- The portrait background was removed with `rembg` (u2net model) and the alpha channel
  was hardened so semi-transparent pixels no longer let the holographic glow bleed
  through the subject.
- The portrait is served as WebP with a palette-PNG fallback via `<picture>` — 7× smaller
  than the original PNG at display resolution.

## License

Personal project — all rights reserved.
