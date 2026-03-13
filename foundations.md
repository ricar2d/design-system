# Design System — Foundations

**Source libraries:** Pattern Library · Icons Library · Inputs & Controls Library
**Product:** OneHQ / PD (Product Design)
**Extracted:** 2026-03-13

---

## Overview

This design system serves a **CRM/productivity application** (OneHQ). The visual identity is clean, professional, and functional — modern SaaS with a corporate-blue primary palette, generous whitespace, and subtle card-based surfaces. All three Figma libraries share the same token set and visual language.

---

## Typography

**Font Family (single family):** `IBM Plex Sans`
All text across all three libraries uses this typeface exclusively.

| Role | Weight | Token (inferred) |
|---|---|---|
| Page titles / section headings | Medium 500 | `font-heading` |
| Body text / descriptions | Regular 400 | `font-body` |
| Interactive labels / links | Medium 500 | `font-label` |
| Rich text content | Bold 700 | `font-bold` (from icon set, inferred) |

> ⚠️ **Missing / recommended addition:** No explicit type scale (H1–H6, body-sm, caption, code) is formalized in any library. A scale should be defined — see `typography.md`.

---

## Color System

See `colors.md` for the full token inventory.

| Family | Prefix | Base hex | Role |
|---|---|---|---|
| Royal Blue | `clr-royal` | `#0073e5` | Primary, interactive, brand, links |
| Neutral Navy | `clr-neutral` | `#334466` | Headings, primary text |
| Neutral Mid | `clr-neutral` | `#627494` | Supporting text, subtitles |
| Wine / Red | `clr-wine` | `#dc3838` | Destructive, error states |
| Gold / Yellow | `clr-gold` | `#fdbe3f` | Warning, highlight |
| White | `global/white` | `#ffffff` | Surfaces, card backgrounds |
| Surface grey | *(inferred)* | `#f3f3f3` | Page/canvas background |
| Card inner grey | *(inferred)* | `#f9f9f9` | Card description areas |

---

## Spacing Scale

> **Inferred pattern** — No explicit spacing tokens exist in the libraries. Values are measured from component padding and gap properties.

| Token (inferred) | Value | Found in |
|---|---|---|
| `space-1` | 4px | Icon component gaps |
| `space-2` | 8px | Icon padding (12px grid gap) |
| `space-3` | 10px | Canvas gaps |
| `space-4` | 16px | Internal component padding |
| `space-5` | 20px | Description element gaps |
| `space-6` | 24px | *(inferred standard)* |
| `space-8` | 32px | *(inferred standard)* |
| `space-10` | 40px | *(inferred)* |
| `space-12` | 48px | Section header top padding |
| `space-16` | 64px | Icon library description padding |
| `space-20` | 76–80px | Card inner padding |
| `space-32` | 128px | Input card side padding |
| `space-40` | 140–180px | Component container padding |
| `space-54` | 215px | Page-level header padding |

---

## Border Radius

| Token (inferred) | Value | Found in |
|---|---|---|
| `radius-sm` | *(inferred ~6–8px)* | Small inputs, badges |
| `radius-md` | *(inferred ~12px)* | Inputs, dropdowns |
| `radius-lg` | `39px` | Option cards, component cards |
| `radius-xl` | `60px` | Page/canvas containers |
| `radius-2xl` | `80px` | Icon library component container |

> ✅ **Found in library:** `39px` (all option cards), `60px` (page frames), `80px` (icon container).

---

## Shadows / Elevation

| Name | Token | CSS Value |
|---|---|---|
| Shadow Mid | `Shadows/Mid` | `0 0 18px rgba(14,67,140,0.07)` |
| Shadow Card | *(inferred)* | `0 4px 23px rgba(22,88,197,0.06)` |

Both use the royal-blue/navy color family at very low opacity. The system has no harsh or dark shadows — all elevation is subtle and cool-tinted.

> ⚠️ **Missing / recommended addition:** `shadow-focus` for focused input rings, `shadow-none` for flat contexts.

---

## Opacity Overlays

White overlay values used for component backgrounds and image washes:

| Level | Value |
|---|---|
| 90% (heavy wash) | `rgba(255,255,255,0.9)` |
| 80% (standard) | `rgba(255,255,255,0.8)` |
| 70% (light) | `rgba(255,255,255,0.7)` |
| 60% (subtle) | `rgba(255,255,255,0.6)` |

---

## Motion Tokens

> ⚠️ **Missing / recommended addition:** No motion or animation tokens are defined in any library. Recommend formalizing: `duration-fast: 100ms`, `duration-default: 200ms`, `duration-slow: 300ms`, `easing: ease-in-out`.

---

## Design Principles (Inferred from libraries)

1. **Clarity over decoration** — No gradients, no textures. Shadows are almost invisible.
2. **Generous rounding** — Large radii (39px, 60px) create warmth in a data-heavy product.
3. **IBM Plex Sans as the single voice** — Strict mono-typeface discipline throughout.
4. **Royal blue as the sole interactive signal** — `#0073e5` handles all links, CTAs, focus states, and brand moments.
5. **Card-first composition** — Every surface is a white or near-white card on `#f3f3f3`.
6. **Navy–grey text hierarchy** — `#334466` (headings) → `#627494` (supporting text).
7. **CRM density awareness** — Layout patterns accommodate dense data grids, filters, and action-heavy surfaces.
