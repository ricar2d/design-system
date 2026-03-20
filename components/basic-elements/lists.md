# Lists

**Purpose:** Vertical sequences of items — the primary pattern for displaying entity records.

**Anatomy:**
- List container
- List item row
  - Leading element (avatar, icon, checkbox)
  - Primary label
  - Secondary label / metadata
  - Trailing element (action, badge, chevron)
- Divider between items (optional)

**Variants (inferred from "The list used everywhere"):**
- Simple list: Text only
- List with icon: Leading icon per item
- List with avatar: Person/entity lists
- List with actions: Trailing action buttons
- List with checkbox: Selectable/multi-select
- Grouped list: With section headers

**States (per item):**
- Default
- Hover
- Selected/Active
- Disabled

**Token dependencies:**
- `clr-neutral/40` — primary label
- `clr-neutral/55` — secondary label
- `clr-royal/50` — active/selected state
- `global/white` — item background
- `clr-surface-page` — hover background (inferred)

---
