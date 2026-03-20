# Semantic Colors

Semantic tokens are named by **purpose**, not visual appearance. They alias specific primitive steps. Always reference these in component code — never primitives directly.

---

## Action / Brand

Interactive elements — buttons, links, active indicators.

| | Token | Hex | Primitive alias |
|:---:|---|---|---|
| ![](../../.gitbook/assets/swatch-0073E5.svg) | `action-brand/primary` | `#0073E5` | `clr-royal/50 (base)` |
| ![](../../.gitbook/assets/swatch-0053B2.svg) | `action-brand/primary-hover` | `#0053B2` | `clr-royal/40` |
| ![](../../.gitbook/assets/swatch-0073E5.svg) | `action-brand/primary-text` | `#0073E5` | `clr-royal/50 (base)` |
| ![](../../.gitbook/assets/swatch-0073E5.svg) | `action-brand/primary-border` | `#0073E5` | `clr-royal/50 (base)` |

## Surface

Background layers and container fills.

| | Token | Hex | Primitive alias |
|:---:|---|---|---|
| ![](../../.gitbook/assets/swatch-F2F6FC.svg) | `surface/default` | `#F2F6FC` | `clr-neutral/95` |
| ![](../../.gitbook/assets/swatch-F9FBFE.svg) | `surface/subtle` | `#F9FBFE` | `clr-neutral/98` |
| ![](../../.gitbook/assets/swatch-E1E8F5.svg) | `surface/elevated` | `#E1E8F5` | `clr-neutral/90` |
| ![](../../.gitbook/assets/swatch-8497B8.svg) | `surface/disabled` | `#8497B8` | `clr-neutral/65` |

## Text

All text across the product.

| | Token | Hex | Primitive alias |
|:---:|---|---|---|
| ![](../../.gitbook/assets/swatch-334466.svg) | `text/primary` | `#334466` | `clr-neutral/40` |
| ![](../../.gitbook/assets/swatch-627494.svg) | `text/secondary` | `#627494` | `clr-neutral/55` |
| ![](../../.gitbook/assets/swatch-8497B8.svg) | `text/disabled` | `#8497B8` | `clr-neutral/65` |

## Status

Feedback and notification states.

| | Token | Hex | Primitive alias |
|:---:|---|---|---|
| ![](../../.gitbook/assets/swatch-DC3838.svg) | `status/error` | `#DC3838` | `clr-wine/50 (base)` |
| ![](../../.gitbook/assets/swatch-FDEEEE.svg) | `status/error-bg` | `#FDEEEE` | `clr-wine/95` |
| ![](../../.gitbook/assets/swatch-DC3838.svg) | `status/error-border` | `#DC3838` | `clr-wine/50 (base)` |
| ![](../../.gitbook/assets/swatch-246B2D.svg) | `status/success` | `#246B2D` | `clr-pea/40` |
| ![](../../.gitbook/assets/swatch-EEFCED.svg) | `status/success-bg` | `#EEFCED` | `clr-pea/95` |
| ![](../../.gitbook/assets/swatch-8F5A00.svg) | `status/warning` | `#8F5A00` | `clr-gold/20 (base)` |
| ![](../../.gitbook/assets/swatch-FFF8EB.svg) | `status/warning-bg` | `#FFF8EB` | `clr-gold/95` |
| ![](../../.gitbook/assets/swatch-007BA8.svg) | `status/info` | `#007BA8` | `clr-sky/40 (base)` |
| ![](../../.gitbook/assets/swatch-005B80.svg) | `status/info-strong` | `#005B80` | `clr-sky/30` |

## Focus

Keyboard navigation and accessibility.

| | Token | Hex | Primitive alias |
|:---:|---|---|---|
| ![](../../.gitbook/assets/swatch-97AAC7.svg) | `focus/ring` | `#97AAC7` | `clr-neutral/70` |

---

## CSS Custom Properties

```css
:root {
  /* action-brand */
  --action-brand-primary: #0073E5;
  --action-brand-primary-hover: #0053B2;
  --action-brand-primary-text: #0073E5;
  --action-brand-primary-border: #0073E5;

  /* surface */
  --surface-default: #F2F6FC;
  --surface-subtle: #F9FBFE;
  --surface-elevated: #E1E8F5;
  --surface-disabled: #8497B8;

  /* text */
  --text-primary: #334466;
  --text-secondary: #627494;
  --text-disabled: #8497B8;

  /* status */
  --status-error: #DC3838;
  --status-error-bg: #FDEEEE;
  --status-error-border: #DC3838;
  --status-success: #246B2D;
  --status-success-bg: #EEFCED;
  --status-warning: #8F5A00;
  --status-warning-bg: #FFF8EB;
  --status-info: #007BA8;
  --status-info-strong: #005B80;

  /* focus */
  --focus-ring: #97AAC7;

}
```