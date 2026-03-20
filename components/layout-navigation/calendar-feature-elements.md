# Calendar Feature Elements

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
