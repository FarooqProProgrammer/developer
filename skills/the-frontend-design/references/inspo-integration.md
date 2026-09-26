# Inspo MCP Integration Guide

Integrating Inspo MCP (`https://inspomcp.dev/`) into your frontend design workflow.

---

## What Inspo Provides

Inspo gives agents access to a curated archive of **832+ production sites**, **2,320+ full screens**, and **68+ canonical reference components** with already-extracted `DESIGN.md` specifications (color palettes, typography ramps, spacing scales, and radii).

Endpoint: `https://inspomcp.dev/api/mcp` (free, hosted, no auth).

---

## Key Inspo MCP Tools

### 1. Orchestration & Discovery
- **`inspo:recommend`** `(brief: string, filters?: object)`
  - **Start here**. Converts a natural-language product brief into a macrostructure choice, 5 real exemplars, matched reference components, and a ranked color palette.
  - *Example*: `inspo:recommend({ brief: "minimalist developer analytics dashboard with dark theme" })`

- **`inspo:search_screens`** `(query: string, filters?: object)`
  - Search real-world production screens by aesthetic, style, or feature keywords.
  - *Example*: `inspo:search_screens({ query: "swiss style typography b2b saas" })`

- **`inspo:find_examples_for_macrostructure`** `(name: string)`
  - Retrieve production sites embodying 1 of the 19 named UI macrostructures (e.g., "Bento Grid", "Split Studio", "Marquee Hero", "Minimalist", "Specimen").
  - *Example*: `inspo:find_examples_for_macrostructure({ name: "Bento Grid" })`

### 2. Design System Extraction & Study
- **`inspo:get_design_system`** `(slug: string)`
  - Fetches the site's complete `DESIGN.md`: exact font pairings, ranked color tokens, type ramp, spacing scale, and border radii.
  - *Example*: `inspo:get_design_system({ slug: "northmail-app" })`

- **`inspo:get_screen`** `(slug: string)`
  - Inspects full screen details across viewports, layout structure, and design breakdowns.

- **`inspo:compare`** `(slugs: string[])`
  - Side-by-side analysis of 2–4 production sites to identify shared patterns and distinct visual differentiators.

### 3. Canonical Reference Components
- **`inspo:find_reference_components`** `(type?: string, macro?: string)`
  - Queries indexed reference components (e.g., `hero`, `pricing`, `features`, `navigation`).

- **`inspo:get_reference_jsx`** `(type: string, id: string)`
  - Retrieves full, production-ready, copy-pasteable JSX source code for a reference component.

---

## Inspo-Driven Frontend Workflow

```
1. Brief / Search (inspo:recommend)
       ↓
2. Study Exemplars & Extract Tokens (inspo:get_design_system)
       ↓
3. Fetch Component Patterns (inspo:get_reference_jsx)
       ↓
4. Refine & Enforce Restraint (Apply Typography-First & No-Icon-Soup Rules)
       ↓
5. Implement Clean, Accessible UI
```

### Applying Inspo Output with Restraint
When using Inspo exemplars and JSX:
1. **Strip Decorative Icon Clutter**: Remove decorative icon stamps that distract from content. Rely on clean typography, borders, and whitespace.
2. **Align to Design Tokens**: Map extracted palette colors and type scales directly into your project's Tailwind config or CSS custom properties.
3. **Ensure WCAG & Keyboard a11y**: Verify color contrast ratios (>= 4.5:1 for body text) and ensure all interactive controls have accessible focus rings.
