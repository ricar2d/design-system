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

## Full Icon Catalogue

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
