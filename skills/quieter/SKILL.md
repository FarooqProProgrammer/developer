---
name: quieter
description: Systematically addresses color saturation, contrast extremes, visual weight, animation excess, and compositional complexity to create calmer, more approachable interfaces. Use when an interface is too loud, overstimulating, aggressive, or visually chaotic.
---

# Quieter

Systematically refine loud, aggressive, or overstimulating user interfaces into calm, focused, and approachable designs through intentional restraint without losing personality or making the result generic.

## Core Principle: Restraint, Not Elimination

> **Quiet design is harder than bold design.** Subtlety requires precision. "Quieter" does not mean boring, washed-out, or generic—it signals luxury, confidence, and focus. Drama is reduced, not eliminated; the product's point of view stays intact.

---

## The 4-Phase Quieter Protocol

```
1. Context Gathering -> 2. Intensity Assessment -> 3. 5-Dimension Refinement -> 4. Character & Affordance Audit
```

### Phase 1: Context Gathering (Stop & Clarify)
Before changing any code, clarify the context:
1. **Purpose**: Is this a marketing page (persuade/experience), a tool (operate), or content (read)?
2. **Audience**: Does the audience require subtle calm or energetic feedback?
3. **What's Working**: Identify strong ideas, core messages, and anchors that must be preserved.
4. If the intent or working components are ambiguous, ask for clarification before editing.

### Phase 2: Intensity Assessment
Analyze the active sources of visual loudness:
- **Color Saturation**: Overly vibrant, fluorescent, or competing accent colors.
- **Contrast Extremes**: Harsh stark juxtapositions causing eye strain.
- **Visual Weight**: Too many competing heavy font weights (e.g., all 800/900 bold).
- **Animation Excess**: Over-animated entries, bouncy physics, or decorative loops.
- **Compositional Complexity**: Too many visual containers, patterns, or decorative elements.

---

## Phase 3: The 5 Refinement Dimensions

### 1. Color (Desaturate & Restrain)
- Shift from 100% saturation to **70%–85%** muted/calibrated OKLCH tones.
- Enforce the **10% Accent Rule**: Neutrals do 90% of the work; color is reserved for primary focus.
- Use **tinted neutrals** (warm zinc or cool slate) instead of raw stark grays.
- **Never gray-on-color**: On colored badges/surfaces, use a darker tint of that color or opacity.

### 2. Visual Weight (Typographic Air)
- Step down font weights: `font-black` (900) $\rightarrow$ `font-semibold` (600), `font-bold` (700) $\rightarrow$ `font-medium` (500).
- Increase whitespace around headings and section boundaries.
- Reduce border opacity or thickness (`border-neutral-800/60` instead of heavy solid lines).

### 3. Simplification (Remove Clutter)
- Strip unnecessary decorative layers, gradient strokes, and multi-drop shadows.
- Flatten card-in-card nesting into single semantic containment layers.
- Remove decorative icons that provide no functional utility.

### 4. Motion (Gentle & Short)
- Shorten translation distances (e.g. 10px–15px instead of 40px–60px).
- Use smooth exponential ease-out curves (`cubic-bezier(0.16, 1, 0.3, 1)`).
- Eliminate all bounce, wobble, and non-functional loop animations.

### 5. Composition (Rhythm & Grid)
- Soften extreme scale jumps between adjacent elements.
- Align rogue margins and paddings back to an 8pt grid scale.
- Maintain consistent vertical rhythm across sections.

---

## Anti-Patterns to Avoid During Calming

- ❌ **Grayscale Flattening**: Quiet does not mean removing all color.
- ❌ **Erasing Visual Hierarchy**: Never make every element the same size or weight. Key anchors must remain distinct.
- ❌ **Sacrificing Usability**: Interactive affordances (hover states, focus rings, disabled indicators) must remain obvious and WCAG compliant.

---

## References

For detailed checklists and recipes, see:
- `references/dimensions.md` - In-depth breakdown of the 5 refinement dimensions.
- `references/context-gathering.md` - Context classification and visitor mode rules.
