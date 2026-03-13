# Components — Basic Elements

**Source:** Pattern Library (`-PD- Pattern Library`)  
**Category:** Basic elements

---

## 1. Avatars & Logos

**Purpose:** Display user or entity identity visuals — profile photos, initials, brand logos.

**Anatomy:**
- Container shape (circle or rounded square)
- Image or initials fallback
- Optional status indicator (dot/badge)

**Variants (inferred):**
- Sizes: XS, SM, MD, LG, XL (standard avatar size scale)
- Types: Photo, Initials, Logo
- States: Default, with status dot, group/stack

**Token dependencies:**
- `clr-royal/50` — border/active ring
- `clr-neutral/40` — initials text
- `global/white` — background
- `radius-full` — circular shape

**Usage guidelines:**
- Use circular avatars for people
- Use rounded-square avatars for organization/brand logos
- Initials fallback should use 1–2 letters
- Stack avatars in groups with slight overlap (use negative margin)

---

## 2. Arrows & Connectors

**Purpose:** Visual connectors for flow diagrams, relationship indicators, and directional cues within the UI.

**Anatomy:**
- Line/path
- Arrowhead (filled or outlined)
- Optional label

**Variants (inferred):**
- Direction: Left, Right, Up, Down, Diagonal
- Style: Solid line, dashed line
- Arrowhead: Single, double, none

**Token dependencies:**
- `clr-neutral/55` — default connector color
- `clr-royal/50` — active/highlighted connector

**Usage guidelines:**
- Used in specific diagram or workflow contexts
- Not for general navigation (use chevrons from icon set instead)

---

## 3. Badges

**Purpose:** Compact indicators of category, status, type, or count. Used throughout tables, cards, and lists.

**Anatomy:**
- Container (pill shape)
- Label text
- Optional leading icon or dot

**Variants (inferred from library description: "Indicators of categories"):**
- Semantic: Default, Primary (blue), Success (green?), Warning (gold), Error (red)
- Size: SM, MD
- Style: Filled, Outlined, Dot-only

**States:**
- Default
- Interactive (clickable filter tag)

**Token dependencies:**
- `clr-royal/50` — primary badge
- `clr-wine/50` — error/destructive badge
- `clr-gold/60` — warning badge
- `clr-neutral/55` — neutral/default badge
- `global/white` — text on colored badge
- `radius-full` — pill shape

**Usage guidelines:**
- Use badges for static category labels
- Use tags/chips (interactive version) for filterable UI
- Keep badge text short (1–3 words max)

---

## 4. Brand Elements

**Purpose:** OneHQ brand assets — logos, wordmarks, brand marks.

**Anatomy:**
- Primary logo (full wordmark)
- Icon mark (standalone symbol)
- Monochrome variants

**Variants:**
- Full color
- White (for dark backgrounds)
- Monochrome dark
- Icon-only

**Usage guidelines:**
- Do not modify, stretch, or recolor brand assets
- Use white variant only on brand-colored (`clr-royal/50`) or dark backgrounds
- Minimum size applies — do not use below threshold size

---

## 5. Buttons

**Purpose:** Primary interactive elements for triggering actions — CTA, form submission, navigation.

**Anatomy:**
- Container (background + border radius)
- Label text (Medium weight)
- Optional leading icon
- Optional trailing icon

**Variants:**
- Hierarchy: Primary, Secondary, Ghost/Text, Destructive, Link
- Size: SM, MD, LG
- Icon: Icon-only, Left icon, Right icon, No icon

**States:**
- Default
- Hover
- Active/Pressed
- Focus (keyboard)
- Disabled
- Loading (spinner)

**Token dependencies:**
- `clr-royal/50` — primary fill
- `global/white` — primary label
- `clr-neutral/40` — secondary label
- `clr-wine/50` — destructive variant
- `clr-neutral/55` — disabled state text
- `font-weight-medium` — label
- `radius-md` — border radius (inferred)

**Usage guidelines:**
- Use Primary for the single most important action per screen/modal
- Use Secondary for secondary actions alongside Primary
- Use Ghost/Text for low-priority or repetitive actions in lists
- Use Destructive only for delete/remove actions with confirmation

**Interaction behavior:**
- Primary: Hover darkens background; active depresses
- Link: Underline on hover
- Disabled: Reduced opacity, no cursor change

---

## 6. Cards

**Purpose:** Container component for grouping related content — the fundamental layout unit of the product.

**Anatomy:**
- White surface (`global/white`)
- Shadow (`shadow-card`)
- Border radius (`radius-lg` — 39px on canvas, scaled)
- Header area (optional)
- Content area
- Footer/actions area (optional)

