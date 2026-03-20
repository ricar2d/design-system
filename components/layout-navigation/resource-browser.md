# Resource Browser

**Purpose:** Navigation panel for browsing entities (contacts, companies, deals) — a persistent or slide-in left sidebar explorer.

**Anatomy:**
- Panel container
- Search/filter bar (top)
- Entity list (scrollable)
  - Entity item (avatar + name + meta)
  - Selected state
  - Group headers
- Load more / pagination

**States:**
- Default
- Loading
- Empty (no results)
- Entity item hover
- Entity item selected

**Token dependencies:**
- `clr-royal/50` — selected item indicator, search active
- `clr-neutral/40` — entity name
- `clr-neutral/55` — entity meta
- `global/white` — panel background
- `shadow-mid` — panel shadow (when floating)

**Usage guidelines:**
- Persistent in wide-screen layouts
- Collapsible or slide-in on narrower viewports
- Maintains scroll position on navigation

---
