# Semantic Colors

Semantic tokens are named by **purpose**, not by visual appearance. They are aliases that point to specific [primitive color](/foundations/primitive-colors) steps. This layer of abstraction means you can retheme the product by only changing semantic mappings — component code stays untouched.

**Source:** `semantic.json` — Figma variable collection "Semantic Colors"

---

## How to use these tokens

Always use semantic tokens in component code — never reference primitives directly. Primitives describe what a color *is*; semantics describe what a color *does*.

```css
/* ✅ Correct — semantic */
color: var(--text-primary);
background: var(--surface-default);
border-color: var(--status-error-border);

/* ❌ Wrong — primitive reference in component code */
color: var(--clr-neutral-40);
```

---

## Action / Brand

Interactive elements — buttons, links, active indicators.

| Token | Hex | Primitive alias | Usage |
|---|---|---|---|
| `action-brand/primary` | `#0073E5` | `clr-royal/50 (base)` | Primary button fill, CTA background |
| `action-brand/primary-hover` | `#0053B2` | `clr-royal/40` | Primary button hover state |
| `action-brand/primary-text` | `#0073E5` | `clr-royal/50 (base)` | Link text, interactive text color |
| `action-brand/primary-border` | `#0073E5` | `clr-royal/50 (base)` | Focused input border, active indicator border |

---

## Surface

Background layers and container fills.

| Token | Hex | Primitive alias | Usage |
|---|---|---|---|
| `surface/default` | `#F2F6FC` | `clr-neutral/95` | Page background, main canvas |
| `surface/subtle` | `#F9FBFE` | `clr-neutral/98` | Card inner areas, description sections |
| `surface/elevated` | `#E1E8F5` | `clr-neutral/90` | Elevated surfaces, dividers, skeleton base |
| `surface/disabled` | `#8497B8` | `clr-neutral/65` | Disabled surface fill |

---

## Text

All text across the product.

| Token | Hex | Primitive alias | Usage |
|---|---|---|---|
| `text/primary` | `#334466` | `clr-neutral/40` | Headings, labels, primary body text |
| `text/secondary` | `#627494` | `clr-neutral/55` | Descriptions, captions, placeholder text |
| `text/disabled` | `#8497B8` | `clr-neutral/65` | Disabled input text, greyed labels |

---

## Status

Feedback and notification states.

| Token | Hex | Primitive alias | Usage |
|---|---|---|---|
| `status/error` | `#DC3838` | `clr-wine/50 (base)` | Error icon, error text, destructive action text |
| `status/error-bg` | `#FDEEEE` | `clr-wine/95` | Error toast background, error field tint |
| `status/error-border` | `#DC3838` | `clr-wine/50 (base)` | Error input border |
| `status/success` | `#246B2D` | `clr-pea/40` | Success icon, success text |
| `status/success-bg` | `#EEFCED` | `clr-pea/95` | Success toast background, success field tint |
| `status/warning` | `#8F5A00` | `clr-gold/20 (base)` | Warning text (dark, for contrast on light bg) |
| `status/warning-bg` | `#FFF8EB` | `clr-gold/95` | Warning toast background, warning field tint |
| `status/info` | `#007BA8` | `clr-sky/40 (base)` | Info icon, info text |
| `status/info-strong` | `#005B80` | `clr-sky/30` | Stronger info variant for emphasis |

---

## Focus

Keyboard navigation and accessibility.

| Token | Hex | Primitive alias | Usage |
|---|---|---|---|
| `focus/ring` | `#97AAC7` | `clr-neutral/70` | Focus ring on interactive elements |

---

## CSS Custom Properties

```css
:root {
  /* Action / Brand */
  --action-brand-primary:        #0073E5;
  --action-brand-primary-hover:  #0053B2;
  --action-brand-primary-text:   #0073E5;
  --action-brand-primary-border: #0073E5;

  /* Surface */
  --surface-default:   #F2F6FC;
  --surface-subtle:    #F9FBFE;
  --surface-elevated:  #E1E8F5;
  --surface-disabled:  #8497B8;

  /* Text */
  --text-primary:    #334466;
  --text-secondary:  #627494;
  --text-disabled:   #8497B8;

  /* Status */
  --status-error:          #DC3838;
  --status-error-bg:       #FDEEEE;
  --status-error-border:   #DC3838;
  --status-success:        #246B2D;
  --status-success-bg:     #EEFCED;
  --status-warning:        #8F5A00;
  --status-warning-bg:     #FFF8EB;
  --status-info:           #007BA8;
  --status-info-strong:    #005B80;

  /* Focus */
  --focus-ring: #97AAC7;
}
```
