# Controls

**Purpose:** Core binary/multi-state controls — checkbox, radio button, toggle switch.

### Checkbox

**Anatomy:**
- Check container (square, rounded)
- Checkmark icon
- Label text

**States:** Unchecked · Checked · Indeterminate · Focused · Disabled

**Token dependencies:**
- `clr-royal/50` — checked fill, indeterminate fill
- `clr-neutral/55` — unchecked border
- `global/white` — checkmark color
- `clr-neutral/40` — label

---

### Radio Button

**Anatomy:**
- Circle container
- Inner dot (selected)
- Label text

**States:** Unselected · Selected · Focused · Disabled

---

### Toggle / Switch

**Anatomy:**
- Track (background)
- Thumb (sliding indicator)
- Label (optional, left or right)

**States:** Off · On · Focused · Disabled-off · Disabled-on

**Token dependencies:**
- `clr-royal/50` — on-state track
- `clr-neutral/55` — off-state track
- `global/white` — thumb

---
