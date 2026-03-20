# Bulk Action Bar

**Used in:** Data tables and lists when one or more rows are selected.

**Structure:**
```
[Bulk action bar: appears above table on selection]
  ├── Selection count ("3 selected")
  ├── Primary bulk actions (Assign, Tag, Export)
  ├── Destructive action (Delete)
  └── Deselect / close button
```

**Token dependencies:**
- Bar background: `clr-royal/50` or `clr-neutral/40` (inferred)
- Bar text: `global/white`
- Destructive action: `clr-wine/50`
