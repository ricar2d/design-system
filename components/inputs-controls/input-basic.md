# Input (Basic)

**Purpose:** Standard single-line text input — the primary data entry component.

**Anatomy:**
- Label (above)
- Input container
  - Leading icon (optional)
  - Text value / placeholder
  - Trailing icon/action (optional)
- Helper text (below)
- Error message (below — on error state)

**Variants:**
- With/without leading icon
- With/without trailing icon (clear, eye-toggle, etc.)
- Sizes: SM, MD (inferred)

**States:**
- Empty (placeholder)
- Filled
- Focused (active border — `clr-royal/50`)
- Error (red border — `clr-wine/50`)
- Disabled (reduced opacity)
- Read-only

**Token dependencies:**
- `clr-royal/50` — focused border
- `clr-wine/50` — error border
- `clr-neutral/40` — filled text
- `clr-neutral/55` — placeholder text, label
- `global/white` — input background
- `radius-md` — corner radius

---
