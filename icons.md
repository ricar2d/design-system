# Icons

**Source:** Icons Library (`-PD- Icons Library`)  
**External SVG assets:** Google Drive folder linked from library header

---

## Overview

The icon system is based on **Feather Icons** as a foundation, extended with custom product-specific icons. The library is organized into discrete size frames on a single canvas page ("Basic Icons").

---

## Size System

| Frame name | Size | Usage context |
|---|---|---|
| `Icon--32px` | 32×32px | Large contexts, empty states, feature illustrations |
| `Icon--24px` | 24×24px | Standard UI icons, navigation, toolbars |
| `Icon--16px` | 16×16px | Inline icons, input fields, compact UI |
| `Icon--12px` | 12×12px | Dense data tables, badges, tags, tight labels |
| `Icon--Filled` | mixed (8–16px) | Filled/solid variants — limited set |

> ✅ **Found in library:** All four stroke sizes are present and consistent. The naming system is clear.

---

## Naming Convention

### Inconsistency — Two different naming patterns by size

| Size frame | Property key | Example |
|---|---|---|
| `Icon--32px` | `Icon=[name]` | `Icon=calendar`, `Icon=chevron-down` |
| `Icon--24px` | `Type=[name]` | `Type=calendar`, `Type=chevron-down` |
| `Icon--16px` | `Type=[name]` | `Type=calendar`, `Type=chevron-down` |
| `Icon--12px` | `Type=[name]` | `Type=calendar`, `Type=chevron-down` |
| `Icon--Filled` | `Type=[name]` | `Type=pin`, `Type=dot` |

> ⚠️ **Inconsistency found:** The 32px frame uses the prefix `Icon=` while all smaller sizes use `Type=`. This creates inconsistency in how icons are referenced in components that use different sizes. The system should standardize on a single property key — `Icon=` is recommended as it more clearly communicates the element type.

---

## Stroke Style

All standard icons are **stroke-based (outline)** at 2px stroke weight, following the Feather Icons specification.

| Frame label | Stroke weight |
|---|---|
| `Elements / 2px stroke` | 2px (32px and 24px frames) |
| `Elements / 1px stroke` | 1px (16px and 12px frames) |

> ✅ Stroke weight scales proportionally with icon size, maintaining visual consistency across sizes.

---

## Filled Icons

A small set of filled (solid) icons exists in the `Icon--Filled` frame:

| Name | Size |
|---|---|
| `Type=pin` | 16×16px |
| `Type=x-circle-small` | 10×10px |
| `Type=dot` | 8×8px |

> ⚠️ **Inconsistency:** The filled icon set is extremely limited (3 icons) compared to the ~350 stroke icons. This suggests filling in states were handled ad-hoc rather than systematically. The system should define when filled vs stroke icons are used.

---

## Exact Icon Count (from Figma source)

| Frame | Unique icons | Notes |
|---|---|---|
| `Icon--32px` | **302** | Full base set |
| `Icon--24px` | ~302 + 8 extras | Adds: `facebook`, `twitter`, `twitch`, `figma`, `git-pull-request`, `bluetooth`, `chevrons-down`, `chevrons-up` |
| `Icon--16px` | ~302 + 4 extras | Adds: `hexagon-variant`, `Undo`, `Redo`, `more-vertical` |
| `Icon--12px` | ~290 | Subset — some less-used icons omitted |
| `Icon--Filled` | **3** | `pin`, `x-circle-small`, `dot` only |
| **Total unique** | **~314** | |

---

## Complete 32px Icon Catalogue (302 icons)

