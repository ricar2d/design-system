# Buttons

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
