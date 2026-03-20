# Settings Layout

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
