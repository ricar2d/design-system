# Components — Inputs & Controls

**Source:** Inputs & Controls Library (`-PD- Inputs & Controls Library`)  
**Total components:** 25

---

## 1. Input (Basic)

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

## 2. Input (Line)

**Purpose:** Minimalist borderless input — uses a bottom border only. Used for inline editing or compact forms.

**Anatomy:**
- Label (optional)
- Text field with bottom border only
- No container box

**States:**
- Empty
- Focused (line color transitions to `clr-royal/50`)
- Filled
- Error
- Disabled

**Token dependencies:**
- `clr-royal/50` — active line
- `clr-wine/50` — error line
- `clr-neutral/55` — default line
- `clr-neutral/40` — text

**Usage guidelines:**
- Use for inline editing contexts (table cells, card fields)
- Do not use in standalone form layouts — use Input Basic instead

---

## 3. Input (Suggestive)

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

## 4. Input (Range)

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

## 5. Input Helper

**Purpose:** Helper text and contextual guidance shown below input fields.

**Anatomy:**
- Icon (info, warning, error — optional)
- Helper text string

**Variants:**
- Neutral hint
- Error message (with error icon)
- Warning message
- Success message (inferred)
- Character count

**Token dependencies:**
- `clr-neutral/55` — hint text
- `clr-wine/50` — error text + icon
- `clr-gold/60` — warning text + icon
- `Icon=alert-circle` — error icon
- `Icon=info` — hint icon

---

## 6. Select (Basic)

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

## 7. Select (Just Text)

**Purpose:** A simplified select trigger that renders as plain text (no box/border) — for inline or contextual selects.

**Anatomy:**
- Text label (current value)
- Trailing chevron
- Dropdown (same as Select Basic)

**Usage guidelines:**
- Use for table column header filters or navigation-level selects
- Not for form fields — use Select Basic there

---

## 8. Select (Line)

**Purpose:** Select with bottom-border only styling — matches Input (Line) for visual consistency in line-style forms.

**Anatomy:**
- Bottom-border trigger
- Trailing chevron
- Dropdown panel (same as Select Basic)

---

## 9. Controls

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

## 10. Dropup

**Purpose:** Same as Select dropdown but opens upward — used when dropdown is near the bottom of the viewport.

**Anatomy:** Same as Select Basic, inverted direction.

**Usage guidelines:**
- Prefer standard Select; use Dropup only when dropdown would be clipped

---

## 11. Kebab

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

## 12. Textarea

**Purpose:** Multi-line text input for longer form content.

**Anatomy:**
- Label
- Multi-line text area
- Resize handle (optional)
- Character counter (optional)
- Helper text

**States:**
- Empty
- Focused
- Filled
- Error
- Disabled
- Read-only

**Token dependencies:** Same as Input Basic.

---

## 13. Rich Text

**Purpose:** WYSIWYG rich text editor for formatted long-form content.

**Anatomy:**
- Toolbar
  - Bold, Italic, Underline buttons
  - Alignment controls
  - List controls
  - Link, image insertion (optional)
  - Text color, fill color
- Editable content area

**Token dependencies:**
- `clr-neutral/40` — toolbar icons (active)
- `clr-neutral/55` — toolbar icons (inactive)
- `clr-royal/50` — active/selected format button
- Icon set: `bold`, `italic`, `underline`, `align-*`, `list`, `font-color`, `fill-color`

---

## 14. Search with Shortcuts

**Purpose:** Enhanced search input with keyboard shortcut hints and quick-access commands.

**Anatomy:**
- Search input
  - Leading search icon
  - Placeholder with shortcut hint (e.g., `⌘K`)
  - Clear button
- Results dropdown (inferred)
  - Category sections
  - Shortcut items
  - Recent searches

**Token dependencies:**
- `clr-neutral/55` — placeholder, shortcut hint text
- `clr-royal/50` — active/focused state
- `Icon=search` — leading icon

---

## 15. Groupings

**Purpose:** Visual grouping wrapper that clusters related form fields or controls under a shared context.

**Anatomy:**
- Group label / header
- Content area (contains inputs, controls)
- Optional border or background treatment

**Variants:**
- Labeled group (fieldset-like)
- Card group (bordered)
- Inline group (no border)

