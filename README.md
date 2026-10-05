# Brick Bag Merge

A small personal web app for building LEGO sets. Import your BrickStore **.bsx** files
(one per bag), tick the bags you want to grab, and it sums identical parts across those
bags into one combined, sortable, printable pick-list — with part photos (BrickLink),
real names & categories (Rebrickable open data), and a Brick Architect link on each part.

Open the GitHub Pages URL (or `index.html` locally). Imported sets stay in your browser,
and can sync between devices through a private GitHub Gist (Import & edit → Sync).
In Chrome it can be installed as an app and works offline.

The app is in beta and uses semantic versioning; see `CHANGELOG.md`.

- `index.html` — the whole app (single file)
- `parts.json` — part names + categories (Rebrickable open data), loaded at runtime
- `manifest.webmanifest`, `sw.js`, `icon-*.png` — installable app and offline support
