# Kebab

**Purpose:** Three-dot overflow menu (`⋮`) for contextual actions on rows, cards, or items.

**Anatomy:**
- Icon trigger (`Icon=more-vertical`)
- Dropdown action list
  - Action item (icon + label)
  - Destructive action item (red)
  - Divider

**States:**
- Default (icon only, often hidden until hover)
- Hover (icon visible)
- Open (dropdown visible)
- Action hover

**Token dependencies:**
- `clr-neutral/55` — icon color
- `clr-wine/50` — destructive action
- `global/white` — dropdown background
- `shadow-card` — dropdown elevation

**Usage guidelines:**
- Use for row-level actions in tables and lists
- Keep to 3–7 items maximum
- Place destructive actions last, separated by a divider

---