---

## 16. Multiple Switcher

**Purpose:** Segmented control / tab switcher for switching between 2–5 options within a context.

**Anatomy:**
- Container (pill or rounded rect)
- Option segments (equal width)
  - Active segment (filled)
  - Inactive segments (transparent)
  - Labels

**States:**
- Segment default
- Segment active
- Segment hover
- Disabled

**Token dependencies:**
- `clr-royal/50` — active segment fill
- `global/white` — active segment text
- `clr-neutral/55` — inactive text
- `radius-full` — container radius (pill style)

**Usage guidelines:**
- Use for 2–5 mutually exclusive options
- All options should be similar in length
- Do not use as primary navigation tabs

---

## 17. Or Input

**Purpose:** Composite input pattern with an "OR" divider — allows entering a value using two alternative methods.

**Anatomy:**
- Primary input
- "OR" divider label
- Secondary input/option

**Usage guidelines:**
- Common pattern for: "Enter email OR phone number"
- Typically used in CRM data entry where multiple field types are acceptable

---

## 18. Drag & Drop

**Purpose:** Drag handles and drop zones for reordering items or uploading files via drag.

**Anatomy (reorder):**
- Drag handle icon (`Icon=grabber`)
- Draggable item container
- Drop zone (highlighted on hover)
- Drop indicator line

**Anatomy (file drop):**
- Drop zone container
- Upload icon
- Label + subtext
- File type/size hint

**States:**
- Default
- Drag over (highlighted drop zone)
- Dragging item
- Dropped/complete

**Token dependencies:**
- `clr-royal/50` — drop zone highlight, drop indicator
- `clr-neutral/55` — drag handle icon
- `Icon=grabber` — drag handle

---

## 19. Uploader Card

**Purpose:** File attachment upload UI — card-style drop zone with file preview.

**Anatomy:**
- Upload card container
- Upload prompt (icon + text)
- File type/size restrictions text
- Browse button
- Uploaded file preview (thumbnail or file icon)
- Remove button

**States:**
- Empty (prompt)
- Drag over
- Uploading (progress)
- Complete (with preview)
- Error (invalid file)

---

## 20. Attachment Groups

**Purpose:** Display and manage a collection of attached files on a record.

**Anatomy:**
- Group container
- Attachment item
  - File type icon (pdf, xls, csv, etc.)
  - Filename
  - File size
  - Download button
  - Remove button
- Add attachment CTA

**Token dependencies:**
- `Icon=file-pdf`, `Icon=file-xls`, `Icon=file-csv` — file type icons
- `clr-royal/50` — download link
- `clr-wine/50` — remove/delete action

---

## 21. Avatar Cropper

**Purpose:** Interactive image crop tool for setting user or entity profile photos.

**Anatomy:**
- Image preview area
- Crop selection handles
- Zoom slider
- Confirm / Cancel actions

**States:**
- No image (upload prompt)
- Image loaded
- Cropping (handles active)
- Confirmed

---

## 22. Swatch Selector

**Purpose:** Color picker using swatches — for selecting a color from a predefined palette.

**Anatomy:**
- Swatch grid
  - Colored circles/squares
  - Selected indicator (ring or checkmark)
- Optional custom color input

**Token dependencies:**
- System colors (`clr-royal/50`, `clr-wine/50`, `clr-gold/60`, etc.)
- `clr-neutral/40` — selected ring

---

## 23. Question Selector

**Purpose:** Interactive question-style selector — allows selecting from a set of options presented as questions or statements.

**Anatomy:**
- Question prompt text
- Option items (radio-like)
  - Option label
  - Description (optional)
  - Selected indicator

**Usage guidelines:**
- Used in onboarding flows, preference settings, and form wizards
- Not a replacement for standard radio buttons in data forms

---

## 24. Form Error List

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

## 25. Layout

**Purpose:** Layout scaffolding components for Inputs & Controls contexts — form layouts, field grids.

**Anatomy:**
- Single column layout
- Two column layout
- Grid layout (for multi-field forms)
- Inline layout (side-by-side label + field)

**Usage guidelines:**
- Use single column for simple forms (3–5 fields)
- Use two column for data-dense forms
- Always group related fields visually