`activity` · `airplay` · `alert-circle` · `alert-octagon` · `alert-triangle` · `align-center` · `align-justify` · `align-left` · `align-right` · `anchor` · `aperture` · `archive` · `arrow-down` · `arrow-down-circle` · `arrow-down-left` · `arrow-down-right` · `arrow-left` · `arrow-left-circle` · `arrow-right` · `arrow-right-circle` · `arrow-up` · `arrow-up-circle` · `arrow-up-left` · `arrow-up-right` · `asterisk` · `at-sign` · `award` · `bar-chart` · `bar-chart-2` · `battery` · `battery-charging` · `bell` · `bell-off` · `bold` · `book` · `book-open` · `bookmark` · `box` · `briefcase` · `calculator` · `calendar` · `calendar-appointment` · `calendar-day` · `calendar-month` · `calendar-today` · `calendar-week` · `camera` · `camera-off` · `cast` · `check` · `check-circle` · `check-square` · `chevron-down` · `chevron-left` · `chevron-right` · `chevron-up` · `chevron-up-down` · `chevrons-left` · `chevrons-right` · `chrome` · `circle` · `clipboard` · `clock` · `clock-alert` · `cloud` · `cloud-drizzle` · `cloud-lightning` · `cloud-off` · `cloud-rain` · `cloud-snow` · `code` · `codepen` · `codesandbox` · `coffee` · `columns` · `command` · `compass` · `copy` · `corner-down-left` · `corner-down-right` · `corner-left-down` · `corner-left-up` · `corner-right-down` · `corner-right-up` · `corner-up-left` · `corner-up-right` · `coulmn-view` *(12px/24px only, misspelling)* · `cpu` · `credit-card` · `crop` · `crosshair` · `database` · `delete` · `disc` · `divide` · `divide-circle` · `divide-square` · `dollar-sign` · `download` · `download-cloud` · `droplet` · `edit` · `edit-2` · `edit-3` · `external-link` · `eye` · `eye-off` · `fast-forward` · `feather` · `file` · `file-csv` · `file-minus` · `file-pdf` · `file-plus` · `file-text` · `file-xls` · `fill-color` · `film` · `filter` · `flag` · `folder` · `folder-minus` · `folder-open` · `folder-plus` · `font-color` · `formula` · `frown` · `gift` · `git-branch` · `git-commit` · `git-merge` · `globe` · `grabber` · `grid` · `hard-drive` · `hash` · `headphones` · `heart` · `help-circle` · `hexagon` · `home` · `image` · `info` · `italic` · `key` · `layers` · `layout` · `life-buoy` · `link` · `link-2` · `list` · `loader` · `lock` · `log-in` · `log-out` · `mail` · `mail-dot` · `map` · `map-pin` · `maximize` · `maximize-2` · `meh` · `menu` · `message-circle` · `message-square` · `mic` · `mic-off` · `minimize` · `minimize-2` · `minus` · `minus-circle` · `minus-square` · `monitor` · `moon` · `more-horizontal` · `more-vertical` · `mouse-pointer` · `move` · `music` · `navigation` · `navigation-2` · `nested-in` · `nested-out` · `not-equal` · `octagon` · `org` · `package` · `paperclip` · `pause` · `pause-circle` · `pen-tool` · `percent` · `phone` · `phone-call` · `phone-forwarded` · `phone-incoming` · `phone-missed` · `phone-off` · `phone-outgoing` · `pie-chart` · `pin` · `pip` · `plane` · `play` · `play-circle` · `plus` · `plus-circle` · `plus-square` · `pocket` · `power` · `printer` · `question` · `radio` · `refresh-ccw` · `refresh-cw` · `repeat` · `rewind` · `rotate-ccw` · `rotate-cw` · `rss` · `save` · `scissors` · `search` · `send` · `server` · `settings` · `share` · `share-2` · `shield` · `shield-off` · `shopping-bag` · `shopping-cart` · `shuffle` · `sidebar left` *(space, not hyphen)* · `sidebar right` *(space, not hyphen)* · `skip-back` · `skip-forward` · `slack` · `slash` · `sliders` · `smartphone` · `smile` · `speaker` · `square` · `star` · `star-active` · `stop-circle` · `sun` · `sunrise` · `sunset` · `tablet` · `tag` · `target` · `terminal` · `thermometer` · `thumbs-down` · `thumbs-up` · `title-above-table` · `title-bellow-table` *(misspelling)* · `toggle-left` · `toggle-right` · `tool` · `top filter` *(space, not hyphen)* · `trash-2` · `trello` · `trending-down` · `trending-up` · `triangle` · `truck` · `tv` · `type` · `umbrella` · `underline` · `unlock` · `upload` · `upload-cloud` · `user` · `user-check` · `user-minus` · `user-plus` · `user-x` · `users` · `users-2` · `video` · `video-off` · `voicemail` · `volume` · `volume-1` · `volume-2` · `volume-x` · `watch` · `wifi` · `wifi-off` · `wind` · `x` · `x-circle` · `x-octagon` · `x-square` · `youtube` · `zap` · `zap-off` · `zoom-in` · `zoom-out`

