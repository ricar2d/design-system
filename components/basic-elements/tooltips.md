# Tooltips

**Purpose:** Contextual short descriptions triggered on hover/focus of an element.

**Anatomy:**
- Container (dark background pill)
- Label text (white, small)
- Arrow pointer (direction varies)

**Variants (inferred from "Tooltip popups"):**
- Direction: Top, Bottom, Left, Right
- Size: SM (short label), MD (multi-line)

**States:**
- Hidden (default)
- Visible (on hover/focus)

**Token dependencies:**
- `clr-neutral/40` — tooltip background (dark navy)
- `global/white` — tooltip text
- `radius-sm` — border radius

**Usage guidelines:**
- Use for icon-only buttons that need labels
- Keep text to 1–2 words or a short phrase
- Do not put interactive content inside a tooltip

> ⚠️ **Note:** Library label has a typo: "Tootlips" — should be "Tooltips".

---
