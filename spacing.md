# Spacing

**Source:** Inferred from all three libraries — no explicit spacing tokens are defined.

---

## Measured Spacing Values

### Micro / Component-level

| Value | Found in | Suggested token |
|---|---|---|
| 4px | Icon frame gaps | `space-1` |
| 8px | Icon symbol padding | `space-2` |
| 10px | Canvas gap between sections | `space-2.5` |
| 16px | *(standard inferred)* | `space-4` |
| 20px | Card description element gap | `space-5` |
| 24px | *(standard inferred)* | `space-6` |
| 36px | ** | `space-9` |

### Component padding

| Value | Found in | Suggested token |
|---|---|---|
| 48px | Section header vertical padding, card description padding | `space-12` |
| 76–80px | Card description horizontal padding, icon library head padding | `space-20` |
| 119px | Page frame top padding | `space-30` |
| 128px | Input card horizontal padding | `space-32` |
| 140px | Icon library container padding | `space-35` |
| 180px | Canvas content padding | `space-45` |
| 215px | Page section header horizontal padding | `space-54` |

### Layout / Canvas

| Value | Found in | Suggested token |
|---|---|---|
| 184px | Gap between option cards in grid | `space-46` |
| 180px | Card grid outer padding | `space-45` |

---

## Recommended Normalized Scale

Rather than mapping every arbitrary value, the system should adopt a **base-4 scale** which covers all observed values:

```
space-0  =  0px
space-1  =  4px
space-2  =  8px
space-3  =  12px
space-4  =  16px
space-5  =  20px
space-6  =  24px
space-8  =  32px
space-10 =  40px
space-12 =  48px
space-16 =  64px
space-20 =  80px
space-24 =  96px
space-32 =  128px
```

> Values above 128px (page-level padding of 180–215px) are layout-specific and should be handled as layout tokens, not spacing tokens.

---

## Component Spacing Patterns

### Card component
```
padding: 48px 76px     (description area)
gap:     20px          (between description elements)
```

### Option Card (index/catalog cards)
```
padding: 48px 76px     (label area)
inner image: 489px     (fixed height)
corner radius: 39px
```

### Page section header
```
padding: 119px 215px
gap: 48px              (between title and subtitle)
```

### Icon canvas grid
```
gap between icons:  4px (within frame)
padding:            8px
grid columns:       26 icons per row at 32px
```

---

## Issues Summary

| Issue | Severity | Action |
|---|---|---|
| No spacing tokens defined | High | Adopt base-4 scale |
| Arbitrary spacing values throughout | High | Map to nearest token value |
| No gap tokens for layout grids | Medium | Define layout spacing separately |
| `184px` card gap is non-standard | Low | Round to `space-46` or nearest grid unit |
