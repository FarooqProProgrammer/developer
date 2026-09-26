# Component & Layout Patterns

Practical guidelines and code patterns for essential modern UI components, prioritizing typography, whitespace, and clean structure over icon-heavy interfaces.

---

## Iconography Rules: Restraint & Purpose

1. **Text First**: Clear, concise labels are always superior to ambiguous icons. Do not prepend icons to standard buttons, nav items, or table headers.
2. **Avoid "Icon Soup"**: An interface filled with 20 different icon badges creates visual noise and cognitive fatigue.
3. **When Icons Are Justified**:
   - Universal utility controls where screen real estate is tight (e.g. search magnifying glass in search inputs, close 'x' in modal dialogs).
   - Directional disclosures (e.g. dropdown chevrons, accordion indicators).
   - Essential status badges where color + concise text is insufficient.

---

## 1. Bento Grid Pattern (Content & Typography Driven)

Bento grids showcase multiple features or metrics in an asymmetrical, visually dynamic layout using typography and data hierarchy instead of decorative icon stamps.

```html
<div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-4 max-w-7xl mx-auto p-4">
  <!-- Feature 1: Wide Hero Card (Spans 2 columns) -->
  <div class="md:col-span-2 rounded-2xl bg-neutral-900 border border-neutral-800 p-6 flex flex-col justify-between overflow-hidden relative group">
    <div class="z-10">
      <span class="text-xs font-semibold uppercase tracking-wider text-blue-400">Core Engine</span>
      <h3 class="text-2xl font-bold text-white mt-2">Real-time Analytics Engine</h3>
      <p class="text-neutral-400 text-sm mt-1 max-w-md">Process millions of events with sub-millisecond latency.</p>
    </div>
    <!-- Visual data representation -->
    <div class="mt-8 h-48 bg-neutral-950/60 rounded-xl border border-neutral-800/80 p-4 flex flex-col justify-between font-mono text-xs text-neutral-400">
      <div class="flex justify-between border-b border-neutral-800 pb-2 text-neutral-300">
        <span>REGION</span>
        <span>LATENCY</span>
        <span>STATUS</span>
      </div>
      <div class="flex justify-between">
        <span>us-east-1</span>
        <span class="text-emerald-400">12ms</span>
        <span class="text-emerald-400">ACTIVE</span>
      </div>
      <div class="flex justify-between">
        <span>eu-central-1</span>
        <span class="text-emerald-400">18ms</span>
        <span class="text-emerald-400">ACTIVE</span>
      </div>
      <div class="flex justify-between">
        <span>ap-southeast-1</span>
        <span class="text-emerald-400">24ms</span>
        <span class="text-emerald-400">ACTIVE</span>
      </div>
    </div>
  </div>

  <!-- Feature 2: Metric Stat Card -->
  <div class="rounded-2xl bg-neutral-900 border border-neutral-800 p-6 flex flex-col justify-between">
    <div>
      <span class="text-xs font-medium text-neutral-400">Total Throughput</span>
      <div class="text-3xl font-extrabold text-white mt-2 tracking-tight">99.99%</div>
      <p class="text-emerald-400 text-xs font-medium mt-1">
        +0.12% vs last 30 days
      </p>
    </div>
    <div class="h-20 bg-neutral-950/50 rounded-lg flex items-end p-2 gap-1 border border-neutral-800/40">
      <div class="bg-blue-500/80 w-full h-[40%] rounded-sm"></div>
      <div class="bg-blue-500/80 w-full h-[65%] rounded-sm"></div>
      <div class="bg-blue-500/80 w-full h-[85%] rounded-sm"></div>
      <div class="bg-blue-500/80 w-full h-[100%] rounded-sm"></div>
    </div>
  </div>

  <!-- Feature 3: Clean Feature Card -->
  <div class="rounded-2xl bg-neutral-900 border border-neutral-800 p-6 flex flex-col justify-between">
    <div>
      <span class="text-xs font-medium text-indigo-400 uppercase tracking-wider">Infrastructure</span>
      <h4 class="text-lg font-semibold text-white mt-2">Instant Edge Sync</h4>
      <p class="text-neutral-400 text-sm mt-1">Automatic replication across global edge locations with guaranteed consistency.</p>
    </div>
    <div class="pt-4 border-t border-neutral-800/80 flex items-center justify-between text-xs text-neutral-500">
      <span>Global cache</span>
      <span class="text-neutral-300 font-mono">300+ nodes</span>
    </div>
  </div>
</div>
```

