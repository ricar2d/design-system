# Activity Feed / Timeline

**Used in:** Entity detail pages, Dialog panel, Work items.

**Structure:**
```
[Activity feed]
  ├── [Timeline axis (vertical line)]
  └── [Activity item] × N
        ├── [Activity icon (type indicator)]
        ├── [Author avatar]
        ├── [Activity content]
        │     ├── Author name + timestamp
        │     ├── Activity description / note text
        │     └── Attachments (optional)
        └── [Reaction / action bar (optional)]
```

**Activity types and icons:**
| Activity | Icon |
|---|---|
| Email | `Icon=mail` |
| Call | `Icon=phone` |
| Note | `Icon=edit-3` |
| Task | `Icon=check-square` |
| Meeting | `Icon=calendar` |
| File attached | `Icon=paperclip` |
| Status change | `Icon=activity` |
| Assignment | `Icon=user` |

**Token dependencies:**
- Timeline line: `clr-neutral/55` at low opacity
- Activity icon: `clr-royal/50` (for brand activities) or `clr-neutral/55`
- Timestamp: `clr-neutral/55`, small text
- Content text: `clr-neutral/40`

---
