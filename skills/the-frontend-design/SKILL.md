---
name: the-frontend-design
description: Comprehensive frontend UI/UX design and implementation system using Tailwind CSS v4 and anti-AI-slop quality discipline. Use when designing, styling, structuring, auditing, or refining modern user interfaces, responsive layouts, design tokens, typography, and component architectures.
---

# The Frontend Design (Tailwind CSS v4 & Anti-Slop Discipline)

Comprehensive frontend UI/UX engineering discipline for creating bespoke, production-grade, accessible, and responsive interfaces that refuse to look like generic AI templates. Powered strictly by **Tailwind CSS v4** and **Inspo MCP**.

## Core Philosophy

1. **Strictly Tailwind CSS v4 (CSS-First)**: All styling, layouts, typography ramps, responsive breakpoints, animations, and interactive component states **MUST** be implemented using **Tailwind CSS v4** (`@import "tailwindcss";` and `@theme` CSS tokens). No legacy `tailwind.config.js/ts` files and no raw inline styles.
2. **Zero Gradients Rule**: **Never use gradients anywhere**—no gradient text (`bg-clip-text`), no gradient backgrounds (`bg-gradient-to-...`), no gradient borders, and no aurora/mesh gradient blobs. Rely strictly on solid ink typography, clean tinted solid surfaces (`oklch`), subtle solid dividers, and depth via solid elevation.
3. **Typography-First & Restrained Iconography**: Never add decorative icons indiscriminately. Rely on strong typographic hierarchy, clean borders, and whitespace. Use icons only when they serve a clear functional purpose (e.g. search input indicator, modal close button, directional chevron).
4. **Distinct Macrostructures for Distinct Briefs**: Never emit the same centered template twice. Match each brief to a deliberate structural shape (Bento Grid, Split Studio, Marquee Hero, Stat-Led, Long Document, Workbench).
5. **Real-World Reference & Taste via Inspo MCP**: Query Inspo MCP (`https://inspomcp.dev/`) to study real production exemplars, extract validated design systems (`DESIGN.md`), and inspect canonical reference components before building.
6. **State Completeness**: Every component must handle every state: default, hover, active, focus, disabled, loading, empty, and error using Tailwind v4 variants (`hover:`, `focus-visible:`, `active:`, `disabled:`).
7. **Accessible by Default**: Accessibility (WCAG 2.1 AA+) is foundational—it drives semantic markup, keyboard focus management, and color contrast.
8. **Fluid Responsiveness**: Interfaces must feel native across mobile (`sm:`), tablet (`md:`), desktop (`lg:`, `xl:`), and ultra-wide screens.

---

## The Four Frontend Actions

| Action | Purpose |
|---|---|
| **Build (Default)** | Create new UI. Query Inspo, select a distinct macrostructure, apply Tailwind v4 solid tokens, and run the anti-slop check. |
| **Audit** | Score existing code against named anti-patterns (gradients, icon overload, card nesting, contrast fails) with actionable fixes. |
| **Redesign** | Preserve copy, brand identity, and IA, but switch to a completely different macrostructure to eliminate AI-template fatigue. |
| **Study** | Query Inspo MCP for a given URL or aesthetic to extract design DNA: solid palette tokens, typography ramp, and structural layout. |

---

## 5-Step UI Construction Workflow

```
0. Inspo Discovery -> 1. Select Macrostructure -> 2. Semantic IA & Spacing -> 3. Solid Visual Tokens (Tailwind v4 @theme) -> 4. Component States -> 5. Anti-Slop Audit
```

### 0. Inspo Discovery & Exemplar Study
- Call Inspo MCP: `inspo:recommend({ brief })` or `inspo:search_screens({ query })` to study real production layouts and extract `DESIGN.md`.

### 1. Select Macrostructure
- Pick a structural shape fitting the genre (see `references/macrostructures.md`): Bento Grid, Split Studio, Marquee Hero, Stat-Led, Long Document, or Workbench.

### 2. Semantic IA & Spacing via Tailwind Primitives
- Structure content with semantic HTML (`<main>`, `<header>`, `<nav>`, `<article>`, `<section>`, `<footer>`).
- Apply Tailwind 8px spacing scale (`p-4`, `p-6`, `p-8`, `gap-4`, `gap-6`).

### 3. Solid Visual Tokens with Tailwind v4 `@theme`
- Define tokens in CSS `@theme`: Solid OKLCH brand palette, neutral solid surface tints, display/sans font pairings, and subtle box shadows.
- Ensure WCAG contrast: minimum 4.5:1 for body text, 3:1 for large headers and UI borders.

### 4. Component Architecture & States
- Build composable components using Tailwind variants: `hover:`, `focus-visible:ring-2`, `active:scale-[0.98]`, and `disabled:opacity-50`.
- Use `fetchpriority="high"` on hero images (LCP). Never `loading="lazy"` on above-the-fold media.

### 5. Anti-Slop Audit & Polish
- Verify zero gradients, zero icon soup, and zero anti-pattern tells (see `references/anti-patterns.md`). Ensure snappy transitions (`duration-150 ease-out`) with `motion-reduce` support.

---

## References & Deep Dives

- `references/anti-patterns.md` - Complete checklist of AI-slop visual tells (including all gradient bans) and handcrafted fixes.
- `references/macrostructures.md` - Catalog of 6 distinct UI structural shapes and selection criteria.
- `references/inspo-integration.md` - Inspo MCP tool guide (`recommend`, `search_screens`, `get_design_system`, `get_reference_jsx`).
- `references/design-tokens.md` - Tailwind v4 `@theme` configuration, solid OKLCH palettes, typography ramp, spacing scale.
- `references/component-patterns.md` - Bento grids, dashboards, hero layouts, modals, forms, toasts, skeletons (all solid styling).
- `references/taste-and-copy-rules.md` - Anti-slop taste dials, brief inference, typography pairing formulas, human-first copy rules, and layout rhythm constraints.
- `references/responsive-and-accessibility.md` - WCAG 2.1 AA checklists, ARIA roles, keyboard navigation, touch targets.
- `references/modern-styling-recipes.md` - Tailwind v4 solid recipes for clean surfaces, crisp borders, and micro-interactions.
