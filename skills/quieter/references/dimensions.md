# The 5 Refinement Dimensions

Detailed guidelines for systematically reducing visual loudness across interfaces.

---

## 1. Color Refinement

1. **Desaturate Accents**:
   - High-saturation colors (Chroma > 0.22 in OKLCH) cause retinal fatigue.
   - Scale down chroma to `0.10`–`0.16` for ambient accents, reserving higher chroma exclusively for active interaction states.
2. **Neutral Dominance (The 90/10 Rule)**:
   - 90% of your visual surface area should be composed of carefully calibrated tinted neutrals (surfaces, text, borders).
   - 10% is allocated to functional color (primary CTA, active status indicator).
3. **Tinted Grays**:
   - Never use dead monochromatic `#808080`.
   - In dark mode, tint dark surfaces slightly with the brand hue (e.g. `oklch(0.15 0.005 250)`).
   - In light mode, use warm/cool paper tones (`oklch(0.985 0.003 250)`).
4. **Contrast Calibration**:
   - Ensure body copy satisfies WCAG AA (4.5:1), but avoid harsh 21:1 stark contrast across every secondary label. Use subdued secondary neutrals (`text-neutral-400` or `text-neutral-500`) to create gentle reading rhythm.

---

## 2. Visual Weight & Typography

1. **Weight Step-Downs**:
   - Replace massive `font-black` (900) display weights with elegant `font-bold` (700) or `font-semibold` (600).
   - Replace heavy labels (`font-bold`) with `font-medium` (500) and slightly wider letter spacing (`tracking-wide text-xs`).
2. **Typographic Air**:
   - Increase line-height on paragraphs (`leading-relaxed` / `1.625`–`1.75`).
   - Increase padding around main heading blocks (`mb-6` or `mb-8`).
3. **Hairline Dividers**:
   - Replace 2px solid borders with 1px semi-transparent borders (`border-neutral-800/60`).

---

## 3. Simplification & De-cluttering

1. **Eliminate Decorative Noise**:
   - Remove decorative background grid lines, ambient particle effects, and generic blobs.
   - Let content and layout structure be the ornament.
2. **Flatten Containers**:
   - If a page has a card inside a container inside a bordered section, remove the outer or middle container.
   - Use whitespace grouping rather than nested bordered boxes.
3. **Icon Removal**:
   - Remove non-essential icons from button labels, navigation bars, and card headers. Plain, well-typeset words are calmer and easier to read.

---

## 4. Motion & Micro-Interactions

1. **Shorten Distances**:
   - Modals and tooltips should animate over `8px`–`16px`, not `40px`–`60px`.
2. **Gentle Timing Curves**:
   - Duration: `150ms`–`220ms`.
   - Easing: Exponential ease-out (`cubic-bezier(0.16, 1, 0.3, 1)` or `ease-out`).
   - Strictly prohibit bouncy, oscillating, or elastic transitions.
3. **Meaningful State Shifts**:
   - Hover states should produce subtle surface brightness lifts or border highlight, not jarring transforms or color flips.

---

## 5. Compositional Balance

1. **Grid Alignment**:
   - Align all disparate padding, margins, and gaps to standard 8pt steps (`8px`, `16px`, `24px`, `32px`, `48px`, `64px`).
2. **Balanced Scale Step Ratio**:
   - Avoid jarring jumps between adjacent text sizes (e.g. 64px heading directly on top of 12px label). Use a stepping subheading (`20px` / `text-xl`) or increase whitespace.
