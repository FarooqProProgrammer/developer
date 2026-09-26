# Anti-Patterns & Anti-AI-Slop Checklist

Quality gates and named visual tells to ensure frontend interfaces look bespoke, intentional, and handcrafted rather than AI-generated.

---

## 1. Zero Gradients Policy (Strictly Enforced)

| Gradient Anti-Pattern | The AI Tell | The Handcrafted Solid Fix |
|---|---|---|
| **Gradient Text Headlines** | `bg-gradient-to-r` + `bg-clip-text text-transparent`. The most common AI design tell. | **Solid ink only**. Use contrasting font weights (`font-bold` vs `font-normal`), scale, or display font pairings for emphasis. |
| **Gradient Backgrounds** | `bg-gradient-to-tr`, `linear-gradient(...)` on heroes, cards, or sections. | **Solid tinted surfaces**. Use flat, calibrated OKLCH tones (e.g., `bg-neutral-900`, `bg-brand-500`) with crisp borders. |
| **Gradient Borders** | Border wrappers with multi-stop linear gradients. | **Solid hairline borders** (`border border-neutral-800` or `border border-white/10`). |
| **Aurora Blobs & Radial Meshes** | Blurred background radial gradients or flowing mesh gradients. | **Zero blobs**. Let clean whitespace and structural alignment provide the atmosphere. |

---

## 2. Layout & Typography Anti-Patterns

| Anti-Pattern | The AI Tell | The Handcrafted Fix |
|---|---|---|
| **Inter-Everywhere** | Using default Inter/Roboto for every element (headings, subheads, buttons, badges) without intentional pairing. | Pair a distinctive display/serif face (e.g. `Cabinet Grotesk`, `Fraunces`, `Cal Sans`) with a clean neo-grotesque body sans. |
| **Symmetric 3-Column Icon Grid** | Three identical columns, each with an icon in a circle above a 2-line heading and 3-line body. | Break the grid: vary column spans (2:1, 1:2), mix card heights, use asymmetrical Bento layouts, or use typographic rows. |
| **Card-in-Card Nesting** | A bordered card containing another bordered card containing a micro-card. | Collapse to a single visual containment layer. Use whitespace and hairline dividers instead of infinite nested boxes. |
| **Pure #000000 & #FFFFFF** | Harsh pure black `#000000` or sterile `#ffffff`. | Tint surfaces toward your anchor hue using OKLCH (`oklch(0.14 0.005 247)` or `oklch(0.985 0.002 247)`). |
| **Generic AI Nav & Footer** | Full-width generic SaaS navbar and 4-column "Product/Company/Legal" sitemap on small or non-SaaS sites. | Pick a genre-appropriate nav (Floating capsule, Masthead, Edge-aligned) and footer (Colophon, Statement, Single-line). |
| **Eyebrows on Every Section** | Putting uppercase mono tags (`01 / FEATURES`, `02 / PRICING`) above every single header. | Eyebrows are **default OFF**. Use them only when content is genuinely sequential or chaptered. Never tag-left/header-right 2-column grids. |
| **Lazy-Loading the Hero Image (LCP)** | Adding `loading="lazy"` to the main hero graphic/image, causing visual blank delay. | Always set `fetchpriority="high"` and eager loading on above-the-fold hero media. Lazy-load only below the fold. |

---

## 3. Interactive & Motion Anti-Patterns

- **Wobbly / Elastic Springs**: Buttons bouncing wildly or icons shaking on hover. Use tight, snappy exponential transitions (`cubic-bezier(0.16, 1, 0.3, 1)` or `transition-all duration-150 ease-out`).
- **Missing Keyboard Focus**: Suppressing `:focus` with `outline-none` without providing `focus-visible:ring-2`.
- **All-Italic Display Words in Headlines**: Flipping random words in headings to italics (e.g. *"Fastest way to build"*). Keep headings roman; use weight or color accents for emphasis.
