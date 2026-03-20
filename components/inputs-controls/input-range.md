# Input (Range)

**Purpose:** Numeric range input with dual handles — for filtering by minimum/maximum values.

**Anatomy:**
- Track (background bar)
- Fill (between handles)
- Handle x2 (draggable thumbs)
- Min/max labels
- Value tooltips (on drag)

**States:**
- Default
- Active handle (dragging)
- Focused handle
- Disabled

**Token dependencies:**
- `clr-royal/50` — track fill, active handle
- `clr-neutral/55` — track background
- `global/white` — handle surface

---
