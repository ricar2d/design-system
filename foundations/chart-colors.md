# Chart Colors

Chart colors are purpose-built palettes for data visualizations — bar charts, line charts, pie charts, scatter plots, and any other quantitative display. They are organized into four named subsets, each designed for different visualization contexts.

**Source:** `chart_Colors.json` — Figma variable collection "Chart Colors"

---

## Four Palettes

| Palette | Count | Best for |
|---|---|---|
| `default` | 24 colors | General-purpose — use when in doubt |
| `contrast` | 13 colors | High-contrast needs, accessibility-critical charts |
| `cold` | 6 colors | Blue/teal/purple data series |
| `warm` | 9 colors | Yellow/orange/red/pink data series |
| `organic` | 8 colors | Green/natural data series |

---

## Default Palette (24 colors)

The broadest palette — covers the widest range of data categories. Cycles through blues, greens, golds, reds, purples, and pinks.

| Index | Hex | Primitive source |
|---|---|---|
| `default/1` | `#3392F0` | `clr-royal/60` |
| `default/2` | `#68B1FB` | `clr-royal/70` |
| `default/3` | `#0898CC` | `clr-sky/50` |
| `default/4` | `#5ECAEB` | `clr-sky/70` |
| `default/5` | `#00A385` | `clr-mint/50` |
| `default/6` | `#46A452` | `clr-pea/60` |
| `default/7` | `#5FD9C0` | `clr-mint/70` |
| `default/8` | `#ABE3AD` | `clr-pea/80` |
| `default/9` | `#8EB846` | `clr-ivy/60` |
| `default/10` | `#CBE899` | `clr-ivy/80` |
| `default/11` | `#FDBE3F` | `clr-gold/60` |
| `default/12` | `#FFD480` | `clr-gold/70` |
| `default/13` | `#F09A42` | `clr-sun/60` |
| `default/14` | `#FACC9E` | `clr-sun/80` |
| `default/15` | `#ED5E5E` | `clr-wine/60` |
| `default/16` | `#FBB6B6` | `clr-wine/80` |
| `default/17` | `#FFB2CF` | `crl-ruby/80` |
| `default/18` | `#FA5F90` | `crl-ruby/60` |
| `default/19` | `#C75ECC` | `clr-plum/60` |
| `default/20` | `#F1B0F5` | `clr-plum/80` |
| `default/21` | `#875FED` | `clr-iris/60` |
| `default/22` | `#C0ABF5` | `clr-iris/80` |
| `default/23` | `#00A385` | `clr-mint/50` |
| `default/24` | `#5FD9C0` | `clr-mint/70` |

---

## Contrast Palette (13 colors)

Higher visual separation between series. Good for presentations, printed output, or when series must be distinguishable without relying on subtle tonal differences.

| Index | Hex | Primitive source |
|---|---|---|
| `contrast/1` | `#46A452` | `clr-pea/60` |
| `contrast/2` | `#FDBE3F` | `clr-gold/60` |
| `contrast/3` | `#3392F0` | `clr-royal/60` |
| `contrast/4` | `#8EB846` | `clr-ivy/60` |
| `contrast/5` | `#875FED` | `clr-iris/60` |
| `contrast/6` | `#ED5E5E` | `clr-wine/60` |
| `contrast/7` | `#F09A42` | `clr-sun/60` |
| `contrast/9` | `#00A385` | `clr-mint/50` |
| `contrast/10` | `#2DB7E0` | `clr-sky/60` |
| `contrast/11` | `#C75ECC` | `clr-plum/60` |
| `contrast/12` | `#DE2C64` | `crl-ruby/50 (base)` |
| `contrast/13` | `#8EB846` | `clr-ivy/60` |

---

## Cold Palette (6 colors)

Blues, teals, and purples. For data with a cool or water-adjacent theme, or when you want a unified cool-hued visualization.

| Index | Hex | Primitive source |
|---|---|---|
| `cold/1` | `#68B1FB` | `clr-royal/70` |
| `cold/2` | `#3392F0` | `clr-royal/60` |
| `cold/3` | `#C0ABF5` | `clr-iris/80` |
| `cold/4` | `#875FED` | `clr-iris/60` |
| `cold/5` | `#5ECAEB` | `clr-sky/70` |
| `cold/6` | `#0898CC` | `clr-sky/50` |

---

## Warm Palette (9 colors)

Yellows, oranges, reds, and pinks. For data with warmth, urgency, or energy — also good for time-based or heat-map style visuals.

| Index | Hex | Primitive source |
|---|---|---|
| `warm/1` | `#FDBE3F` | `clr-gold/60` |
| `warm/2` | `#FFD480` | `clr-gold/70` |
| `warm/3` | `#F09A42` | `clr-sun/60` |
| `warm/4` | `#FACC9E` | `clr-sun/80` |
| `warm/5` | `#ED5E5E` | `clr-wine/60` |
| `warm/6` | `#FBB6B6` | `clr-wine/80` |
| `warm/7` | `#FFB2CF` | `crl-ruby/80` |
| `warm/8` | `#FA5F90` | `crl-ruby/60` |
| `warm/9` | `#CBE899` | `clr-ivy/80` |

---

## Organic Palette (8 colors)

Greens and natural tones. For nature-themed data, sustainability metrics, or botanical/agricultural contexts.

| Index | Hex | Primitive source |
|---|---|---|
| `organic/1` | `#46A452` | `clr-pea/60` |
| `organic/2` | `#ABE3AD` | `clr-pea/80` |
| `organic/3` | `#8EB846` | `clr-ivy/60` |
| `organic/4` | `#CBE899` | `clr-ivy/80` |
| `organic/5` | `#F09A42` | `clr-sun/60` |
| `organic/6` | `#FACC9E` | `clr-sun/80` |
| `organic/7` | `#00A385` | `clr-mint/50` |
| `organic/8` | `#5FD9C0` | `clr-mint/70` |

---

## Usage Guidelines

- Always pick the **smallest palette** that covers your data categories — fewer colors read more clearly.
- For 1–3 data series, use `cold`, `warm`, or `organic` for thematic coherence.
- For 4–8 series, use `contrast`.
- For 9+ series, use `default`.
- Pair adjacent light/dark steps (e.g. `default/1` + `default/2`) for related but distinguishable sub-series.
- Never use chart colors for UI status states — use [semantic tokens](/foundations/semantic-colors) for those.
