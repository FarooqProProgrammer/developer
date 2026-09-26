# Modern Solid Styling Recipes (Tailwind CSS v4)

Snippets and CSS patterns for modern UI visual polish using **Tailwind CSS v4** with **solid colors only (no gradients)**.

---

## 1. Clean Frosted & Solid Layered Surfaces

Achieve high-end contrast with translucent solid backdrops and crisp hairline borders without any background gradients.

```html
<!-- Translucent Solid Card -->
<div class="rounded-2xl bg-neutral-900/80 backdrop-blur-md border border-neutral-800 p-6 shadow-xl shadow-black/20">
  <h4 class="text-white font-semibold text-base">Solid Surface Card</h4>
  <p class="text-neutral-400 text-sm mt-1">Frosted solid backdrop with crisp hairline border.</p>
</div>

<!-- Layered Solid Panels -->
<div class="rounded-2xl bg-neutral-950 border border-neutral-800 p-6 space-y-4">
  <div class="flex items-center justify-between border-b border-neutral-800 pb-3">
    <span class="text-xs font-mono uppercase tracking-wider text-neutral-400">Environment</span>
    <span class="px-2 py-0.5 rounded text-xs font-mono bg-emerald-500/10 text-emerald-400 border border-emerald-500/20">Production</span>
  </div>
  <div class="rounded-xl bg-neutral-900 border border-neutral-800/80 p-4 font-mono text-xs text-neutral-300">
    <code>DEPLOY_TARGET=global-edge-01</code>
  </div>
</div>
```

---

## 2. Crisp Hairline Borders & High-Contrast Dividing

Use solid hairline borders to define distinct component sections without relying on gradient strokes.

```html
<div class="rounded-2xl bg-neutral-900 border border-neutral-800 divide-y divide-neutral-800 overflow-hidden shadow-sm">
  <div class="p-4 flex items-center justify-between">
    <span class="text-sm font-medium text-white">Automated Backups</span>
    <span class="text-xs font-mono text-neutral-400">Daily at 00:00 UTC</span>
  </div>
  <div class="p-4 flex items-center justify-between">
    <span class="text-sm font-medium text-white">SSL Certificates</span>
    <span class="text-xs font-mono text-emerald-400">Active</span>
  </div>
</div>
```

---

## 3. Micro-Interactions & Custom Utilities (Tailwind v4 `@utility`)

```css
@import "tailwindcss";

@utility card-hover {
  transition: transform 0.2s cubic-bezier(0.16, 1, 0.3, 1), box-shadow 0.2s cubic-bezier(0.16, 1, 0.3, 1), border-color 0.2s ease;
  &:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 16px -4px rgba(0, 0, 0, 0.2);
    border-color: var(--color-neutral-700);
  }
}
```

---

## 4. Scrollbar Styling (Solid Neutral)

```css
/* Sleek solid custom scrollbars */
::-webkit-scrollbar {
  width: 6px;
  height: 6px;
}

::-webkit-scrollbar-track {
  background: transparent;
}

::-webkit-scrollbar-thumb {
  background: rgba(150, 150, 150, 0.2);
  border-radius: 9999px;
}

::-webkit-scrollbar-thumb:hover {
  background: rgba(150, 150, 150, 0.4);
}
```