---

## 2. Interactive Button Variants & States (Typography-First)

Buttons should rely on clear labels, distinct background/border styling, and responsive micro-interactions without unnecessary leading icons.

```html
<!-- Primary Action Button -->
<button class="px-4 py-2 rounded-lg font-medium text-sm text-white bg-blue-600 hover:bg-blue-500 active:scale-[0.98] focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-blue-500 focus-visible:ring-offset-2 transition-all duration-150 disabled:opacity-50 disabled:pointer-events-none shadow-sm">
  Deploy Project
</button>

<!-- Secondary / Surface Button -->
<button class="px-4 py-2 rounded-lg font-medium text-sm text-neutral-200 bg-neutral-800 hover:bg-neutral-700 border border-neutral-700 active:scale-[0.98] focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-neutral-400 focus-visible:ring-offset-2 transition-all duration-150 disabled:opacity-50">
  View Documentation
</button>

<!-- Ghost / Subtle Button -->
<button class="px-3 py-1.5 rounded-lg font-medium text-sm text-neutral-400 hover:text-neutral-100 hover:bg-neutral-800 active:scale-[0.98] transition-all">
  Cancel
</button>
```

---

## 3. Loading Skeletons & Clean Empty States

### Skeleton Loader (Zero Layout Shift)
```html
<div class="p-6 rounded-2xl bg-neutral-900 border border-neutral-800 animate-pulse space-y-4 max-w-sm">
  <div class="space-y-2">
    <div class="h-4 bg-neutral-800 rounded w-3/4"></div>
    <div class="h-3 bg-neutral-800 rounded w-1/2"></div>
  </div>
  <div class="space-y-2 pt-2">
    <div class="h-3 bg-neutral-800 rounded"></div>
    <div class="h-3 bg-neutral-800 rounded w-5/6"></div>
  </div>
</div>
```

### Clean Empty State (Content & Action Focused)
```html
<div class="text-center py-12 px-6 rounded-2xl border border-dashed border-neutral-800 bg-neutral-900/30 max-w-md mx-auto">
  <div class="inline-block px-2.5 py-1 rounded-full text-xs font-medium text-neutral-400 bg-neutral-800 border border-neutral-700">
    Workspace Empty
  </div>
  <h3 class="mt-4 text-base font-semibold text-neutral-100">No projects found</h3>
  <p class="mt-1.5 text-sm text-neutral-400 leading-relaxed">
    Get started by creating your first project or importing from an existing repository.
  </p>
  <div class="mt-6">
    <button class="px-4 py-2 rounded-lg bg-blue-600 hover:bg-blue-500 text-white text-sm font-medium transition shadow-sm">
      Create New Project
    </button>
  </div>
</div>
```

---

## 4. Modal / Dialog Pattern

```html
<div class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/60 backdrop-blur-sm" role="dialog" aria-modal="true" aria-labelledby="dialog-title">
  <div class="w-full max-w-md bg-neutral-900 border border-neutral-800 rounded-2xl p-6 shadow-2xl space-y-4 animate-in fade-in zoom-in-95 duration-200">
    <div class="flex items-center justify-between">
      <h3 id="dialog-title" class="text-lg font-semibold text-white">Create Workspace</h3>
      <button aria-label="Close dialog" class="text-neutral-400 hover:text-white px-2 py-1 rounded-md hover:bg-neutral-800 text-sm transition">
        Close
      </button>
    </div>
    <p class="text-sm text-neutral-400">Workspaces allow your team to collaborate on projects and manage configuration centrally.</p>
    <div class="space-y-3">
      <label class="block text-xs font-medium text-neutral-300">Workspace Name</label>
      <input type="text" placeholder="e.g. Acme Studio" class="w-full px-3 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-white placeholder-neutral-500 text-sm focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition" />
    </div>
    <div class="flex justify-end gap-3 pt-3">
      <button class="px-3 py-1.5 text-sm font-medium text-neutral-400 hover:text-white transition">Cancel</button>
      <button class="px-4 py-2 rounded-lg bg-blue-600 hover:bg-blue-500 text-white text-sm font-medium transition shadow-sm">Confirm</button>
    </div>
  </div>
</div>
```
