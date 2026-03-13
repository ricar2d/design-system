# Components — Layout & Navigation

**Source:** Pattern Library (`-PD- Pattern Library`)  
**Category:** Layouts & Navigation

---

## 1. Carousel

**Purpose:** Horizontal content slider for browsing multiple cards, media items, or featured content in sequence.

**Anatomy:**
- Track (overflow-hidden container)
- Slides (equally-sized content panels)
- Navigation arrows (left / right)
- Dot indicators (optional pagination)
- Drag/swipe support

**Variants:**
- Single item (full-width)
- Multi-item (shows partial next/prev)
- Auto-advancing
- Manual only

**States:**
- Default (resting)
- Transitioning
- First slide (left arrow disabled)
- Last slide (right arrow disabled)

**Token dependencies:**
- `clr-royal/50` — active dot indicator, navigation arrow hover
- `clr-neutral/55` — inactive dot indicators
- `Icon=chevron-left`, `Icon=chevron-right` — navigation
- `shadow-card` — slide card elevation

---

## 2. Resource Browser

**Purpose:** Navigation panel for browsing entities (contacts, companies, deals) — a persistent or slide-in left sidebar explorer.

**Anatomy:**
- Panel container
- Search/filter bar (top)
- Entity list (scrollable)
  - Entity item (avatar + name + meta)
  - Selected state
  - Group headers
- Load more / pagination

**States:**
- Default
- Loading
- Empty (no results)
- Entity item hover
- Entity item selected

**Token dependencies:**
- `clr-royal/50` — selected item indicator, search active
- `clr-neutral/40` — entity name
- `clr-neutral/55` — entity meta
- `global/white` — panel background
- `shadow-mid` — panel shadow (when floating)

**Usage guidelines:**
- Persistent in wide-screen layouts
- Collapsible or slide-in on narrower viewports
- Maintains scroll position on navigation

---

## 3. Dialog

**Purpose:** Persistent contextual panel — the backdrop structure for conversations, work items, and detail panels in the CRM.

**Anatomy:**
- Dialog container (full-height panel)
- Header
  - Avatar / entity icon
  - Title (entity name)
  - Actions bar (close, expand, etc.)
- Body (scrollable content area)
  - Tabbed content sections
  - Activity feed
  - Related items
- Footer (optional — reply bar, action row)

**Variants:**
- Message dialog (conversation view)
- Work item dialog (task/project detail)
- Discussion dialog

**States:**
- Collapsed
- Expanded (partial width)
- Full-screen
- Loading

**Token dependencies:**
- `global/white` — dialog background
- `shadow-mid` — dialog left edge shadow
- `clr-royal/50` — active tab, link actions
- `clr-neutral/40` — dialog title

**Usage guidelines:**
- Dialog is the primary detail view — not a modal overlay
- Slides in from the right edge of the main content area
- Tab structure allows navigating between related data types

---

## 4. Calendar Feature Elements

**Purpose:** Purpose-built components for the Calendar feature — event tiles, time grid, agenda items, day cells.

**Anatomy:**
- Month/Week/Day/Agenda views (switching via icon: `calendar-month`, `calendar-week`, `calendar-day`)
- Event tile
  - Color indicator
  - Event title
  - Time label
  - Participant avatars
- Today indicator
- Current time line (in time-grid views)
- Empty day cell
- Day header

**Variants:**
- Month grid
- Week time-grid
- Day view
- Agenda list

**States:**
- Event default
- Event hover
- Event selected/expanded
- Event being created (drag-to-create)
- Conflicting events

**Token dependencies:**
- `clr-royal/50` — today indicator, active view, event creation
- `clr-neutral/40` — day numbers, event titles
- `clr-neutral/55` — time labels, weekday names
- Custom event colors (from `clr-wine`, `clr-gold`, and extended palette)
- Icon set: `calendar-today/month/week/day/appointment`

---

## 5. Work Feature Elements

**Purpose:** UI components specific to the Work/Tasks feature — task cards, Kanban boards, project views.

**Anatomy:**
- Task card
  - Priority indicator
  - Task title
  - Assignee avatar
  - Due date
  - Status badge
  - Progress indicator
- Kanban column
  - Column header (status label + count)
  - Task card stack
  - Add task CTA
- List row (for list view)

**Variants:**
- Kanban board view
- List view
- Gantt/timeline (inferred)

**States (task):**
- To do
- In progress
- Blocked
- Complete

**Token dependencies:**
- `clr-royal/50` — in-progress state
- `clr-gold/60` — blocked state
- `clr-wine/50` — overdue, urgent
- *(green — inferred)* — complete state (color not found in defined tokens)
- `clr-neutral/40` — task title

> ⚠️ **Missing / recommended addition:** A success/complete color (green) appears necessary for task states but is not defined in the token system.

---

## 6. Filters

**Purpose:** Filter bar and filter components for narrowing table/list results.

**Anatomy:**
- Filter bar container
- Filter chips (active filters)
  - Filter label (field: value)
  - Remove button
- Add filter button
- Filter dropdown/popover
  - Field selector
  - Operator selector (is, is not, contains, etc.)
  - Value input
  - Apply / Cancel

**Variants:**
- Inline filter bar (above tables)
- Side panel filters (for browse views)
- Quick filter (icon-only toggles)

**States:**
- No filters active
- 1+ filters active (chips shown)
- Filter popover open
- Filter being configured

**Token dependencies:**
- `clr-royal/50` — active filter chip background, add filter CTA
- `clr-neutral/55` — inactive filter states
- `global/white` — chip background (inferred)
- `Icon=filter` — filter icon
- `Icon=x` — remove filter chip

---

## 7. Navigation

**Purpose:** Primary application navigation — top bar, side nav, breadcrumbs, tabs.

**Anatomy:**

### Top / App Bar
- Logo/brand mark
- Global search
- Module/feature navigation (links)
- User avatar + profile menu
- Notification bell
- Help/support link

### Sidebar navigation
- Module list items
  - Icon + label
  - Active indicator
  - Badge (for counts)
- Collapsible sections
- User profile footer

### Breadcrumbs
- Path items (links)
- Separator (`/` or `>`)
- Current page (non-link)

### Tabs
- Tab items (label, optional icon)
- Active indicator (underline or filled)
- Overflow handling

**States:**
- Nav item default
- Nav item hover
- Nav item active/current
- Nav item with badge

**Token dependencies:**
- `clr-royal/50` — active nav item, active tab indicator
- `clr-neutral/40` — nav labels
- `clr-neutral/55` — inactive nav icons
- `global/white` — nav bar surface
- `shadow-mid` — top bar/sidebar shadow

> ⚠️ **Note:** The library description for "Navigations" has a typo ("Navigaition") and the subtitle was empty in the index — this component may need more documentation.

---

## 8. Skeletons

**Purpose:** Loading placeholder animations shown while content is being fetched.

**Anatomy:**
- Skeleton block (rounded grey bar)
- Skeleton circle (for avatars)
- Skeleton card (mimics card structure)
- Shimmer animation

**Variants:**
- Text skeleton (1–3 lines)
- Avatar skeleton
- Card skeleton
- Table row skeleton
- List item skeleton

**Token dependencies:**
- `clr-surface-page` (`#f3f3f3`) — skeleton base
- *(lighter pulse color — inferred)* `#e8e8e8` — shimmer highlight
- `radius-md`, `radius-full` — shape radii

**Usage guidelines:**
- Show immediately on data fetch — do not show a spinner for more than 200ms before showing skeletons
- Skeleton shapes should match the approximate real content dimensions
- Animate with a shimmer/pulse effect (left-to-right highlight sweep)