## 24px-only Icons (not in 32px frame)

`bluetooth` · `chevrons-down` · `chevrons-up` · `facebook` · `figma` · `git-pull-request` · `twitch` · `twitter`

## 16px-only Icons (not in 32px frame)

`hexagon-variant` · `Undo` *(capitalised — inconsistency)* · `Redo` *(capitalised — inconsistency)* · `more-vertical`

## Filled Icons (Icon--Filled frame)

`Type=pin` (16px) · `Type=x-circle-small` (10px) · `Type=dot` (8px)

---

## Full Icon Catalogue (legacy grouped view)

### Navigation & Directional
`arrow-up` · `arrow-down` · `arrow-left` · `arrow-right` · `arrow-up-left` · `arrow-up-right` · `arrow-down-left` · `arrow-down-right` · `arrow-up-circle` · `arrow-down-circle` · `arrow-left-circle` · `arrow-right-circle` · `chevron-up` · `chevron-down` · `chevron-left` · `chevron-right` · `chevron-up-down` · `chevrons-up` · `chevrons-down` · `chevrons-left` · `chevrons-right` · `corner-down-left` · `corner-down-right` · `corner-left-down` · `corner-left-up` · `corner-right-down` · `corner-right-up` · `corner-up-left` · `corner-up-right` · `navigation` · `navigation-2`

### Actions
`edit` · `edit-2` · `edit-3` · `save` · `copy` · `paste` _(not found)_ · `delete` · `trash-2` · `archive` · `download` · `download-cloud` · `upload` · `upload-cloud` · `share` · `share-2` · `send` · `print` / `printer` · `refresh-cw` · `refresh-ccw` · `rotate-cw` · `rotate-ccw` · `repeat` · `plus` · `plus-circle` · `plus-square` · `minus` · `minus-circle` · `minus-square` · `x` · `x-circle` · `x-octagon` · `x-square` · `check` · `check-circle` · `check-square` · `search` · `zoom-in` · `zoom-out` · `filter` · `sliders` · `log-in` · `log-out` · `external-link` · `link` · `link-2` · `scissors` · `crop` · `move` · `maximize` · `maximize-2` · `minimize` · `minimize-2`

### Communication
`mail` · `mail-dot` · `message-square` · `message-circle` · `phone` · `phone-call` · `phone-forwarded` · `phone-incoming` · `phone-missed` · `phone-off` · `phone-outgoing` · `voicemail` · `send` · `rss` · `wifi` · `wifi-off` · `bluetooth` · `at-sign`

### Files & Data
`file` · `file-plus` · `file-minus` · `file-text` · `file-pdf` · `file-csv` · `file-xls` · `folder` · `folder-open` · `folder-plus` · `folder-minus` · `clipboard` · `paperclip` · `database` · `server` · `hard-drive` · `archive` · `layers` · `layout` · `columns` · `grid` · `list` · `align-left` · `align-center` · `align-right` · `align-justify` · `coulmn-view`

### Users & People
`user` · `users` · `users-2` · `user-check` · `user-minus` · `user-plus` · `user-x` · `briefcase`

### Calendar & Time
`calendar` · `calendar-today` · `calendar-month` · `calendar-week` · `calendar-day` · `calendar-appointment` · `clock` · `clock-alert` · `watch`

