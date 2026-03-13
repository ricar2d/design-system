# Design System Audit

**Libraries audited:**
- Pattern Library (`-PD- Pattern Library`)
- Icons Library (`-PD- Icons Library`)
- Inputs & Controls Library (`-PD- Inputs & Controls Library`)

**Audit date:** 2026-03-13

---

## Summary

| Category | Issues found | Critical | Medium | Low |
|---|---|---|---|---|
| Token inconsistencies | 8 | 2 | 4 | 2 |
| Naming inconsistencies | 9 | 0 | 4 | 5 |
| Missing definitions | 7 | 3 | 3 | 1 |
| Component issues | 5 | 0 | 3 | 2 |
| Typos | 5 | 0 | 0 | 5 |
| **Total** | **34** | **5** | **14** | **15** |

---

## 🔴 Critical Issues

### C-01: Color token ramp is undefined
**Libraries:** All three  
**Problem:** Only the base step (`/50` or `/60`) of each color family is explicitly defined. The system has `clr-royal/50` but no `/10`, `/20`, `/30`, `/40`, `/60`, `/70` steps. Component states (hover, disabled, selected, focus ring) likely require lighter tints that are hardcoded rather than tokenized.  
**Impact:** Impossible to ensure consistent hover/focus states. Changes to the primary color require hunting down hardcoded values.  
**Recommendation:** Extract a full ramp (5–9 steps) for Royal, Neutral, Wine, and Gold families from actual component usage.

---

### C-02: Surface colors not tokenized
**Libraries:** All three  
**Problem:** `#f3f3f3` (page background) and `#f9f9f9` (card inner background) appear consistently throughout all libraries but are never defined as tokens. They are hardcoded values.  
**Impact:** If the surface color needs to change (e.g., dark mode, theming), all components would need individual updates.  
**Recommendation:** Define `clr-surface-page: #f3f3f3` and `clr-surface-inner: #f9f9f9` as explicit tokens immediately.

---

### C-03: No spacing token system
**Libraries:** All three  
**Problem:** No spacing tokens exist anywhere in the libraries. All padding, gap, and margin values are hardcoded in component definitions.  
**Impact:** Spacing changes require global search-and-replace. Developers must guess values rather than reference a system.  
**Recommendation:** Define a base-4 spacing scale (`space-1` through `space-32`) and migrate component values to use it.

---

### C-04: No motion/animation tokens
**Libraries:** All three  
**Problem:** Zero animation or transition tokens are defined. This means every component team defines their own transitions, leading to inconsistent timing across the product.  
**Impact:** The product feels inconsistent — some things animate quickly, others slowly. No standardized UX rhythm.  
**Recommendation:** Define: `duration-fast: 100ms`, `duration-default: 200ms`, `duration-slow: 300ms`, `easing-default: ease-in-out`.

---

### C-05: Success/green color missing from token system
**Libraries:** Pattern Library  
**Problem:** The Work Feature components (task completion, success notifications) clearly need a "success" or "green" semantic color. No green token is defined anywhere in the three libraries.  
**Impact:** Success states are likely handled with ad-hoc color values, breaking visual consistency.  
**Recommendation:** Define `clr-green/50` (or `clr-success`) for use in: task completion, success toasts, positive trend indicators.

---

## 🟡 Medium Issues

### M-01: Token naming format inconsistency across libraries
**Libraries:** Pattern Library vs Inputs & Controls Library  
**Problem:** The same tokens exist under two different naming conventions:
- Pattern Library: `clr-neutral/40` (hyphen-separated, slash notation)
- Inputs & Controls Library: `clrNeutral/40` (camelCase)

Both resolve to `#334466`. This happens for both neutral tokens.  
**Recommendation:** Standardize on `clr-neutral/40` format (hyphen-separated). Update all Figma variable references in the Inputs & Controls Library.

---

### M-02: Icon naming inconsistency (32px vs other sizes)
**Library:** Icons Library  
**Problem:** The `Icon--32px` frame uses the property key `Icon=[name]` while all other size frames (`24px`, `16px`, `12px`) use `Type=[name]`.  
**Impact:** Component properties that use icons at different sizes reference them with different property names, breaking consistent prop-passing in component variants.  
**Recommendation:** Standardize all icon frames to use `Icon=[name]`. The 24px, 16px, and 12px frames should be updated to match.

---

### M-03: Filled icon set is severely under-developed
**Library:** Icons Library  
**Problem:** Only 3 filled icons exist (`pin`, `x-circle-small`, `dot`). If any component needs a filled icon for a "selected/active" state, it either uses the stroke version (incorrect semantics) or creates a one-off.  
**Impact:** Inconsistent treatment of selected vs unselected icon states.  
**Recommendation:** Define a policy: either create filled variants for the core 20–30 most-used icons, or document that stroke icons are used in all states and filled is reserved for decoration only.

---

### M-04: Legacy deprecated tokens still present
**Library:** Icons Library  
**Problem:** Two legacy tokens are explicitly marked as deprecated but still present:
- `legacy(Deprecated)/surface/neutral--dark` → `#334466`
- `legacy(Deprecated)/surface/icon--base` → `#627494`

These duplicate `clr-neutral/40` and `clr-neutral/55`.  
**Impact:** If any component still references the legacy names, updates to neutral colors would not propagate correctly.  
**Recommendation:** Audit all components for legacy token usage, migrate to current tokens, then delete legacy entries.

