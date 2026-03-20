# Semantic Colors

Semantic tokens are named by **purpose**, not visual appearance. They are aliases pointing to specific [primitive color](/foundations/primitive-colors) steps. Always use semantic tokens in component code — never reference primitives directly.

**Source:** `semantic.json` — Figma variable collection "Semantic Colors"

---

## Action / Brand — interactive elements: buttons, links, active indicators

| Swatch | Token | Hex | Primitive alias |
|---|---|---|---|
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#0073E5;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#0073E5` | `action-brand/primary` | `#0073E5` | `clr-royal/50 (base)` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#0053B2;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#0053B2` | `action-brand/primary-hover` | `#0053B2` | `clr-royal/40` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#0073E5;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#0073E5` | `action-brand/primary-text` | `#0073E5` | `clr-royal/50 (base)` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#0073E5;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#0073E5` | `action-brand/primary-border` | `#0073E5` | `clr-royal/50 (base)` |

## Surface — background layers and container fills

| Swatch | Token | Hex | Primitive alias |
|---|---|---|---|
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#F2F6FC;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#F2F6FC` | `surface/default` | `#F2F6FC` | `clr-neutral/95` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#F9FBFE;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#F9FBFE` | `surface/subtle` | `#F9FBFE` | `clr-neutral/98` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#E1E8F5;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#E1E8F5` | `surface/elevated` | `#E1E8F5` | `clr-neutral/90` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#8497B8;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#8497B8` | `surface/disabled` | `#8497B8` | `clr-neutral/65` |

## Text — all text across the product

| Swatch | Token | Hex | Primitive alias |
|---|---|---|---|
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#334466;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#334466` | `text/primary` | `#334466` | `clr-neutral/40` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#627494;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#627494` | `text/secondary` | `#627494` | `clr-neutral/55` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#8497B8;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#8497B8` | `text/disabled` | `#8497B8` | `clr-neutral/65` |

## Status — feedback and notification states

| Swatch | Token | Hex | Primitive alias |
|---|---|---|---|
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#DC3838;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#DC3838` | `status/error` | `#DC3838` | `clr-wine/50 (base)` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#FDEEEE;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#FDEEEE` | `status/error-bg` | `#FDEEEE` | `clr-wine/95` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#DC3838;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#DC3838` | `status/error-border` | `#DC3838` | `clr-wine/50 (base)` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#246B2D;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#246B2D` | `status/success` | `#246B2D` | `clr-pea/40` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#EEFCED;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#EEFCED` | `status/success-bg` | `#EEFCED` | `clr-pea/95` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#8F5A00;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#8F5A00` | `status/warning` | `#8F5A00` | `clr-gold/20 (base)` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#FFF8EB;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#FFF8EB` | `status/warning-bg` | `#FFF8EB` | `clr-gold/95` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#007BA8;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#007BA8` | `status/info` | `#007BA8` | `clr-sky/40 (base)` |
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#005B80;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#005B80` | `status/info-strong` | `#005B80` | `clr-sky/30` |

## Focus — keyboard navigation and accessibility

| Swatch | Token | Hex | Primitive alias |
|---|---|---|---|
| <span style="display:inline-block;width:16px;height:16px;border-radius:3px;background:#97AAC7;vertical-align:middle;margin-right:8px;border:1px solid rgba(0,0,0,0.1)"></span>`#97AAC7` | `focus/ring` | `#97AAC7` | `clr-neutral/70` |

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