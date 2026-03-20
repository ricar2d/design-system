# Multiple Switcher

**Purpose:** Segmented control / tab switcher for switching between 2–5 options within a context.

**Anatomy:**
- Container (pill or rounded rect)
- Option segments (equal width)
  - Active segment (filled)
  - Inactive segments (transparent)
  - Labels

**States:**
- Segment default
- Segment active
- Segment hover
- Disabled

**Token dependencies:**
- `clr-royal/50` — active segment fill
- `global/white` — active segment text
- `clr-neutral/55` — inactive text
- `radius-full` — container radius (pill style)

**Usage guidelines:**
- Use for 2–5 mutually exclusive options
- All options should be similar in length
- Do not use as primary navigation tabs

---
