# Filters

**Purpose:** Filter bar and filter components for narrowing table/list results.

**Anatomy:**
- Filter bar container
- Filter chips (active filters)
  - Filter label (field: value)
  - Remove button
- Add filter button
- Filter dropdown/popover
  - Field selector
  - Operator selector (is, is not, contains, etc.)
  - Value input
  - Apply / Cancel

**Variants:**
- Inline filter bar (above tables)
- Side panel filters (for browse views)
- Quick filter (icon-only toggles)

**States:**
- No filters active
- 1+ filters active (chips shown)
- Filter popover open
- Filter being configured

**Token dependencies:**
- `clr-royal/50` — active filter chip background, add filter CTA
- `clr-neutral/55` — inactive filter states
- `global/white` — chip background (inferred)
- `Icon=filter` — filter icon
- `Icon=x` — remove filter chip

---
