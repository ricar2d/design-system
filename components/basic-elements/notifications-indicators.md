# Notifications & Indicators

**Purpose:** System-level feedback — growl toasts, progress bars, spinners.

**Anatomy (Toast/Growl):**
- Container (rounded, shadowed)
- Icon (status indicator)
- Title + description
- Close button
- Auto-dismiss timer (optional)

**Anatomy (Progress bar):**
- Track (background)
- Fill (progress indication)
- Label (percentage or step)

**Anatomy (Spinner):**
- Animated circular indicator

**Variants:**
- Toast: Success, Error, Warning, Info
- Progress: Linear bar, circular
- Spinner: SM, MD, LG

**Token dependencies:**
- `clr-royal/50` — info / progress fill
- `clr-wine/50` — error toast
- `clr-gold/60` — warning toast
- `global/white` — toast background
- `shadow-card` — toast elevation

---
