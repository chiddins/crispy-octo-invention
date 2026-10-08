# Changelog

Brick Bag Merge uses [semantic versioning](https://semver.org). While the version
starts with `0.` the app is in beta: new features bump the middle number, fixes bump
the last one. It becomes `1.0.0` once it's stable.

Builds before 0.8.3 showed a plain build number in the header (v39 to v46). Each
version below lists that old number and the commits it covers.

## 0.18.0 (2026-10-08)
- Searching parts no longer freezes on big sets. Letters show up as you type and the
  list updates once you pause (a quarter of a second after the last letter), instead
  of after every letter. Rows that haven't changed are reused rather than rebuilt.
  In a test with 20 bags (640 parts) all selected, on a CPU slowed to tablet speed:
  each letter used to freeze the app for 1.3 to 2.2 seconds; now the filtered list
  shows about 0.35 s after you stop. Clearing the search went from 1.5 s to 0.5 s,
  and a pick from 3 s to 0.3 s.
- The Categories and Colours fields can't be typed into anymore. Tapping one opens
  its list, which has its own search box at the top ("Search colours"). That box
  isn't selected when the list opens, so the keyboard only comes up if you tap it.
  A search with no results says "No matches". With nothing picked, the field shows a
  down arrow.
- On a phone, when the field is near the bottom of the screen, the page scrolls up
  so the whole list is in view.
- The Search parts box gets the same blue outline as Categories and Colours while
  it has text in it.
- Pick some… and Edit total no longer put the cursor in the amount box, so the
  keyboard stays down. Use − / +, or tap the number to type one.
- The X in Search parts clears it without bringing the keyboard up.
- Backspace no longer removes the last chip, since the field has no text box. Use
  the chip's × or the X instead.

## 0.17.1 (2026-10-08)
- Fixed: tapping an option in the Categories or Colours list brought the keyboard
  back. Now the keyboard only comes up when you tap the text box itself. Picking
  from the list closes the keyboard, and the list stays open for more picks.
  Tapping the chips or the empty part of the field opens or closes the list without
  the keyboard.
- Escape closes an open filter list from anywhere, not only from inside the text
  box.
- In the Pick some… and Edit total dialogs, "4 of 59 picked so far" is yellow, or
  green once the part is complete.

## 0.17.0 (2026-10-08)
- The "Changes on two devices" dialog shows each device as a radio option, with when
  it last changed things and what it holds. The newer one starts selected and is
  marked Latest. The button says what will happen ("Use Android phone’s" or "Keep
  this device’s").
- The app now notes when this device last changed synced data, so it can tell which
  version is newer. Changes made before this version have no time, so in that case
  this device starts selected as before.

## 0.16.0 (2026-10-07)
- New "Pick some…" button beside Pick remaining and Pick N. It adds to what you've
  already picked: "Enter amount to pick", with − / + buttons, starting at the Pick N
  number. It shows which bag needs how many ("Bag 2 needs 12 · 4 of 59 picked so
  far") and what the total will be ("Picked will be 5 of 59") before you tap
  "Add 1". Earlier picks stay in their own bags.
- Setting the total moved to a pencil right after the "4/59 picked" count ("Edit
  total picked", same − / + layout, "Save total"). It used to sit among the buttons
  that add, which made it look like it added too. It's also there on finished parts,
  so you can fix an over-pick.
- When the remaining-parts threshold is met, Pick remaining becomes the solid yellow
  button and Pick N becomes the yellow outline.
- All text buttons now use the same type as the main Pick button (toolbar and dialog
  buttons were a little larger and lighter).

## 0.15.0 (2026-10-06)
- The Categories and Colours filters show what you've picked as small chips inside the
  field (colours keep their swatch). Each chip has its own × to remove it, and the
  field grows to fit them.
- Picking a value from the list adds its chip and clears whatever you'd typed, and
  the full list comes back for the next pick. Enter picks the first match and
  Backspace in an empty field removes the last chip.
- The X in a filter now clears the picked values and any typed text. It also shows
  as soon as you type.
- Both filter lists are in alphabetical order. Colours used to be ordered by
  BrickLink colour number.

## 0.14.4 (2026-10-06)
- "Brick Architect ↗" and "Brickset ↗" no longer split across two lines, and neither
  does "Part 3001" with its copy button. When the row is too narrow, a whole link
  moves to the next line, and that line doesn't start with a stray "·".

## 0.14.3 (2026-10-06)
- The colour tag now comes before the category tag on part rows, and in the part
  summary at the top of the custom-amount and Flag missing dialogs.

## 0.14.2 (2026-10-06)
- Fixed: the Remaining parts threshold box (and other boxes) offered saved passwords
  and codes. Chrome had grouped every box on the page into one login form with the
  GitHub token field. The token field now has a form of its own, so it's the only
  place passwords are offered, and autofill is off on every other box.

## 0.14.1 (2026-10-06)
- The green "Picked" button on finished rows is now a green outline instead of a solid
  green fill, matching the outlined "Pick remaining" button. In light mode it uses a
  darker green so the text stays readable.

## 0.14.0 (2026-10-06)
- Settings → Keep screen on stops the screen from going to sleep while the app is
  open. Android lets go of it when you switch away or turn the screen off, and the
  app takes it back when you return. It's remembered on each device and isn't
  synced. If the device refuses (battery saver, say), the menu says so.

## 0.13.0 (2026-10-05)
- Progress bars are yellow while there's still picking to do and turn green at 100%,
  along with their numbers ("520 / 520 · 0 left"), with the green tick before the
  percentage.
- Each bag in the Bags panel has a thin progress bar under its piece count, yellow
  until the bag is done, then green.
- A settings button (gear) replaces the light/dark button. Its menu has a Dark mode
  switch and Refresh app, which reloads to the latest version (it saves any changes
  waiting to sync first).
- "Bags selected" and "Total pieces" moved into the Bags panel. "Part types" and
  "Picked" are gone ("Picked" counted fully picked part types, not pieces). Select all
  moved up next to the Bags heading.
- Fixed: on tablets in landscape, the end of the Bags list could sit below the bottom
  of the screen until you'd scrolled the parts list right down. The panel now always
  fits on screen, so its last bag can always be scrolled into view.
- Ticking Show progress no longer resizes the Bags panel; it just moves down with the
  header.

## 0.12.0 (2026-10-05)
- Picking more of a part that's flagged missing asks about the flag first:
  "Pick and remove flag" if you found them, "Pick, keep flag" if they're still
  missing (say you picked that part for another bag), or Cancel. Picking every last
  one always clears the flag.
- Flagged parts get a "Remove flag" button next to "Flag missing". The button in the
  Flag missing dialog is called "Remove flag" too (it was "Mark all found (clear)").
- Each bag in the Bags panel shows its picked pieces on a second line under the
  name ("12 / 145 pieces"), with a green tick next to the name once it's complete.
- On phones the Reset / Flag missing / Remove flag buttons share the row evenly, and
  question dialogs stack their buttons full width.

## 0.11.0 (2026-10-05)
- The progress bars are back in the header, behind a "Show progress" switch to the
  right of the sync button. Tick it and the header grows to show both bars (selected
  bags and whole set); untick it to get the space back. The sticky footer is gone.
  The switch is remembered on each device and isn't synced.
- The header stays on one row at every width. On narrower screens the tagline goes,
  then the sync label, and on phones "Show progress" becomes an icon button.
- On phones each progress bar sits under its own numbers so nothing runs off the
  screen.
- Fixed: on 360px-wide phones the part list ran 8px past the right edge of the
  screen.
- Fixed: in light mode the empty part of a progress bar was almost invisible.

## 0.10.5 (2026-10-05)
- Fixed: the custom amount (pencil) was capped at the selected bags' total, so
  entering 10 for a part with 8 in the selected bags and 30 overall saved 8. The
  number is now your total for the part, up to everything in all bags; selected
  bags fill first, then the others. The dialog says so when other bags are involved.

## 0.10.4 (2026-10-05)
- Fixed: on wide screens the Bags panel ran behind the sticky footer, hiding the
  last bags. It now fits between the header and footer, and its list scrolls
  inside it (or shows every bag when there's room).

## 0.10.3 (2026-10-05)
- The stacked progress bars moved to a sticky footer along the bottom of the screen;
  the header is back to a single row.

## 0.10.2 (2026-10-05)
- Fixed: picking a custom amount (pencil button) marked the whole bag as done, so
  the row showed as fully picked with no way to pick the rest. Rows now show how
  many are still to get and a Pick button for them; entering 0 leaves the part
  unpicked; half-picked parts count as Unpicked.
- Enter on the keyboard confirms the custom-amount and Flag missing dialogs.

## 0.10.1 (2026-10-05)
- The two progress bars moved from the floating footer into the header, stacked:
  beside the title on wide screens, on their own row under it on narrower ones.

## 0.10.0 (2026-10-05)
- Floating progress bar at the bottom of the screen: pieces picked and left for the
  selected bags, and for the whole set.
- The header now stays at the top however far you scroll (it used to scroll away
  after the first screen).

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
