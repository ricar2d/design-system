# Form / Modal Layout

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
