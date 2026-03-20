# Colors

The color system is organized in three layers. Start with primitives, build semantics, use semantics in components.

| Layer | File | Purpose |
|---|---|---|
| [Primitive Colors](foundations/primitive-colors.md) | `Primitive_colors.json` | Raw color ramps — 13 families, ~150 steps |
| [Semantic Colors](foundations/semantic-colors.md) | `semantic.json` | Purpose-named aliases: `text/primary`, `status/error`, `surface/default` |
| [Chart Colors](foundations/chart-colors.md) | `chart_Colors.json` | 5 data visualization palettes |

## The rule

Use **semantic tokens** in all component and layout code. Only reference primitives when defining new semantic tokens.

```css
/* ✅ Correct */
color: var(--text-primary);

/* ❌ Wrong — primitives in component code */
color: var(--clr-neutral-40);
```
