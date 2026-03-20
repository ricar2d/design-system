# Carousel

**Purpose:** Horizontal content slider for browsing multiple cards, media items, or featured content in sequence.

**Anatomy:**
- Track (overflow-hidden container)
- Slides (equally-sized content panels)
- Navigation arrows (left / right)
- Dot indicators (optional pagination)
- Drag/swipe support

**Variants:**
- Single item (full-width)
- Multi-item (shows partial next/prev)
- Auto-advancing
- Manual only

**States:**
- Default (resting)
- Transitioning
- First slide (left arrow disabled)
- Last slide (right arrow disabled)

**Token dependencies:**
- `clr-royal/50` — active dot indicator, navigation arrow hover
- `clr-neutral/55` — inactive dot indicators
- `Icon=chevron-left`, `Icon=chevron-right` — navigation
- `shadow-card` — slide card elevation

---
