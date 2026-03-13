# Patterns — CRM Patterns

**Source:** Pattern Library (inferred from component catalog and library structure)

---

## Overview

OneHQ is a CRM/productivity platform. Several component patterns are purpose-built for CRM workflows. This document catalogs the CRM-specific UI patterns that go beyond generic component usage.

---

## Pattern 1: Entity Record Header

**Used in:** Contact, Company, Deal, and Lead detail pages.

**Structure:**
```
[Record header bar]
  ├── [Entity avatar / logo]
  ├── [Entity name (large, primary text)]
  ├── [Entity type badge]
  ├── [Key attributes row]
  │     └── Email · Phone · Company · Status (inline icons + values)
  └── [Actions toolbar]
        ├── Primary CTA (e.g., "Send Email")
        ├── Secondary actions (Call, Task, Note)
        └── Kebab (more actions)
```

**Token dependencies:**
- Entity name: `clr-neutral/40`, Medium weight, large size
- Attributes: `clr-neutral/55`, Regular, small
- Primary CTA: `clr-royal/50`
- Avatar: `radius-full` (circle)

---

## Pattern 2: Activity Feed / Timeline

**Used in:** Entity detail pages, Dialog panel, Work items.

**Structure:**
```
[Activity feed]
  ├── [Timeline axis (vertical line)]
  └── [Activity item] × N
        ├── [Activity icon (type indicator)]
        ├── [Author avatar]
        ├── [Activity content]
        │     ├── Author name + timestamp
        │     ├── Activity description / note text
        │     └── Attachments (optional)
        └── [Reaction / action bar (optional)]
```

**Activity types and icons:**
| Activity | Icon |
|---|---|
| Email | `Icon=mail` |
| Call | `Icon=phone` |
| Note | `Icon=edit-3` |
| Task | `Icon=check-square` |
| Meeting | `Icon=calendar` |
| File attached | `Icon=paperclip` |
| Status change | `Icon=activity` |
| Assignment | `Icon=user` |

**Token dependencies:**
- Timeline line: `clr-neutral/55` at low opacity
- Activity icon: `clr-royal/50` (for brand activities) or `clr-neutral/55`
- Timestamp: `clr-neutral/55`, small text
- Content text: `clr-neutral/40`

---

## Pattern 3: Relationship Panel

**Used in:** Entity sidebars, showing related contacts, companies, deals.

**Structure:**
```
[Panel section]
  ├── Section header (label + "Add" button)
  └── [Related entity list]
        └── [Entity row]
              ├── Avatar
              ├── Entity name (link)
              ├── Role/type label
              └── Remove action
```

**Token dependencies:**
- Section header: `clr-neutral/40`, Medium
- Add button: `clr-royal/50`
- Entity name: link style (`clr-royal/50`, underline on hover)
- Role label: `clr-neutral/55`

---

## Pattern 4: Pipeline / Kanban View

**Used in:** Deals pipeline, Sales stages, Task boards.

**Structure:**
```
[Board container: horizontal scroll]
  └── [Pipeline column] × N
        ├── [Column header]
        │     ├── Stage name
        │     ├── Count badge
        │     └── Column value (sum, for deals)
        ├── [Deal/Task cards stack]
        │     └── [Card]
        │           ├── Entity name
        │           ├── Value / progress
        │           ├── Owner avatar
        │           └── Due date / stage badge
        └── [Add card button]
```

**Token dependencies:**
- Column header: `clr-neutral/40`, Medium
- Card: `global/white`, `shadow-card`, `radius-lg`
- Stage badge: semantic colors per stage
- Value text: `clr-neutral/40`
- Add button: `clr-royal/50`

---

## Pattern 5: Contact / Company Quick Preview Card

**Used in:** Hovering over a linked entity name in tables, activity feeds, emails.

**Structure:**
```
[Popover card: shadow-card, radius-lg]
  ├── [Header: avatar + name + type]
  ├── [Key fields: 3–5 rows]
  │     └── [Icon + label + value]
  └── [Actions: View, Email, Call]
```

