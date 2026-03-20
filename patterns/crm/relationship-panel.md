# Relationship Panel

**Used in:** Entity sidebars, showing related contacts, companies, deals.

**Structure:**
```
[Panel section]
  ├── Section header (label + "Add" button)
  └── [Related entity list]
        └── [Entity row]
              ├── Avatar
              ├── Entity name (link)
              ├── Role/type label
              └── Remove action
```

**Token dependencies:**
- Section header: `clr-neutral/40`, Medium
- Add button: `clr-royal/50`
- Entity name: link style (`clr-royal/50`, underline on hover)
- Role label: `clr-neutral/55`

---
