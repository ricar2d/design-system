# Input (Line)

**Purpose:** Minimalist borderless input — uses a bottom border only. Used for inline editing or compact forms.

**Anatomy:**
- Label (optional)
- Text field with bottom border only
- No container box

**States:**
- Empty
- Focused (line color transitions to `clr-royal/50`)
- Filled
- Error
- Disabled

**Token dependencies:**
- `clr-royal/50` — active line
- `clr-wine/50` — error line
- `clr-neutral/55` — default line
- `clr-neutral/40` — text

**Usage guidelines:**
- Use for inline editing contexts (table cells, card fields)
- Do not use in standalone form layouts — use Input Basic instead

---
