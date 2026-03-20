# Skeletons

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
