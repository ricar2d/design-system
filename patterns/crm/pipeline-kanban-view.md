# Pipeline / Kanban View

**Used in:** Deals pipeline, Sales stages, Task boards.

**Structure:**
```
[Board container: horizontal scroll]
  └── [Pipeline column] × N
        ├── [Column header]
        │     ├── Stage name
        │     ├── Count badge
        │     └── Column value (sum, for deals)
        ├── [Deal/Task cards stack]
        │     └── [Card]
        │           ├── Entity name
        │           ├── Value / progress
        │           ├── Owner avatar
        │           └── Due date / stage badge
        └── [Add card button]
```

**Token dependencies:**
- Column header: `clr-neutral/40`, Medium
- Card: `global/white`, `shadow-card`, `radius-lg`
- Stage badge: semantic colors per stage
- Value text: `clr-neutral/40`
- Add button: `clr-royal/50`

---
