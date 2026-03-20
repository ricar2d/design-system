# Modals & Popups

**Purpose:** Overlay dialogs for confirmations, forms, detail views, and focused interactions.

**Anatomy:**
- Backdrop overlay
- Modal container
  - Header (title + close button)
  - Body content (scrollable)
  - Footer (action buttons)

**Variants (inferred):**
- Confirmation dialog (small, 2-button)
- Form modal (medium, scrollable body)
- Detail view modal (large, full context)
- Fullscreen modal
- Bottom sheet (mobile)

**States:**
- Closed
- Opening (animation — inferred)
- Open
- Closing (animation — inferred)

**Token dependencies:**
- `global/white` — modal background
- `clr-neutral/40` — modal title
- `shadow-mid` — modal elevation
- `radius-lg` — modal border radius
- `clr-royal/50` — primary action
- Backdrop: `rgba(clr-neutral-40, 0.5)` (inferred)

---