**Token dependencies:**
- Card: `global/white`, `shadow-card`
- Trigger: hover on linked entity name
- Actions: `clr-royal/50`

---

## Pattern 6: Inline Editing Pattern

**Used in:** Table cells, record field values, card content.

**Structure:**
```
[Field value — display mode]
  └── Click/hover → [Field value — edit mode]
        ├── Input (Basic) or Select
        └── Save / Cancel inline actions
```

**Key behaviors:**
- Click field value to enter edit mode
- `Enter` or blur to save
- `Escape` to cancel
- Input style switches from display text to `Input (Line)` style
- Save/cancel appear as small inline icon buttons

**Token dependencies:**
- Display text: `clr-neutral/40`
- Edit mode input: `Input (Line)` component
- Save: `clr-royal/50` (`Icon=check`)
- Cancel: `clr-neutral/55` (`Icon=x`)

---

## Pattern 7: Data Grid (Advanced Table)

**Found:** As a standalone node reference (`Data Grid`) in the Pattern Library canvas.

**Structure:**
```
[Data grid]
  ├── [Toolbar: column config, filters, export, search]
  ├── [Pinned header row]
  ├── [Data rows with inline editing]
  │     ├── Row selection checkbox
  │     ├── Pinned columns (left)
  │     ├── Scrollable columns
  │     └── Row action kebab
  ├── [Column resize handles]
  ├── [Column reorder (drag)]
  └── [Footer: pagination, row count, load more]
```

**Advanced features (inferred from icon usage):**
- Column-level filtering (`Icon=filter`)
- Formula columns (`Icon=formula`)
- Nested rows (`Icon=nested-in`, `Icon=nested-out`)
- Column view toggle (`Icon=coulmn-view`)
- Top filter bar (`Icon=top filter`)
- Sidebar panel (`Icon=sidebar left`, `Icon=sidebar right`)
- Title placement above/below table (`Icon=title-above-table`, `Icon=title-bellow-table`)
- Export: PDF, CSV, XLS (`Icon=file-pdf`, `Icon=file-csv`, `Icon=file-xls`)

---

## Pattern 8: Communication / Messaging

**Used in:** Dialog panel messaging, email compose, note creation.

**Structure (Message thread):**
```
[Thread container]
  ├── [Message list (scrollable)]
  │     └── [Message item]
  │           ├── Avatar
  │           ├── Sender name + timestamp
  │           ├── Message content (rich text supported)
  │           └── Attachment chips
  └── [Reply composer]
        ├── Rich text input
        ├── Attachment button
        ├── Formatting toolbar
        └── Send button
```

**Key CRM-specific behaviors:**
- Messages are linked to entity records
- Email messages show full header (To, CC, BCC, Subject)
- Activities auto-logged on send
- `Icon=send` for send action

---

## Pattern 9: Search with Entity Results

**Used in:** Global search, record lookup, mention autocomplete.

**Structure:**
```
[Search input: Search with Shortcuts component]
  └── [Results panel]
        ├── [Section: People]
        │     └── Entity rows (avatar + name + company)
        ├── [Section: Companies]
        │     └── Entity rows (logo + name + type)
        ├── [Section: Deals]
        │     └── Entity rows (name + stage + value)
        └── [Section: Recent]
              └── Previously viewed items
```

**Token dependencies:**
- Section headers: `clr-neutral/55`, small, Medium weight
- Entity names: `clr-neutral/40`
- Match highlight: `clr-royal/50`
- Keyboard shortcut hint: `clr-neutral/55`

---

## Pattern 10: Bulk Action Bar

**Used in:** Data tables and lists when one or more rows are selected.

**Structure:**
```
[Bulk action bar: appears above table on selection]
  ├── Selection count ("3 selected")
  ├── Primary bulk actions (Assign, Tag, Export)
  ├── Destructive action (Delete)
  └── Deselect / close button
```

**Token dependencies:**
- Bar background: `clr-royal/50` or `clr-neutral/40` (inferred)
- Bar text: `global/white`
- Destructive action: `clr-wine/50`
