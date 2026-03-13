# Colors

**Source:** All three libraries share the same color token set.

---

## Token Naming Convention

The system uses a **`clr-[family]/[step]`** naming pattern with optional descriptors in parentheses.

```
clr-royal/50 (base)   →  primary blue
clr-neutral/40        →  dark navy text
clr-neutral/55        →  mid grey-blue text
clr-wine/50 (base)    →  destructive red
clr-gold/60           →  warning yellow
global/white          →  pure white
```

> ⚠️ **Inconsistency found:** The Pattern Library uses `clr-neutral/40` (with slash separator and space) while the Inputs & Controls Library uses `clrNeutral/40` (camelCase, no space). Both resolve to the same hex `#334466`. These are duplicate definitions with different naming formats that should be unified.

---

## Color Palette

### Royal — Primary / Interactive

| Token | Hex | Usage |
|---|---|---|
| `clr-royal/50 (base)` | `#0073e5` | CTA buttons, links, active states, brand |

> ⚠️ **Missing / recommended addition:** Only the base (50) step is explicitly defined. The full ramp (10–90) is inferred to exist from the `/50` naming convention but is not documented. Lighter tints (`/10`, `/20`) are likely used for hover backgrounds and focus rings. A full ramp should be extracted from component states.

---

### Neutral — Text / Surfaces

| Token | Hex | Usage |
|---|---|---|
| `clr-neutral/40` | `#334466` | Page titles, section headings, primary labels |
| `clr-neutral/55` | `#627494` | Descriptions, subtitles, placeholder text, captions |

> The neutral family doubles as both a text color and a legacy surface color (see deprecated tokens).

---

### Wine — Destructive / Error

| Token | Hex | Usage |
|---|---|---|
| `clr-wine/50 (base)` | `#dc3838` | Error states, delete actions, destructive indicators |

> ✅ Found in Icons Library variable defs under both `clr-wine/50 (base)` and `Wine - clrWine/50 (base)` — **duplicate entry, different format** (see audit).

---

### Gold — Warning / Highlight

| Token | Hex | Usage |
|---|---|---|
| `clr-gold/60` | `#fdbe3f` | Warning states, highlight badges, star/rating icons |

---

### Global / Surfaces

| Token | Hex | Usage |
|---|---|---|
| `global/white` | `#ffffff` | Card surfaces, component backgrounds |
| *(inferred)* `surface/page` | `#f3f3f3` | Page/canvas background |
| *(inferred)* `surface/card-inner` | `#f9f9f9` | Card description/label zones |

---

## Deprecated / Legacy Tokens

Found in the Icons Library — these are marked deprecated:

| Legacy Token | Hex | Modern Equivalent |
|---|---|---|
| `legacy(Deprecated)/surface/neutral--dark` | `#334466` | `clr-neutral/40` |
| `legacy(Deprecated)/surface/icon--base` | `#627494` | `clr-neutral/55` |

> ✅ These tokens have direct equivalents in the current system. They should be removed and all usages migrated to `clr-neutral/40` and `clr-neutral/55`.

---

## CSS Custom Properties (Recommended)

```css
:root {
  /* Royal */
  --clr-royal-50:       #0073e5;

  /* Neutral */
  --clr-neutral-40:     #334466;
  --clr-neutral-55:     #627494;

  /* Wine */
  --clr-wine-50:        #dc3838;

  /* Gold */
  --clr-gold-60:        #fdbe3f;

  /* Global surfaces */
  --clr-white:          #ffffff;
  --clr-surface-page:   #f3f3f3;
  --clr-surface-inner:  #f9f9f9;
}
```

---

## Semantic Color Mapping (Inferred)

| Semantic Role | Token |
|---|---|
| `color-text-primary` | `clr-neutral/40` — `#334466` |
| `color-text-secondary` | `clr-neutral/55` — `#627494` |
| `color-text-link` | `clr-royal/50` — `#0073e5` |
| `color-text-error` | `clr-wine/50` — `#dc3838` |
| `color-text-warning` | `clr-gold/60` — `#fdbe3f` |
| `color-text-on-primary` | `global/white` — `#ffffff` |
| `color-bg-surface` | *(inferred)* `#f3f3f3` |
| `color-bg-card` | `global/white` — `#ffffff` |
| `color-bg-card-inner` | *(inferred)* `#f9f9f9` |
| `color-interactive-default` | `clr-royal/50` — `#0073e5` |
| `color-interactive-destructive` | `clr-wine/50` — `#dc3838` |
| `color-interactive-warning` | `clr-gold/60` — `#fdbe3f` |

---

## Issues Summary

| Issue | Severity | Action |
|---|---|---|
| `clr-neutral/40` vs `clrNeutral/40` — same value, two formats | Medium | Standardize to `clr-neutral/40` |
| `Wine - clrWine/50 (base)` duplicate entry | Low | Remove duplicate |
| Only base steps defined (no ramps) | High | Extract full ramp from components |
| Legacy tokens not fully removed | Medium | Migrate and delete |
| `#f3f3f3` and `#f9f9f9` used but not tokenized | High | Add as surface tokens |
