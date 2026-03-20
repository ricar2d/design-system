# Master-Detail Layout

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
