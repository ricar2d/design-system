# Inline Editing Pattern

**Used in:** Table cells, record field values, card content.

**Structure:**
```
[Field value — display mode]
  └── Click/hover → [Field value — edit mode]
        ├── Input (Basic) or Select
        └── Save / Cancel inline actions
```

**Key behaviors:**
- Click field value to enter edit mode
- `Enter` or blur to save
- `Escape` to cancel
- Input style switches from display text to `Input (Line)` style
- Save/cancel appear as small inline icon buttons

**Token dependencies:**
- Display text: `clr-neutral/40`
- Edit mode input: `Input (Line)` component
- Save: `clr-royal/50` (`Icon=check`)
- Cancel: `clr-neutral/55` (`Icon=x`)

---
