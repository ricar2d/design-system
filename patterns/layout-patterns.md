# Patterns — Layout Patterns

**Source:** Inferred from Pattern Library structure and component catalog

---

## Overview

Layout patterns describe how components are assembled into repeating page structures. These are not individual components — they are compositions that appear consistently across the OneHQ product.

---

## Pattern 1: Card Grid Index

**Used in:** Pattern Library index pages, component catalog views, dashboard overviews.

**Structure:**
```
[Page background: #f3f3f3]
  └── [Page header: white card, full-width]
        ├── Section title (IBM Plex Sans Medium, large)
        └── Section subtitle (IBM Plex Sans Regular, smaller)
  └── [Content grid: flex-wrap, gap 184px, padding 180px]
        └── [Option Card] × N
              ├── Image/preview area (fixed height ~489px canvas)
              └── Description area (#f9f9f9, padding 48px 76px)
                    ├── Link title (blue, Medium, underlined)
                    └── Subtitle (grey, Regular)
```

**Tokens:**
- Background: `clr-surface-page` (`#f3f3f3`)
- Header shadow: `shadow-mid`
- Card radius: `radius-lg` (39px)
- Card shadow: `shadow-card`
- Card inner bg: `clr-surface-inner` (`#f9f9f9`)

---

## Pattern 2: Master-Detail Layout

**Used in:** Contact view, Company view, Deal view, most CRM entity screens.

**Structure:**
```
[App shell: full height]
  ├── [Left: Resource Browser / Navigation sidebar]
  │     └── Entity list with search
  └── [Right: Main content area]
        ├── [Entity header: avatar, name, actions]
        ├── [Tab bar: Overview, Activity, Notes, Files...]
        └── [Tab content area]
              ├── [Detail panels: key fields]
              ├── [Activity feed]
              └── [Related entities list]
  └── [Far right: Dialog panel (slide-in)]
        └── Conversation / Work thread
```

**Token dependencies:**
- Nav sidebar background: `global/white`
- Main content background: `clr-surface-page`
- Dialog background: `global/white`
- Panel shadows: `shadow-mid`

---

## Pattern 3: Data Table Page

**Used in:** All entity list views (Contacts, Companies, Deals, Tasks).

**Structure:**
```
[Page container]
  ├── [Page header]
  │     ├── Title + entity count
  │     └── Actions (New, Import, Export)
  ├── [Filter bar]
  │     ├── Search input
  │     ├── Active filter chips
  │     └── Add filter + Saved views
  ├── [Table]
  │     ├── Column headers (sortable)
  │     ├── Data rows (with hover actions)
  │     └── Bulk selection bar (on select)
  └── [Pagination / load more]
```

**Key patterns:**
- Columns are resizable (via `sidebar left/right` / `columns` icon)
- Rows show kebab menu on hover
- Bulk actions bar appears above table when rows are selected
- Column header includes sort arrows and filter indicator

---

## Pattern 4: Form / Modal Layout

**Used in:** Create entity modal, edit forms, settings.

**Structure:**
```
[Modal overlay]
  └── [Modal container]
        ├── [Header: Title + close icon]
        ├── [Body: scrollable]
        │     ├── Form section title + divider
        │     ├── Form rows (label + input)
        │     │     ├── Single column (simple forms)
        │     │     └── Two column (dense forms)
        │     └── Form section 2...
        └── [Footer: Cancel + Primary action]
```

**Token dependencies:**
- Modal background: `global/white`
- Shadow: `shadow-mid`
- Radius: `radius-lg`
- Section dividers: `clr-neutral/55` at low opacity
- Primary button: `clr-royal/50`

---

## Pattern 5: Filter + Results Pattern

**Used in:** Search results, Browse views, Calendar filtering, Pipeline views.

**Structure:**
```
[Layout container]
  ├── [Top filter bar OR Left panel filters]
  │     ├── Quick filter toggles (icon buttons)
  │     ├── Filter chips (active filters)
  │     └── Advanced filter popover
  └── [Results area]
        ├── Results count + sort controls
        └── Card grid OR List OR Table
```

**Variants:**
- Top filter bar (for tables and grids)
- Left panel filters (for browse views like Resource Browser)
- Inline column filters (within table header)

---

## Pattern 6: Empty + Onboarding States

**Used in:** First-time user experience, empty sections.

**Structure:**
```
[Centered content area]
  ├── Illustration or large icon
  ├── Title (primary empty state message)
  ├── Description (explain what goes here)
  └── CTA Button (primary action to fill it)
```

**Token dependencies:**
- Title: `clr-neutral/40`
- Description: `clr-neutral/55`
- CTA: `clr-royal/50`
- Background: `clr-surface-page`

---

## Pattern 7: Settings Layout

**Used in:** User settings, account settings, workspace configuration.

**Structure:**
```
[Full-height layout]
  ├── [Left: Settings navigation]
  │     └── Grouped nav links (Profile, Notifications, Integrations...)
  └── [Right: Settings content]
        ├── Section heading + description
        ├── Setting rows (label + control)
        └── Save actions
```

**Token dependencies:**
- Nav: `global/white` background
- Content: `clr-surface-page` or `global/white`
- Controls: Toggles, selects, inputs from Inputs & Controls library

---

## Responsive Behavior (Inferred)

> ⚠️ **Inferred pattern:** No responsive breakpoints are defined in the libraries. The following is inferred from component structure.

| Breakpoint | Layout behavior |
|---|---|
| Desktop wide (1440+) | Full master-detail with sidebar + dialog panel |
| Desktop (1024–1440) | Sidebar collapsible, dialog panel as modal |
| Tablet (768–1024) | Sidebar as slide-in drawer, no dialog panel |
| Mobile (< 768) | Single column, all panels as full-screen sheets |
