# Changelog

Brick Bag Merge uses [semantic versioning](https://semver.org). While the version
starts with `0.` the app is in beta: new features bump the middle number, fixes bump
the last one. It becomes `1.0.0` once it's stable.

Builds before 0.8.3 showed a plain build number in the header (v39 to v46). Each
version below lists that old number and the commits it covers.

## 0.9.0 (2026-10-05)
- Copy button next to each part number: tap it to copy just the number (it shows a
  green tick when copied).

## 0.8.3 (2026-10-05)
- Tapped part photos scale up to fill the screen instead of staying at their small
  original size, and refit when the device rotates.
- Photo captions say "Part 57539", matching the rows.
- Semantic versioning, with a Beta badge in the header.
- On phone-width screens the version sits under the title instead of the tagline.

## 0.8.2 (2026-09-27), was v46 (`de8bd32`)
- Sync button shows a tick cloud when synced and an x cloud on errors, with a
  "Synced … ago" label.
- Reset moved into the toolbar next to Print.
- "Open gist" button text is white in dark mode.

## 0.8.1 (2026-09-27), was v45 (`37b83f9`)
- Removed the per-bag line from part rows; 8px gaps between detail rows.

## 0.8.0 (2026-09-27), was v44 (`496622c`)
- Sync sets and picking progress between devices through a private GitHub Gist.
- Installable as a Chrome app, and works offline.
- Filter control labels use the same type as the bag list.

## 0.7.3 (2026-09-27), was v43 (`8b7a9b2`)
- Filled circle check for picked parts; part numbers labelled "Part 3022".

## 0.7.2 (2026-09-27), was v42 (`f861c5d`)
- Bigger colour swatches and progress icons; part number moved beside the links.

## 0.7.1 (2026-09-27), was v41 (`e61b70b`)
- One checkbox style and one clear-button style everywhere; yellow kept for picking
  actions only; the set name became a text-only heading.

## 0.7.0 (2026-09-26 to 27), was v40 (`44f5c86` to `f2843ec`)
- Colour swatches, multi-select category and colour filters, colour-aware Brickset
  links, and a Select all checkbox for bags.
- Text 20% larger; blue (#127ab8) for secondary controls.

## 0.6.0 (2026-09-26), was v39 (`f788540`)
- Version number shown in the header; picking by bag became the only pick model.

## 0.5.0 (2026-09-26, `f099cb3` to `2c8c0d6`)
- Pick by bag: partial picks, missing-part tracking with Flag missing, BrickLink
  colour names, and All / Unpicked / Picked / Missing views.

## 0.4.0 (2026-09-23 to 24, `a5d8547` to `0bb9721`)
- Part row redesigns: completed-row state, per-row reset, category tags, and an
  enter-an-amount dialog.

## 0.3.0 (2026-09-23, `255f2bb` to `a87ee08`)
- Mobile fixes (file picker, wrapping rows), per-part undo, and an adjustable
  low-remaining highlight.

## 0.2.0 (2026-09-22, `9ae5483` to `a208178`)
- Grab tracking per bag, filters, image sizes, other-bag info, and grab controls.

## 0.1.0 (2026-09-22, `999a7b6`)
- First version: import BrickStore .bsx bags into one combined pick-list with part
  photos, names, categories and Brick Architect links.
