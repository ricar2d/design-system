# Design Tokens

**Source:** Variable definitions extracted from all three Figma libraries.  
**Status legend:**  ✅ Found in library  ⚠️ Inferred pattern  ❌ Missing / recommended addition

---

## Color Tokens

### Confirmed (found in library)

| Token name | Raw Figma name | Hex value | Libraries |
|---|---|---|---|
| `--clr-royal-50` | `clr-royal/50 (base)` | `#0073e5` | Pattern, Inputs, Icons |
| `--clr-neutral-40` | `clr-neutral/40` | `#334466` | Pattern, Inputs |
| `--clr-neutral-55` | `clr-neutral/55` | `#627494` | Pattern, Inputs |
| `--clr-wine-50` | `clr-wine/50 (base)` | `#dc3838` | Icons |
| `--clr-gold-60` | `clrGold/60` | `#fdbe3f` | Icons |
| `--clr-white` | `global/white` | `#ffffff` | All |

### Duplicate / Inconsistent entries (same value, different name)

| Token A | Token B | Hex | Action |
|---|---|---|---|
| `clr-neutral/40` | `clrNeutral/40` (camelCase) | `#334466` | Standardize to `clr-neutral/40` |
| `clr-neutral/55` | `clrNeutral/55` (camelCase) | `#627494` | Standardize to `clr-neutral/55` |
| `clr-wine/50 (base)` | `Wine - clrWine/50 (base)` | `#dc3838` | Remove duplicate |
| `clr-neutral/40` | `legacy(Deprecated)/surface/neutral--dark` | `#334466` | Delete legacy |
| `clr-neutral/55` | `legacy(Deprecated)/surface/icon--base` | `#627494` | Delete legacy |

### Inferred surface colors (used but not tokenized)

| Recommended token | Hex | Found in |
|---|---|---|
| `--clr-surface-page` | `#f3f3f3` | Page/canvas backgrounds across all libraries |
| `--clr-surface-card-inner` | `#f9f9f9` | Card description areas in Pattern Library |

---

## Shadow Tokens

| Token name | Raw Figma name | Value |
|---|---|---|
| `--shadow-mid` | `Shadows/Mid` | `drop-shadow(0 0 18px rgba(14,67,140,0.07))` |
| `--shadow-card` | *(inferred)* | `drop-shadow(0 4px 23px rgba(22,88,197,0.06))` |

---

## Border Radius Tokens

| Token name | Value | Found in |
|---|---|---|
| `--radius-lg` | `39px` | All option cards |
| `--radius-xl` | `60px` | Page/canvas container frames |
| `--radius-2xl` | `80px` | Icon library component container |
| `--radius-sm` | *(inferred ~6–8px)* | Inputs, badges — needs verification |
| `--radius-md` | *(inferred ~12px)* | Dropdowns, tooltips — needs verification |

---

## Typography Tokens

| Token name | Value | Notes |
|---|---|---|
| `--font-family` | `'IBM Plex Sans', sans-serif` | ✅ Confirmed — only family used |
| `--font-weight-regular` | `400` | ✅ Used throughout |
| `--font-weight-medium` | `500` | ✅ Used for labels, CTAs, headings |
| `--font-weight-bold` | `700` | ⚠️ Inferred — present in icon set |

---

## Opacity Tokens (White overlays)

| Token name (inferred) | Value | Usage |
|---|---|---|
| `--overlay-90` | `rgba(255,255,255,0.9)` | Heavy image wash |
| `--overlay-80` | `rgba(255,255,255,0.8)` | Standard image wash |
| `--overlay-70` | `rgba(255,255,255,0.7)` | Light image wash |
| `--overlay-60` | `rgba(255,255,255,0.6)` | Subtle wash |

---

## Spacing Tokens (Inferred — not defined in libraries)

| Token name | Value |
|---|---|
| `--space-1` | `4px` |
| `--space-2` | `8px` |
| `--space-3` | `12px` |
| `--space-4` | `16px` |
| `--space-5` | `20px` |
| `--space-6` | `24px` |
| `--space-8` | `32px` |
| `--space-10` | `40px` |
| `--space-12` | `48px` |
| `--space-16` | `64px` |
| `--space-20` | `80px` |
| `--space-32` | `128px` |

---

## Motion Tokens (Missing — not defined in libraries)

❌ No motion or animation tokens exist in any library.

| Recommended token | Recommended value |
|---|---|
| `--duration-fast` | `100ms` |
| `--duration-default` | `200ms` |
| `--duration-slow` | `300ms` |
| `--easing-default` | `ease-in-out` |
| `--easing-enter` | `ease-out` |
| `--easing-exit` | `ease-in` |

---

## Full Token Reference (CSS)

```css
:root {
  /* ─── Colors ─────────────────────────────── */
  --clr-royal-50:          #0073e5;
  --clr-neutral-40:        #334466;
  --clr-neutral-55:        #627494;
  --clr-wine-50:           #dc3838;
  --clr-gold-60:           #fdbe3f;
  --clr-white:             #ffffff;
  --clr-surface-page:      #f3f3f3;  /* inferred */
  --clr-surface-inner:     #f9f9f9;  /* inferred */

  /* ─── Semantic color aliases ─────────────── */
  --color-text-primary:        var(--clr-neutral-40);
  --color-text-secondary:      var(--clr-neutral-55);
  --color-text-link:           var(--clr-royal-50);
  --color-text-error:          var(--clr-wine-50);
  --color-text-warning:        var(--clr-gold-60);
  --color-text-on-brand:       var(--clr-white);
  --color-bg-page:             var(--clr-surface-page);
  --color-bg-card:             var(--clr-white);
  --color-bg-card-inner:       var(--clr-surface-inner);
  --color-interactive:         var(--clr-royal-50);
  --color-destructive:         var(--clr-wine-50);
  --color-warning:             var(--clr-gold-60);

  /* ─── Shadows ────────────────────────────── */
  --shadow-mid:    0 0 18px rgba(14,67,140,0.07);
  --shadow-card:   0 4px 23px rgba(22,88,197,0.06);

  /* ─── Border radius ──────────────────────── */
  --radius-sm:     6px;    /* inferred */
  --radius-md:     12px;   /* inferred */
  --radius-lg:     39px;
  --radius-xl:     60px;
  --radius-2xl:    80px;

  /* ─── Typography ─────────────────────────── */
  --font-family:          'IBM Plex Sans', sans-serif;
  --font-weight-regular:  400;
  --font-weight-medium:   500;
  --font-weight-bold:     700;

  /* ─── Spacing ────────────────────────────── */
  --space-1:    4px;
  --space-2:    8px;
  --space-3:    12px;
  --space-4:    16px;
  --space-5:    20px;
  --space-6:    24px;
  --space-8:    32px;
  --space-10:   40px;
  --space-12:   48px;
  --space-16:   64px;
  --space-20:   80px;
  --space-32:   128px;

  /* ─── Overlays ───────────────────────────── */
  --overlay-90:  rgba(255,255,255,0.9);
  --overlay-80:  rgba(255,255,255,0.8);
  --overlay-70:  rgba(255,255,255,0.7);
  --overlay-60:  rgba(255,255,255,0.6);

  /* ─── Motion (recommended additions) ────── */
  --duration-fast:     100ms;
  --duration-default:  200ms;
  --duration-slow:     300ms;
  --easing-default:    ease-in-out;
}
```
