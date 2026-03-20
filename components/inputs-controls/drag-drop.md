# Drag & Drop

**Purpose:** Drag handles and drop zones for reordering items or uploading files via drag.

**Anatomy (reorder):**
- Drag handle icon (`Icon=grabber`)
- Draggable item container
- Drop zone (highlighted on hover)
- Drop indicator line

**Anatomy (file drop):**
- Drop zone container
- Upload icon
- Label + subtext
- File type/size hint

**States:**
- Default
- Drag over (highlighted drop zone)
- Dragging item
- Dropped/complete

**Token dependencies:**
- `clr-royal/50` — drop zone highlight, drop indicator
- `clr-neutral/55` — drag handle icon
- `Icon=grabber` — drag handle

---
