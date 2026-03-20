# Work Feature Elements

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
