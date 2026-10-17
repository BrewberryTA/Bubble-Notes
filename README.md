# Bubble Notes (Orrery)

An infinite-canvas note app. Notes start as circles on a flat, gridded plane. Explode any note and it becomes a sphere with 48 predefined orbit slots (4 shells of 12) where child notes attach. Draw arrows between notes on the plane or in 3D. Organize separate subjects into their own canvases, and link between canvases with portal notes.

## Run it

This is a single static page — no build step. Open `index.html` in a browser, or serve the folder with any static file server:

```
npx serve .
```

It loads Three.js from a CDN (`three@0.159.0`) and Geist/Geist Mono from Google Fonts.

## Storage

The app looks for a `window.claude.use('db')` runtime (the Claude Artifacts platform) for synced, multi-device storage. Outside that environment it falls back to `localStorage` on the current device, with a bundled example canvas the first time it runs.

## Features

- **Plane / Orbit** — a 2D plane with an invisible snap grid; toggle into a 3D view where exploded notes lift off the plane.
- **Explode** — any note can open 48 predefined slots (4 concentric shells of 12) that fill one at a time.
- **Arrows** — automatic parent→child links, plus manual arrows between any two notes.
- **Canvases** — multiple independent boards, each with its own name, switchable from the top-left menu.
- **Portals** — a note can link to another canvas; click its badge to jump there, with a "back" pill to return.
- **Notes** — title, rich text body, tags, and 7 color swatches.

See `index.html` for the full implementation (single file, vanilla JS + Three.js).
