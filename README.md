# OneHQ Design System

> **One source of truth** for every color, component, and pattern that makes OneHQ feel like OneHQ.

This documentation is extracted directly from the official Figma libraries and token files. It is the canonical reference for designers and engineers building on the OneHQ platform.

---

## What this is

The OneHQ Design System is a multi-layer architecture:

```
Primitive Colors
    ↓ aliased by
Semantic Tokens  ·  Chart Colors
    ↓ consumed by
Components
    ↓ assembled into
Patterns
```

**Primitives** are the raw values — every color swatch in every ramp. Named by family and lightness step (`clr-royal/50`), not by intent.

**Semantic tokens** map primitives to roles (`text/primary`, `status/error`, `surface/default`). This is the layer your component code should reference.

**Components** are the UI building blocks — buttons, inputs, cards, tables, modals. Each component is documented with its anatomy, variants, states, and token dependencies.

**Patterns** are compositions — how components combine into recurring page structures like master-detail layouts, CRM record views, and data table pages.

---

## Figma source libraries

| Library | Description |
|---|---|
| [Pattern Library](https://www.figma.com/design/qKL6hhOFWMH30bcMxjngCU) | All components and layout patterns |
| [Icons Library](https://www.figma.com/design/rezBIVAdkICAShyFzPMHT2) | 314 icons across 4 sizes |
| [Inputs & Controls](https://www.figma.com/design/7qCBGLBSUsnlNAJVl9Rz0b) | All form and input components |

---

## Quick reference

### Core interactive color
```css
--action-brand-primary:       #0073E5;  /* clr-royal/50 */
--action-brand-primary-hover: #0053B2;  /* clr-royal/40 */
```

### Text
```css
--text-primary:   #334466;  /* clr-neutral/40 — headings, labels */
--text-secondary: #627494;  /* clr-neutral/55 — descriptions, captions */
--text-disabled:  #8497B8;  /* clr-neutral/65 */
```

### Surfaces
```css
--surface-default:  #F2F6FC;  /* clr-neutral/95 — page background */
--surface-subtle:   #F9FBFE;  /* clr-neutral/98 — card inner areas */
--surface-elevated: #E1E8F5;  /* clr-neutral/90 */
```

### Status
```css
--status-error:   #DC3838;  /* clr-wine/50  */
--status-success: #246B2D;  /* clr-pea/40   */
--status-warning: #8F5A00;  /* clr-gold/20  */
--status-info:    #007BA8;  /* clr-sky/40   */
```

### Typography
```css
font-family: 'IBM Plex Sans', sans-serif;
font-weight: 400 | 500;  /* Regular | Medium */
```

---

## What's in this documentation

### Foundations
| Page | Description |
|---|---|
| [Foundations](foundations.md) | Visual language and design principles |
| [Primitive Colors](foundations/primitive-colors.md) | All 13 color families with full ramps |
| [Semantic Colors](foundations/semantic-colors.md) | Purposeful token aliases — use these in code |
| [Chart Colors](foundations/chart-colors.md) | 5 data visualization palettes |
| [Typography](typography.md) | IBM Plex Sans usage, weights, scale |
| [Spacing](spacing.md) | Spacing scale and values |
| [Tokens](tokens.md) | All tokens in one CSS reference |

### Icons
[314 icons](icons.md) across 4 sizes — Feather base extended with OneHQ-specific additions.

### Components
46 individual component pages across three groups: Basic Elements (13), Inputs & Controls (25), Layout & Navigation (8).

### Patterns
17 pattern pages: Layout Patterns (7) and CRM Patterns (10).

### Audit
[34 documented issues](audit.md) — 5 critical, 14 medium, 15 low.

---

## Design principles

**Clarity over decoration.** Every visual decision should aid comprehension. The neutral-dominant palette keeps UI recessive so content can breathe.

**Systematic over ad-hoc.** Use tokens. A hex value typed directly into a component is a future inconsistency.

**Predictable states.** Every interactive element needs a complete set: default, hover, active, focus, disabled.

**Accessible by default.** Text contrast, focus indicators, and status colors are chosen to meet WCAG AA minimum.

---

*Last extracted: 2026-03-20*
