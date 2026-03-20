# Primitive Colors

Primitive colors are the raw, named color values that form the foundation of the entire design system. Every semantic token, component color, and chart color is an alias pointing to one of these primitives.

**Source:** `Primitive_colors.json` — Figma variable collection "Primitive Colors"

---

## How the scale works

Each color family is numbered on a scale from **10 (darkest)** to **95–98 (lightest)**. The base step — the "truest" version of that hue — is labeled `(base)` and varies per family depending on where the hue reads most purely. Lower numbers are rich and dark (suitable for text and deep backgrounds); higher numbers are pale and airy (suitable for tinted surfaces and hover states).

```
10 ──────── darkest / richest
      ...
   base ←── truest expression of the hue
      ...
95 ──────── lightest / most tinted
```

---

## Global

| Token | Hex | Usage |
|---|---|---|
| `global/white` | `#FFFFFF` | All white surfaces, card backgrounds, modals |
| `global/black` | `#000000` | Pure black — use sparingly |

---

## Royal — Primary / Brand Blue

The primary interactive color. Used for buttons, links, active states, focus indicators, and brand elements.

| Step | Hex | Notes |
|---|---|---|
| `clr-royal/10` | `#000919` | Near-black blue |
| `clr-royal/15` | `#001433` | |
| `clr-royal/20` | `#001F4C` | |
| `clr-royal/25` | `#002A66` | |
| `clr-royal/30` | `#003780` | |
| `clr-royal/35` | `#004599` | |
| `clr-royal/40` | `#0053B2` | Hover state for primary buttons |
| `clr-royal/45` | `#0063CC` | |
| `clr-royal/50 (base)` | `#0073E5` | **Primary interactive — CTA, links, active** |
| `clr-royal/55` | `#1C84EB` | |
| `clr-royal/60` | `#3392F0` | Chart color 1 |
| `clr-royal/65` | `#4CA0F5` | |
| `clr-royal/70` | `#68B1FB` | Chart color 2 |
| `clr-royal/75` | `#80BFFF` | |
| `clr-royal/80` | `#9CCEFF` | |
| `clr-royal/85` | `#B6DBFF` | |
| `clr-royal/90` | `#D2E9FF` | |
| `clr-royal/95` | `#EBF6FF` | Lightest tint — selected row backgrounds |

---

## Neutral — Text / UI Structure

The workhorse family. Used for all text, borders, dividers, surface backgrounds, and disabled states.

| Step | Hex | Notes |
|---|---|---|
| `clr-neutral/10` | `#050C19` | Near-black navy |
| `clr-neutral/15` | `#0A1326` | |
| `clr-neutral/20` | `#0F1B33` | |
| `clr-neutral/25` | `#172540` | |
| `clr-neutral/30` | `#1F2E4C` | |
| `clr-neutral/35` | `#273859` | |
| `clr-neutral/40` | `#334466` | **Primary text — headings, labels** |
| `clr-neutral/45` | `#3F5173` | |
| `clr-neutral/50 (base)` | `#4E6185` | |
| `clr-neutral/55` | `#627494` | **Secondary text — descriptions, captions** |
| `clr-neutral/60` | `#7486A6` | |
| `clr-neutral/65` | `#8497B8` | Disabled text + surfaces |
| `clr-neutral/70` | `#97AAC7` | Focus ring |
| `clr-neutral/75` | `#AEBED6` | |
| `clr-neutral/80` | `#C5D2E5` | |
| `clr-neutral/85` | `#D3DCED` | |
| `clr-neutral/90` | `#E1E8F5` | Elevated surface |
| `clr-neutral/95` | `#F2F6FC` | **Default surface / page background** |
| `clr-neutral/98` | `#F9FBFE` | **Subtle surface — card inner areas** |

---

## Wine — Destructive / Error

Used for error states, destructive actions, delete confirmations.

| Step | Hex | Notes |
|---|---|---|
| `clr-wine/10` | `#570000` | |
| `clr-wine/20` | `#7A0000` | |
| `clr-wine/30` | `#9B0808` | |
| `clr-wine/40` | `#BC1515` | |
| `clr-wine/50 (base)` | `#DC3838` | **Error, destructive actions** |
| `clr-wine/60` | `#ED5E5E` | Chart color 15 |
| `clr-wine/70` | `#F48B8B` | |
| `clr-wine/80` | `#FBB6B6` | Chart color 16 |
| `clr-wine/90` | `#FDD8D8` | |
| `clr-wine/95` | `#FDEEEE` | Error background |

---

## Gold — Warning / Highlight

Used for warning states, badges, star ratings, and attention highlights. Note: the base is at /20, not /50.

| Step | Hex | Notes |
|---|---|---|
| `clr-gold/10` | `#664100` | |
| `clr-gold/20 (base)` | `#8F5A00` | **Warning text — semantic `status/warning`** |
| `clr-gold/30` | `#B27100` | |
| `clr-gold/40` | `#DB8F00` | |
| `clr-gold/50` | `#F4AB19` | |
| `clr-gold/60` | `#FDBE3F` | **Warning fill — badges, highlights** |
| `clr-gold/70` | `#FFD480` | |
| `clr-gold/80` | `#FFE1A6` | |
| `clr-gold/90` | `#FFEECC` | |
| `clr-gold/95` | `#FFF8EB` | Warning background |

---

## Pea — Success / Positive

Used for success states, task completion, positive indicators.

| Step | Hex | Notes |
|---|---|---|
| `clr-pea/10` | `#003304` | |
| `clr-pea/20` | `#0A430F` | |
| `clr-pea/30` | `#165A22` | |
| `clr-pea/40` | `#246B2D` | **Success text — semantic `status/success`** |
| `clr-pea/50 (base)` | `#31873C` | |
| `clr-pea/60` | `#46A452` | Chart colors |
| `clr-pea/70` | `#75C778` | |
| `clr-pea/80` | `#ABE3AD` | Chart colors |
| `clr-pea/90` | `#D8F7D7` | |
| `clr-pea/95` | `#EEFCED` | Success background |

