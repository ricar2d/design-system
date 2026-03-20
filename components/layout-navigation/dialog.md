# Dialog

**Purpose:** Persistent contextual panel — the backdrop structure for conversations, work items, and detail panels in the CRM.

**Anatomy:**
- Dialog container (full-height panel)
- Header
  - Avatar / entity icon
  - Title (entity name)
  - Actions bar (close, expand, etc.)
- Body (scrollable content area)
  - Tabbed content sections
  - Activity feed
  - Related items
- Footer (optional — reply bar, action row)

**Variants:**
- Message dialog (conversation view)
- Work item dialog (task/project detail)
- Discussion dialog

**States:**
- Collapsed
- Expanded (partial width)
- Full-screen
- Loading

**Token dependencies:**
- `global/white` — dialog background
- `shadow-mid` — dialog left edge shadow
- `clr-royal/50` — active tab, link actions
- `clr-neutral/40` — dialog title

**Usage guidelines:**
- Dialog is the primary detail view — not a modal overlay
- Slides in from the right edge of the main content area
- Tab structure allows navigating between related data types

---
