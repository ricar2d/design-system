# Badges

**Purpose:** Compact indicators of category, status, type, or count. Used throughout tables, cards, and lists.

**Anatomy:**
- Container (pill shape)
- Label text
- Optional leading icon or dot

**Variants (inferred from library description: "Indicators of categories"):**
- Semantic: Default, Primary (blue), Success (green?), Warning (gold), Error (red)
- Size: SM, MD
- Style: Filled, Outlined, Dot-only

**States:**
- Default
- Interactive (clickable filter tag)

**Token dependencies:**
- `clr-royal/50` — primary badge
- `clr-wine/50` — error/destructive badge
- `clr-gold/60` — warning badge
- `clr-neutral/55` — neutral/default badge
- `global/white` — text on colored badge
- `radius-full` — pill shape

**Usage guidelines:**
- Use badges for static category labels
- Use tags/chips (interactive version) for filterable UI
- Keep badge text short (1–3 words max)

---
