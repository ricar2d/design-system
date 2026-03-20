# Cards

**Purpose:** Container component for grouping related content — the fundamental layout unit of the product.

**Anatomy:**
- White surface (`global/white`)
- Shadow (`shadow-card`)
- Border radius (`radius-lg` — 39px on canvas, scaled)
- Header area (optional)
- Content area
- Footer/actions area (optional)

**Variants (inferred from "all the basic and complex cards"):**
- Basic card: White surface with shadow
- Complex card: With header, media area, or nested components
- Option card: Used in library indices — image + label + link
- Data card: For metric/KPI display
- Contact card: CRM-specific person/company card
- Activity card: Timeline event

**States:**
- Default
- Hover (shadow elevation increase — inferred)
- Selected/Active
- Loading (skeleton state)

**Token dependencies:**
- `global/white` — card background
- `shadow-card` — elevation
- `radius-lg` — corner radius
- `clr-surface-inner` — inner sections (`#f9f9f9`)
- `clr-neutral/40` — card title
- `clr-neutral/55` — card subtitle/meta

**Usage guidelines:**
- Cards should always have adequate internal padding
- Use shadow-card for floating cards; no shadow for inline embedded cards
- Avoid nesting cards deeper than 2 levels

---
