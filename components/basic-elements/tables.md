# Tables

**Purpose:** Structured data display for records, reports, and CRM entity lists.

**Anatomy:**
- Table header row
  - Column label (Medium weight)
  - Sort indicator (icon)
  - Resize handle (optional)
- Table body rows
  - Cell content
  - Row actions (hover-reveal)
- Pagination / footer

**Variants:**
- Standard table
- Data grid (referenced as separate component — `Data Grid` node found)
- Compact/dense table
- Striped rows (inferred)
- Bordered cells (inferred)

**States (per row):**
- Default
- Hover
- Selected (checkbox or row click)
- Active/Expanded
- Loading (skeleton)

**Token dependencies:**
- `clr-neutral/40` — header labels
- `clr-neutral/55` — cell content
- `clr-royal/50` — sort active, selected row indicator
- `global/white` — row background
- `shadow-mid` — sticky header shadow (inferred)

---
