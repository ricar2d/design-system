# Card Grid Index

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
