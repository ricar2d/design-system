# Select (Basic)

**Purpose:** Dropdown selector — allows choosing one item from a list.

**Anatomy:**
- Trigger (input-like container)
  - Selected value / placeholder
  - Trailing chevron icon
- Dropdown panel
  - Search field (optional)
  - Option list
    - Option item (icon + label + description)
    - Selected indicator (checkmark)
  - Footer actions (optional)

**Variants:**
- Single select
- With search
- With grouping (sections)
- With icons
- Multi-select (see also: Controls)

**States:**
- Closed (default)
- Open
- Option highlighted
- Option selected
- Loading
- Empty/no results
- Error
- Disabled

**Token dependencies:**
- `clr-royal/50` — active trigger border, selected checkmark
- `clr-neutral/40` — selected value text
- `clr-neutral/55` — placeholder, option labels
- `global/white` — dropdown background
- `shadow-card` — dropdown elevation
- `radius-md` — trigger and dropdown radius

---