---

### M-05: Duplicate wine token entry
**Library:** Icons Library  
**Problem:** `clr-wine/50 (base)` and `Wine - clrWine/50 (base)` both resolve to `#dc3838`. Different prefix format for the same token.  
**Recommendation:** Delete `Wine - clrWine/50 (base)` and keep only `clr-wine/50 (base)`.

---

### M-06: No type scale defined
**Libraries:** All three  
**Problem:** No typographic scale (heading levels, body text sizes, captions) is formalized. Text sizes are hardcoded per component.  
**Impact:** Typography is inconsistent across different parts of the product. Developers cannot look up what size to use for an H2 or body text.  
**Recommendation:** Derive the scale from measured component values and define it as tokens (see `typography.md`).

---

### M-07: `Empty States` component page appears incomplete
**Library:** Pattern Library  
**Problem:** The Empty States option card in the index shows "..." as its description — suggesting the component page was never fully built out.  
**Impact:** Empty state usage is undocumented and inconsistent across the product.  
**Recommendation:** Complete the Empty States component page with variants, usage guidelines, and copy direction.

---

### M-08: "Navigation" page may be incomplete
**Library:** Pattern Library  
**Problem:** The Navigations option card in the Layouts & Navigation section has an empty subtitle and a typo in its internal link ("Navigaition").  
**Impact:** Navigation components may be underdocumented.  
**Recommendation:** Review and complete the Navigation component page.

---

## 🔵 Low Issues

### L-01: Typo — "Tootlips" in component index
**Library:** Pattern Library  
**Problem:** Component link labeled "Tootlips" — should be "Tooltips".  
**Recommendation:** Rename frame/link to "Tooltips".

---

### L-02: Typo — "Arrows & Conectors"
**Library:** Pattern Library  
**Problem:** Component link labeled "Arrows & Conectors" — should be "Arrows & Connectors".  
**Recommendation:** Fix typo.

---

### L-03: Typo — "title-bellow-table"
**Library:** Icons Library  
**Problem:** Icon named `title-bellow-table` — should be `title-below-table`.  
**Recommendation:** Rename icon across all 4 size frames.

---

### L-04: Typo — "Foorm Error List" (link text)
**Library:** Inputs & Controls Library  
**Problem:** The internal link text says "Foorm Error List" — should be "Form Error List".  
**Recommendation:** Fix typo in index card.

---

### L-05: Typo — "Slect (Just Text)" (link text)
**Library:** Inputs & Controls Library  
**Problem:** Index card label says "Slect (Just Text)" — should be "Select (Just Text)".  
**Recommendation:** Fix typo.

---

### L-06: Icon naming — spaces instead of hyphens
**Library:** Icons Library  
**Problem:** Several icons use spaces in names rather than hyphens:
- `sidebar left` → should be `sidebar-left`
- `sidebar right` → should be `sidebar-right`
- `top filter` → should be `top-filter`

**Recommendation:** Rename affected icons in all size frames.

---

### L-07: Icon "coulmn-view" misspelling
**Library:** Icons Library  
**Problem:** `coulmn-view` should be `column-view`.  
**Recommendation:** Rename in all size frames.

---

### L-08: `Undo` / `Redo` capitalized inconsistently
**Library:** Icons Library  
**Problem:** Most icon names are lowercase. `Undo` and `Redo` use Title Case.  
**Recommendation:** Rename to `undo` and `redo`.

---

### L-09: `hexagon-variant` only in 16px
**Library:** Icons Library  
**Problem:** `hexagon-variant` exists only in the 16px frame. `hexagon` exists at all sizes. This variant is not available at 24px or 32px.  
**Recommendation:** Either add to all sizes or document that it is intentionally 16px-only.

---

## Component / Pattern Gaps

| Gap | Priority | Notes |
|---|---|---|
| Dark mode / theming | High | No dark mode tokens or guidelines exist |
| Focus states | High | No documented focus ring style |
| Responsive breakpoints | High | No breakpoints defined |
| Z-index system | Medium | No z-index tokens for layering modals, tooltips, dropdowns |
| Form validation patterns | Medium | `Input Helper` and `Form Error List` exist but validation state flow is undocumented |
| Date/time picker | Medium | Calendar Feature exists but a standalone date picker component is not catalogued |
| Numeric stepper input | Low | Common form control, not found in libraries |
| Tag/Chip (interactive badge) | Low | Badge exists but interactive tag/chip variant not explicitly catalogued |
| Pagination component | Low | Referenced in layout patterns but not a standalone library component |

---

## Normalization Recommendations (Priority Order)

1. **Tokenize `#f3f3f3` and `#f9f9f9`** as surface tokens (Critical — affects every component)
2. **Define spacing token scale** — adopt base-4 (Critical — affects implementation consistency)
3. **Extract and document full color ramps** for Royal, Neutral, Wine, Gold (Critical)
4. **Add success/green token** for task completion and positive states (Critical)
5. **Standardize token naming** — remove camelCase variants, unify to `clr-*` format (Medium)
6. **Standardize icon naming** — `Icon=` for all sizes, fix typos, fix spaces (Medium)
7. **Define type scale tokens** derived from measured component values (Medium)
8. **Remove deprecated legacy tokens** after audit (Medium)
9. **Add motion tokens** (Medium)
10. **Complete Empty States and Navigation pages** (Medium)
11. **Fix all typos** in library labels (Low — but affects developer trust)
