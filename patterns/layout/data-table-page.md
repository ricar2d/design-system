# Data Table Page

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
