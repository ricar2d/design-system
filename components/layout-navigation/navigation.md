# Navigation

**Purpose:** Primary application navigation — top bar, side nav, breadcrumbs, tabs.

**Anatomy:**

### Top / App Bar
- Logo/brand mark
- Global search
- Module/feature navigation (links)
- User avatar + profile menu
- Notification bell
- Help/support link

### Sidebar navigation
- Module list items
  - Icon + label
  - Active indicator
  - Badge (for counts)
- Collapsible sections
- User profile footer

### Breadcrumbs
- Path items (links)
- Separator (`/` or `>`)
- Current page (non-link)

### Tabs
- Tab items (label, optional icon)
- Active indicator (underline or filled)
- Overflow handling

**States:**
- Nav item default
- Nav item hover
- Nav item active/current
- Nav item with badge

**Token dependencies:**
- `clr-royal/50` — active nav item, active tab indicator
- `clr-neutral/40` — nav labels
- `clr-neutral/55` — inactive nav icons
- `global/white` — nav bar surface
- `shadow-mid` — top bar/sidebar shadow

> ⚠️ **Note:** The library description for "Navigations" has a typo ("Navigaition") and the subtitle was empty in the index — this component may need more documentation.

---
