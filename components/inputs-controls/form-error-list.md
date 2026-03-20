# Form Error List

**Purpose:** Summary of all validation errors in a form, displayed at the top or bottom of the form.

**Anatomy:**
- Error container
- Error count / header
- Error list
  - Error item (field name + message)
  - Link to field (optional)

**Token dependencies:**
- `clr-wine/50` — error text and icon
- `Icon=alert-circle` — error indicator

**Usage guidelines:**
- Show after form submission attempt
- Each error should link to or describe the problematic field
- Do not show on first render — only after user interaction

---