**Variants (inferred from "all the basic and complex cards"):**
- Basic card: White surface with shadow
- Complex card: With header, media area, or nested components
- Option card: Used in library indices — image + label + link
- Data card: For metric/KPI display
- Contact card: CRM-specific person/company card
- Activity card: Timeline event

**States:**
- Default
- Hover (shadow elevation increase — inferred)
- Selected/Active
- Loading (skeleton state)

**Token dependencies:**
- `global/white` — card background
- `shadow-card` — elevation
- `radius-lg` — corner radius
- `clr-surface-inner` — inner sections (`#f9f9f9`)
- `clr-neutral/40` — card title
- `clr-neutral/55` — card subtitle/meta

**Usage guidelines:**
- Cards should always have adequate internal padding
- Use shadow-card for floating cards; no shadow for inline embedded cards
- Avoid nesting cards deeper than 2 levels

---

## 7. Empty States

**Purpose:** Placeholder UI for when a section, list, or feature has no data yet.

**Anatomy:**
- Illustration or icon
- Title (primary message)
- Description (supporting text)
- CTA button (optional)

**Variants (inferred):**
- No data (first-use onboarding)
- No results (after filter/search)
- Error state
- Permission denied

**Token dependencies:**
- `clr-neutral/40` — title
- `clr-neutral/55` — description
- `clr-royal/50` — CTA button

**Usage guidelines:**
- Always include a clear message explaining why it's empty
- Include a CTA when there is a clear action to take
- Use consistent tone across empty states

> ⚠️ **Note:** The library description for Empty States shows "..." as the subtitle, suggesting this component page may be incomplete.

---

## 8. Lists

**Purpose:** Vertical sequences of items — the primary pattern for displaying entity records.

**Anatomy:**
- List container
- List item row
  - Leading element (avatar, icon, checkbox)
  - Primary label
  - Secondary label / metadata
  - Trailing element (action, badge, chevron)
- Divider between items (optional)

**Variants (inferred from "The list used everywhere"):**
- Simple list: Text only
- List with icon: Leading icon per item
- List with avatar: Person/entity lists
- List with actions: Trailing action buttons
- List with checkbox: Selectable/multi-select
- Grouped list: With section headers

**States (per item):**
- Default
- Hover
- Selected/Active
- Disabled

**Token dependencies:**
- `clr-neutral/40` — primary label
- `clr-neutral/55` — secondary label
- `clr-royal/50` — active/selected state
- `global/white` — item background
- `clr-surface-page` — hover background (inferred)

---

## 9. Tables

**Purpose:** Structured data display for records, reports, and CRM entity lists.

**Anatomy:**
- Table header row
  - Column label (Medium weight)
  - Sort indicator (icon)
  - Resize handle (optional)
- Table body rows
  - Cell content
  - Row actions (hover-reveal)
- Pagination / footer

**Variants:**
- Standard table
- Data grid (referenced as separate component — `Data Grid` node found)
- Compact/dense table
- Striped rows (inferred)
- Bordered cells (inferred)

**States (per row):**
- Default
- Hover
- Selected (checkbox or row click)
- Active/Expanded
- Loading (skeleton)

**Token dependencies:**
- `clr-neutral/40` — header labels
- `clr-neutral/55` — cell content
- `clr-royal/50` — sort active, selected row indicator
- `global/white` — row background
- `shadow-mid` — sticky header shadow (inferred)

---

## 10. Tooltips

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

## 11. Modals & Popups

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

## 12. Notifications & Indicators

**Purpose:** System-level feedback — growl toasts, progress bars, spinners.

**Anatomy (Toast/Growl):**
- Container (rounded, shadowed)
- Icon (status indicator)
- Title + description
- Close button
- Auto-dismiss timer (optional)

**Anatomy (Progress bar):**
- Track (background)
- Fill (progress indication)
- Label (percentage or step)

**Anatomy (Spinner):**
- Animated circular indicator

**Variants:**
- Toast: Success, Error, Warning, Info
- Progress: Linear bar, circular
- Spinner: SM, MD, LG

**Token dependencies:**
- `clr-royal/50` — info / progress fill
- `clr-wine/50` — error toast
- `clr-gold/60` — warning toast
- `global/white` — toast background
- `shadow-card` — toast elevation

---

## 13. Section Elements

**Purpose:** Typography and structural elements used to organize page and card sections.

**Anatomy:**
- Section title
- Section divider (horizontal rule)
- Section label (uppercase/caps label)

**Variants:**
- Title only
- Title + divider
- Title + description
- Divider only

**Token dependencies:**
- `clr-neutral/40` — section title
- `clr-neutral/55` — section description
- `clr-surface-page` / `clr-neutral/55` — divider color (inferred)
- `font-weight-medium` — section title weight
