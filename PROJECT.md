---
name: LED mapping reviews
status: active
priority:
version: 2026-10-12
deadline:
next: Share the Mapping-Komplett-V01 review internally; update it when the four screen 2 checks are answered
updated: 2026-11-04
repo: daveleo/led-mapping-reviews
url: https://daveleo.github.io/led-mapping-reviews/
---

# LED mapping reviews

Internal GitHub Pages site with reviews of NovaStar NovaLCT screen files (`.scr`): what each file maps, what looks wrong, and cabinet maps to play on the screens. For Expromo colleagues.

## What it is for

When a NovaLCT mapping comes in for checking, its review goes here as one page: findings first, then each screen in detail, then the files (the `.scr` as received, exact-size cabinet maps, diagrams). The link is shared internally instead of attaching files.

## How to run

Nothing to build: the pages are static HTML. GitHub Pages serves the repo root of `main`.

## How to use

1. Put the `.scr` in `projects\grid-system\local\` and generate the maps: `python make_grid.py local/<name>.scr --out local/<name>` (PNGs need Cairo; on this PC render the SVGs with Edge).
2. Copy the maps and the `.scr` into a folder here (`<name>/`) and write `<name>.html` (copy `mapping-komplett-v01.html` as the model; its tables were generated from the decoded file, not typed).
3. Add a card for it at the top of `index.html`, commit and push. The page is live within a minute or two.

## What is what

- `index.html`: list of reviews, newest first
- `mapping-komplett-v01.html`: review of Mapping-Komplett-V01.scr (two screens)
- `mapping-komplett-v01/`: its files: the `.scr`, cabinet maps (PNG + SVG), screen 2 diagram, zoom crops
- `.nojekyll`: serve files as they are

## Current state

First review published 2026-10-12: Mapping-Komplett-V01.scr. Screen 1 (sending card 1, 6 × 9 cabinets of 72 × 32 px, 4 ports) is fine apart from a question about its port split. Screen 2 (sending card 3, 27 strips 2–4 px tall, 1886 × 15 px) has two 84 px overlaps (3-1-16/17, 3-1-17/18), reaches x 1886 past the 1680 px screen area, and uses sending card 3 with nothing on 2. Pages are public (GitHub Pages) but marked `noindex`; there is no customer name on them.

## Milestones

- [x] 2026-10-12 — Site created; first review: Mapping-Komplett-V01.scr

## Links

- Live: https://daveleo.github.io/led-mapping-reviews/
- Related: [[projects/grid-system/PROJECT|Grid_System]] (make_grid.py decodes the `.scr` and draws the maps)