---

## Sky — Info / Informational Blue

A cooler, cyan-leaning blue. Used for info states and chart data series.

| Step | Hex | Notes |
|---|---|---|
| `clr-sky/10` | `#00334D` | |
| `clr-sky/20` | `#004766` | |
| `clr-sky/30` | `#005B80` | Info strong |
| `clr-sky/40 (base)` | `#007BA8` | **Info — semantic `status/info`** |
| `clr-sky/50` | `#0898CC` | Chart color 3 |
| `clr-sky/60` | `#2DB7E0` | |
| `clr-sky/70` | `#5ECAEB` | Chart color 4 |
| `clr-sky/80` | `#93DEF5` | |
| `clr-sky/90` | `#C8EEFA` | |
| `clr-sky/95` | `#EBF8FC` | |

---

## Mint — Teal / Aqua Green

A teal-green. Used for chart data series and accent colors.

| Step | Hex | Notes |
|---|---|---|
| `clr-mint/10` | `#00332A` | |
| `clr-mint/20` | `#0C4D40` | |
| `clr-mint/30` | `#006B59` | |
| `clr-mint/40 (base)` | `#00856E` | |
| `clr-mint/50` | `#00A385` | Chart color 5, 23 |
| `clr-mint/60` | `#20C5A4` | |
| `clr-mint/70` | `#5FD9C0` | Chart color 7, 24 |
| `clr-mint/80` | `#8EE5D4` | |
| `clr-mint/90` | `#C2F2E9` | |
| `clr-mint/95` | `#E6FAF6` | |

---

## Ivy — Olive / Warm Green

A yellow-toned green. Used for chart data series.

| Step | Hex | Notes |
|---|---|---|
| `clr-ivy/10` | `#263803` | |
| `clr-ivy/20` | `#344D04` | |
| `clr-ivy/30` | `#486608` | |
| `clr-ivy/40 (base)` | `#5D820D` | |
| `clr-ivy/50` | `#759E28` | |
| `clr-ivy/60` | `#8EB846` | Chart color 9, 13 |
| `clr-ivy/70` | `#ABD169` | |
| `clr-ivy/80` | `#CBE899` | Chart color 10 |
| `clr-ivy/90` | `#E7F5D0` | |
| `clr-ivy/95` | `#F4FAEB` | |

---

## Sun — Amber / Warm Orange

A warm amber. Used for chart data series.

| Step | Hex | Notes |
|---|---|---|
| `clr-sun/10` | `#663000` | |
| `clr-sun/20` | `#8D4301` | |
| `clr-sun/30 (base)` | `#B15401` | |
| `clr-sun/40` | `#D96908` | |
| `clr-sun/50` | `#E58019` | |
| `clr-sun/60` | `#F09A42` | Chart color 13 |
| `clr-sun/70` | `#F6B36F` | |
| `clr-sun/80` | `#FACC9E` | Chart color 14 |
| `clr-sun/90` | `#FEE6CD` | |
| `clr-sun/95` | `#FEF4EA` | |

---

## Iris — Blue-Violet / Purple

A blue-leaning violet. Used for chart data series.

| Step | Hex | Notes |
|---|---|---|
| `clr-iris/10` | `#0F0133` | |
| `clr-iris/20` | `#331F66` | |
| `clr-iris/30` | `#44278C` | |
| `clr-iris/40` | `#5B34BF` | |
| `clr-iris/50 (base)` | `#6F43DE` | |
| `clr-iris/60` | `#875FED` | Chart color 21 |
| `clr-iris/70` | `#A180F2` | |
| `clr-iris/80` | `#C0ABF5` | Chart color 22 |
| `clr-iris/90` | `#E4DCFA` | |
| `clr-iris/95` | `#F5F2FC` | |

---

## Plum — Red-Violet / Magenta

A red-leaning violet. Used for chart data series.

| Step | Hex | Notes |
|---|---|---|
| `clr-plum/10` | `#3C0B3D` | |
| `clr-plum/20` | `#591C5C` | |
| `clr-plum/30` | `#762B7A` | |
| `clr-plum/40` | `#8F3494` | |
| `clr-plum/50 (base)` | `#A83DAD` | |
| `clr-plum/60` | `#C75ECC` | Chart color 19 |
| `clr-plum/70` | `#D784DB` | |
| `clr-plum/80` | `#F1B0F5` | Chart color 20 |
| `clr-plum/90` | `#F8D4FA` | |
| `clr-plum/95` | `#FCF2FC` | |

---

## Ruby — Hot Pink / Cerise

A warm pink-red. Used for chart data series. Note: named `crl-ruby` (with typo) in source.

| Step | Hex | Notes |
|---|---|---|
| `crl-ruby/10` | `#5E0228` | |
| `crl-ruby/20` | `#800035` | |
| `crl-ruby/30` | `#9E003F` | |
| `crl-ruby/40` | `#C40A4E` | |
| `crl-ruby/50 (base)` | `#DE2C64` | Chart color 12 |
| `crl-ruby/60` | `#FA5F90` | Chart color 18 |
| `crl-ruby/70` | `#FF8CB3` | |
| `crl-ruby/80` | `#FFB2CF` | Chart color 17 |
| `crl-ruby/90` | `#FFD9E9` | |
| `crl-ruby/95` | `#FFF2F8` | |

> ⚠️ **Naming typo:** `crl-ruby` should be `clr-ruby`. The `crl` prefix is inconsistent with all other families. Fix in source.
