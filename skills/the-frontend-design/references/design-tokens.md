# Design Tokens Reference (Tailwind CSS v4)

A standardized design token architecture for building cohesive, scalable interfaces using **Tailwind CSS v4**.

---

## 1. Tailwind v4 `@theme` Configuration (CSS-First)

In Tailwind CSS v4, all theme tokens, fonts, custom colors, animations, and shadows are defined in CSS using the `@theme` directive. There are **no** `tailwind.config.js` or `tailwind.config.ts` files.

### `globals.css` / `app.css`

```css
@import "tailwindcss";

@theme {
  /* Font Families */
  --font-sans: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --font-display: "Cabinet Grotesk", "Inter", sans-serif;
  --font-mono: "JetBrains Mono", monospace;

  /* Custom OKLCH Color Palette */
  --color-brand-50: oklch(0.97 0.015 250);
  --color-brand-100: oklch(0.93 0.04 250);
  --color-brand-200: oklch(0.86 0.08 250);
  --color-brand-500: oklch(0.60 0.20 250);
  --color-brand-600: oklch(0.52 0.22 250);
  --color-brand-700: oklch(0.44 0.20 250);

  /* Semantic Theme Variables mapped to utilities */
  --color-surface-canvas: oklch(0.985 0.002 247);
  --color-surface-card: oklch(1 0 0);
  --color-surface-subtle: oklch(0.96 0.005 247);
  --color-border-subtle: oklch(0.92 0.005 247);
  --color-border-default: oklch(0.88 0.01 247);

  /* Elevation Shadows */
  --shadow-subtle: 0 1px 2px 0 rgb(0 0 0 / 0.05);
  --shadow-card: 0 4px 6px -1px rgb(0 0 0 / 0.07), 0 2px 4px -2px rgb(0 0 0 / 0.05);
  --shadow-overlay: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.05);
}

/* Dark Mode Overrides for Tailwind v4 */
@layer base {
  .dark {
    --color-surface-canvas: oklch(0.14 0.005 247);
    --color-surface-card: oklch(0.18 0.005 247);
    --color-surface-subtle: oklch(0.22 0.008 247);
    --color-border-subtle: oklch(0.24 0.008 247);
    --color-border-default: oklch(0.28 0.01 247);
  }
}
```

---

## 2. Spacing System (8pt Base Grid)

All layout dimensions, margins, paddings, and gaps align directly to Tailwind v4 utility classes.

| Token | Pixels | Rem | Tailwind v4 Utility | Primary Usage |
|---|---|---|---|---|
| `space-1` | 4px | 0.25rem | `p-1`, `gap-1`, `m-1` | Micro-spacing, badge padding, compact gap |
| `space-2` | 8px | 0.5rem | `p-2`, `gap-2`, `m-2` | Button inner padding (Y), tight form spacing |
| `space-3` | 12px | 0.75rem | `p-3`, `gap-3`, `m-3` | Input padding, compact card padding |
| `space-4` | 16px | 1.0rem | `p-4`, `gap-4`, `m-4` | Standard component padding, standard gap |
| `space-6` | 24px | 1.5rem | `p-6`, `gap-6`, `m-6` | Card padding, section gaps |
| `space-8` | 32px | 2.0rem | `p-8`, `gap-8`, `m-8` | Modal padding, grid gutter |
| `space-12` | 48px | 3.0rem | `p-12`, `gap-12`, `m-12` | Page section dividers |
| `space-16` | 64px | 4.0rem | `p-16`, `gap-16`, `m-16` | Hero section padding, layout margins |

---

## 3. Typography Ramp (Tailwind v4)

| Token | Size / Line Height | Tailwind v4 Class Combo | Typical Usage |
|---|---|---|---|
| `text-xs` | 12px / 16px | `text-xs leading-4` | Captions, badges, timestamps |
| `text-sm` | 14px / 20px | `text-sm leading-5` | Form labels, helper text, secondary info |
| `text-base` | 16px / 24px | `text-base leading-6` | Default body copy, inputs, table rows |
| `text-lg` | 18px / 28px | `text-lg font-semibold leading-7` | Card titles, subheadings |
| `text-xl` | 20px / 28px | `text-xl font-semibold leading-7` | Section headers, panel titles |
| `text-2xl` | 24px / 32px | `text-2xl font-bold leading-8 tracking-tight` | Subsection headers, dialog titles |
| `text-3xl` | 30px / 36px | `text-3xl font-bold leading-9 tracking-tight` | Page titles, key dashboard metrics |
| `text-4xl` | 36px / 40px | `text-4xl font-extrabold tracking-tight` | Marketing hero headers |

---

## 4. Tailwind v4 Border Radii

- `rounded-sm` (2px–4px): Small badges, status tags.
- `rounded-md` (6px): Input fields, action buttons.
- `rounded-lg` (8px): Standard cards, dialog windows.
- `rounded-xl` / `rounded-2xl` (12px–16px): Large feature containers, Bento grid cards.
- `rounded-full` (9999px): Avatars, pill status badges.
