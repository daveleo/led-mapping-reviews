# LED mapping reviews — Claude instructions

Workspace rules in `D:\Work\CLAUDE.md` apply. Keep `PROJECT.md` and `CHANGELOG.md` current.

## What this is

Internal GitHub Pages site: one static page per reviewed NovaLCT `.scr` file, plus `index.html` listing them. Maps and decoding come from `projects\grid-system` (`make_grid.py`).

## How to run / build

Static HTML; nothing to build. Push `main` and GitHub Pages serves it.

## Rules specific to this project

- The site is public (GitHub Pages on a public repo) even though it is for internal use. Keep pages `noindex`, and leave customer names, sites and contact details off them unless Dawid says otherwise.
- Pushing publishes: ask before pushing.
- Generate tables from the decoded file, don't type coordinates by hand.
