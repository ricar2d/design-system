# Search with Entity Results

**Used in:** Global search, record lookup, mention autocomplete.

**Structure:**
```
[Search input: Search with Shortcuts component]
  └── [Results panel]
        ├── [Section: People]
        │     └── Entity rows (avatar + name + company)
        ├── [Section: Companies]
        │     └── Entity rows (logo + name + type)
        ├── [Section: Deals]
        │     └── Entity rows (name + stage + value)
        └── [Section: Recent]
              └── Previously viewed items
```

**Token dependencies:**
- Section headers: `clr-neutral/55`, small, Medium weight
- Entity names: `clr-neutral/40`
- Match highlight: `clr-royal/50`
- Keyboard shortcut hint: `clr-neutral/55`

---
