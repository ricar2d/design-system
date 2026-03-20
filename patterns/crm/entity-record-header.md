# Entity Record Header

**Used in:** Contact, Company, Deal, and Lead detail pages.

**Structure:**
```
[Record header bar]
  ├── [Entity avatar / logo]
  ├── [Entity name (large, primary text)]
  ├── [Entity type badge]
  ├── [Key attributes row]
  │     └── Email · Phone · Company · Status (inline icons + values)
  └── [Actions toolbar]
        ├── Primary CTA (e.g., "Send Email")
        ├── Secondary actions (Call, Task, Note)
        └── Kebab (more actions)
```

**Token dependencies:**
- Entity name: `clr-neutral/40`, Medium weight, large size
- Attributes: `clr-neutral/55`, Regular, small
- Primary CTA: `clr-royal/50`
- Avatar: `radius-full` (circle)

---
