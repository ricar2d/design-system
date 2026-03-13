# Typography

**Source:** Pattern Library, Inputs & Controls Library, Icons Library  
**Typeface:** IBM Plex Sans (single family, all weights)

---

## Font Family

```css
font-family: 'IBM Plex Sans', sans-serif;
```

IBM Plex Sans is IBM's open-source humanist sans-serif. It carries a structured, technical character that suits a CRM/productivity product. It is highly legible at small sizes and carries both Regular and Medium weights across all components.

---

## Weights Found in Libraries

| Weight | Value | CSS Class (Figma output) |
|---|---|---|
| Regular | 400 | `font-['IBM_Plex_Sans:Regular',sans-serif]` |
| Medium | 500 | `font-['IBM_Plex_Sans:Medium',sans-serif]` |
| Bold | 700 | *(inferred — Bold icon present in icon set)* |

> ✅ **Found in library:** Regular and Medium are used throughout all components.
> ⚠️ **Inferred pattern:** Bold (700) is present in the icon library (`Icon=bold`, `Icon=italic`, `Icon=underline`) indicating rich-text editor support, but Bold weight is not found in system-level components.

---

## Type Scale (Inferred — not formally defined in libraries)

The following scale is measured from Figma frame dimensions and relative sizing within components. Values are in the Figma canvas coordinate system (at approximately 2× scale from actual px).

> ⚠️ **Important note:** The Figma files appear to use a high-DPI canvas (components are laid out at ~2× screen scale). The text sizes below reflect raw Figma values. Actual rendered sizes should be divided by approximately 2 for standard screen implementation.

| Role | Figma value | Estimated screen px | Weight | Token (recommended) |
|---|---|---|---|---|
| Page section title | 171px | ~24px | Medium | `text-page-title` |
| Component/card title | 80px | ~14–16px | Medium | `text-component-title` |
| Body / description | 91px | ~16px | Regular | `text-body` |
| Supporting / subtitle | 44px | ~12px | Regular | `text-caption` |
| Icon label text | 64–80px | ~14px | Regular | `text-label` |
| Header text (Icon lib) | 112px | ~20px | Regular | `text-header` |

> ⚠️ **Missing / recommended addition:** No formal type scale with named tokens exists in any library. The system needs a documented scale for consistent implementation. The above is derived from measured values and should be verified against the running application.

---

## Line Height

| Context | Value found | Notes |
|---|---|---|
| Default block text | `leading-[normal]` | Browser default (~1.2–1.4) |
| Icon library description | `leading-[95px]` | Large canvas scale |
| Component labels | `leading-[0]` with nested `leading-[normal]` | Collapsed container with internal reset |

> ⚠️ **Inconsistency:** Line height is inconsistently applied. Some elements use `leading-[normal]`, others use explicit pixel values. A semantic set of `line-height` tokens would improve consistency.

---

## Text Color Usage

| Color | Token | Typical role |
|---|---|---|
| `#334466` | `clr-neutral/40` | Headings, section titles, primary labels |
| `#627494` | `clr-neutral/55` | Descriptions, subtitles, placeholder |
| `#0073e5` | `clr-royal/50` | Links, interactive text, CTA labels |
| `#ffffff` | `global/white` | Text on colored backgrounds |

---

## Text Decoration

- Links use `underline` + `decoration-solid` + `[text-decoration-skip-ink:none]`
- Active/interactive links: `cursor-pointer`
- No `text-transform` (uppercase/lowercase) found — titles use natural case

---

## Recommended Token Set

```css
:root {
  --font-family-base: 'IBM Plex Sans', sans-serif;
  --font-weight-regular: 400;
  --font-weight-medium: 500;
  --font-weight-bold: 700;

  /* Type scale — verify against running app */
  --text-page-title:       24px / 1.2  Medium;
  --text-section-heading:  20px / 1.3  Medium;
  --text-component-title:  16px / 1.3  Medium;
  --text-body:             14px / 1.5  Regular;
  --text-label:            14px / 1.2  Medium;
  --text-caption:          12px / 1.4  Regular;
  --text-link:             14px / 1.3  Medium;
}
```

---

## Issues Summary

| Issue | Severity | Action |
|---|---|---|
| No formal type scale defined | High | Define and document scale with tokens |
| Canvas scale vs screen scale ambiguity | High | Verify actual rendered sizes in app |
| Inconsistent line-height usage | Medium | Define `line-height` tokens per role |
| Bold weight present in icons but not used in UI | Low | Decide if bold weight is needed in text |
