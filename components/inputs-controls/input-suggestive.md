# Input (Suggestive)

**Purpose:** Autocomplete/typeahead input — shows dropdown suggestions as the user types.

**Anatomy:**
- Input field (same as Input Basic)
- Dropdown suggestion list
  - Suggestion items (with match highlighting)
  - Loading state (spinner)
  - No results state

**States:**
- Empty
- Typing (dropdown opens)
- Suggestions loaded
- Item highlighted (keyboard nav)
- Selected
- Loading
- No results
- Error

**Token dependencies:**
- All Input Basic tokens
- `shadow-card` — dropdown elevation
- `clr-royal/50` — matched text highlight, selected item
- `global/white` — dropdown background

---
