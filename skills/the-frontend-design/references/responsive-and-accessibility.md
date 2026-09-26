# Responsive Design & Accessibility (a11y)

Guidelines to ensure interfaces are universally accessible, keyboard operable, and adapt smoothly across all viewport sizes.

---

## 1. Responsive Breakpoint Strategy

Design mobile-first. Default styles apply to mobile viewports, with minimum-width queries expanding the layout.

| Breakpoint | Minimum Width | Target Devices | Typical Layout Strategy |
|---|---|---|---|
| `sm` | 640px | Large phones / small phablets | 1-2 columns, compact headers |
| `md` | 768px | Tablets / iPad portrait | 2 columns, visible sidebar toggle |
| `lg` | 1024px | Laptops / iPad landscape | 3 columns, persistent sidebar, expanded tables |
| `xl` | 1280px | Desktops | 4 columns, max-width containers (`max-w-7xl`) |
| `2xl` | 1536px | Large monitors | Centered container with balanced negative margins |

### Mobile Touch Targets
- Minimum touch target size: **44px × 44px** (or 48px × 48px for material standards).
- Always ensure adequate spacing between adjacent buttons or clickable elements to prevent accidental taps.

---

## 2. Accessibility (WCAG 2.1 AA Checklist)

### 1. Color Contrast & Visual Indicators
- **Normal text (<18pt or <14pt bold)**: Minimum **4.5:1** contrast against background.
- **Large text (>=18pt or >=14pt bold)**: Minimum **3.0:1** contrast.
- **UI Components & Borders**: Minimum **3.0:1** contrast against adjacent backgrounds.
- Never rely on color alone to convey meaning (e.g. validation errors must include clear descriptive text alongside color changes).

### 2. Semantic HTML & Heading Hierarchy
- Use proper landmark tags: `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`.
- Maintain a logical heading hierarchy (`<h1> -> <h2> -> <h3>`). Do not skip levels for visual sizing (use CSS classes for size instead).
- Use native interactive HTML elements (`<button>`, `<a>`, `<input>`, `<select>`) whenever possible instead of clickable `<div>` elements.

### 3. Keyboard Navigation & Focus Indicators
- Every interactive element must be reachable and operable via keyboard (`Tab`, `Shift+Tab`, `Enter`, `Space`, arrow keys).
- **Never suppress focus styles** with `outline: none` without providing an accessible replacement:
  ```css
  /* High visibility focus ring */
  :focus-visible {
    outline: 2px solid var(--brand-primary);
    outline-offset: 2px;
  }
  ```
- Modals and drawers must trap focus inside while open and return focus to the trigger element when closed.
- Pressing `Escape` must close any active modal, popover, or dropdown menu.

### 4. Text-First Design & Screen Reader Support
- **Prefer Explicit Text**: Label buttons with clear descriptive words (e.g. "Delete", "Settings", "Edit") rather than ambiguous icons.
- **Icon-Only Controls (When strictly necessary)**: Always provide an `aria-label` or visually hidden screen reader text:
  ```html
  <button aria-label="Close dialog" class="...">
    <span aria-hidden="true">&times;</span>
  </button>
  ```
- **Live Regions**: Announce dynamic updates (like form errors or toast messages) with `aria-live="polite"`.
- **Expanded States**: Use `aria-expanded="true|false"` on accordions and collapsible triggers.

---

## 3. Motion & Reduced Motion

Always respect user preferences for reduced motion:

```css
@media (prefers-reduced-motion: reduce) {
  *, ::before, ::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

In Tailwind:
```html
<div class="transition-transform duration-300 motion-reduce:transition-none hover:scale-105 motion-reduce:hover:scale-100">
  ...
</div>
```
