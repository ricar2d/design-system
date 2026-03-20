# Avatars & Logos

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