### Media & UI Controls
`play` · `play-circle` · `pause` · `pause-circle` · `stop-circle` · `rewind` · `fast-forward` · `skip-back` · `skip-forward` · `volume` · `volume-1` · `volume-2` · `volume-x` · `mic` · `mic-off` · `camera` · `camera-off` · `video` · `video-off` · `image` · `film` · `music` · `headphones` · `speaker` · `radio` · `tv` · `monitor`

### Status & Feedback
`alert-circle` · `alert-triangle` · `alert-octagon` · `info` · `help-circle` · `check-circle` · `x-circle` · `bell` · `bell-off` · `loader` · `activity` · `trending-up` · `trending-down` · `star` · `star-active` · `heart` · `thumbs-up` · `thumbs-down` · `smile` · `meh` · `frown`

### Maps & Location
`map` · `map-pin` · `globe` · `compass` · `navigation` · `navigation-2` · `plane`

### Commerce & Business
`shopping-cart` · `shopping-bag` · `credit-card` · `dollar-sign` · `percent` · `tag` · `package` · `gift` · `truck` · `target`

### Charts & Analytics
`bar-chart` · `bar-chart-2` · `pie-chart` · `trending-up` · `trending-down` · `activity`

### Text Formatting (Rich Text)
`bold` · `italic` · `underline` · `type` · `font-color` · `fill-color` · `align-left` · `align-center` · `align-right` · `align-justify` · `list`

### Developer / Technical
`code` · `codepen` · `codesandbox` · `terminal` · `cpu` · `server` · `database` · `git-branch` · `git-commit` · `git-merge` · `git-pull-request` · `command` · `hash` · `key` · `lock` · `unlock` · `shield` · `shield-off`

### Product-Specific (Custom / non-Feather)
`org` · `pip` (Picture-in-Picture) · `grabber` · `sidebar left` · `sidebar right` · `top filter` · `title-above-table` · `title-bellow-table` · `formula` · `not-equal` · `asterisk` · `nested-in` · `nested-out` · `clock-alert` · `calendar-today` · `calendar-month` · `calendar-week` · `calendar-day` · `calendar-appointment` · `file-pdf` · `file-csv` · `file-xls` · `mail-dot` · `coulmn-view` · `Undo` · `Redo` · `question` · `hexagon-variant` (16px only)

---

## Custom Icons vs Feather Base

| Category | Count (approx) | Notes |
|---|---|---|
| Feather Icons base | ~280 | Standard set, consistent stroke style |
| Custom product icons | ~25+ | Calendar variants, CRM-specific, formatting tools |
| Social/brand icons | ~8 | `slack`, `trello`, `chrome`, `facebook`, `twitter`, `twitch`, `youtube`, `figma` |

---

## Usage Patterns

- Icons are used as **Figma symbols** (components) — not inline SVGs in the design tool
- SVG files are stored externally in a **Google Drive folder** (linked from library)
- Icons inherit color from parent — they do not have hardcoded fill colors
- Typical colors: `clr-neutral/55` (`#627494`) for inactive, `clr-royal/50` (`#0073e5`) for active/brand, `clr-wine/50` (`#dc3838`) for destructive actions

---

## Issues & Inconsistencies

| Issue | Severity | Action |
|---|---|---|
| 32px uses `Icon=` prefix; all others use `Type=` | Medium | Standardize to `Icon=` across all sizes |
| Filled icon set has only 3 icons | Medium | Expand filled set or document when to use |
| `coulmn-view` — misspelling (should be `column-view`) | Low | Rename to `column-view` |
| `title-bellow-table` — misspelling (should be `below`) | Low | Rename to `title-below-table` |
| `top filter` — uses space, others use hyphens | Low | Rename to `top-filter` |
| `sidebar left` / `sidebar right` — spaces in name | Low | Rename to `sidebar-left`, `sidebar-right` |
| `Undo` / `Redo` — capitalized, inconsistent | Low | Rename to `undo`, `redo` |
| `hexagon-variant` exists only in 16px, not 32/24 | Low | Add to all sizes or remove |
| Social icons (`facebook`, `twitter`, etc.) lack product relevance context | Low | Document when to use |
| No dark/light mode icon variants defined | Medium | Define icon color usage for dark mode |
