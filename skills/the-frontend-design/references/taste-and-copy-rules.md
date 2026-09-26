# Taste Skill & Anti-Slop Copy Guidelines

Principles inspired by and synthesized from **Taste Skill** (`https://tasteskill.dev` / `Leonxlnx/taste-skill`), **Nutlope/hallmark**, and **pbakaus/impeccable**.

---

## 1. Brief Inference & The 3 Taste Dials

Before writing code, read the brief context and declare a one-line **Design Read**:
> *"Reading this as: `<page kind>` for `<audience>`, with a `<vibe>` language, leaning toward `<macrostructure / design system>`."*

### The Three Taste Dials (Scale 1–10)
Set explicit dials for the build:
- **`DESIGN_VARIANCE`** (1 = Symmetrical/Classic, 10 = Asymmetrical/Experimental) — *Default: 7*
- **`MOTION_INTENSITY`** (1 = Static/Crisp, 10 = Kinetic/Spring Physics) — *Default: 5*
- **`VISUAL_DENSITY`** (1 = Spacious/Editorial, 10 = Dense/Cockpit) — *Default: 4*

| Brief Type | VARIANCE | MOTION | DENSITY |
|---|---|---|---|
| B2B SaaS / Devtool | 6–7 | 4–5 | 5–6 |
| Creative Studio / Portfolio | 8–9 | 6–8 | 3–4 |
| Editorial / Publication | 6–7 | 3–4 | 3–4 |
| High-End Consumer / DTC | 7–8 | 5–6 | 3–4 |
| Public-Sector / Trust-First | 3–4 | 2–3 | 5–6 |

---

## 2. Copy & Content Discipline (Human-First Copy)

AI models have a signature writing style that immediately dates and diminishes UI designs. Apply strict copy sanitation:

### A. Em-Dash & Punctuation Sanitation
- **Ban AI Em-Dashes (—)**: Strip decorative em-dashes from headlines, subheads, bullet points, and quotes. Use clean commas, periods, colons, or natural sentence breaks.
- **Typographic Quotes**: Use true curly quotes (`“”`, `‘’`) in editorial copy; never raw straight double quotes (`""`).

### B. Hero Copy & Stack Discipline
- **Max 4 Hero Text Elements**:
  1. Optional Eyebrow (mono/uppercase label) OR Brand Tag
  2. Headline (max 2 lines at desktop)
  3. Subtext (max 20 words, max 3–4 lines)
  4. CTA Row (1 primary + max 1 secondary)
- **Banned in the Hero**: Do not cram logo walls, trust micro-strips, pricing tags, and bullet feature lists into the hero block. Move social proof and feature details to dedicated sections below the hero.
- **Top Padding Cap**: Maximum `pt-24` (6rem) at desktop so content remains firmly within the initial viewport.

### C. Eyebrow Restraint (#1 Violated AI Tell)
- **Max 1 Eyebrow per 3 Sections**: An eyebrow is a small uppercase tracking label above a header (e.g. `text-xs uppercase tracking-widest font-mono`).
- If Section 1 has an eyebrow, Sections 2 and 3 MUST NOT have one.
- In most sections, the headline alone carries the section without needing an artificial category label.

### D. Single-Line CTA & Intent Unification
- **Single-Line Desktop CTAs**: CTA button text MUST NOT wrap to 2 lines on desktop. Keep CTA copy concise (1–3 words: *"Start Free Trial"*, *"View Portfolio"*, *"Deploy Now"*).
- **Zero Duplicate CTA Intent**: Never mix synonyms on the same page (e.g., mixing *"Get in touch"*, *"Let's talk"*, *"Contact us"*, and *"Reach out"*). Pick ONE canonical action label per user intent across nav, hero, and footer.

### E. Anti-Cute Copy Self-Audit
- Flag and rewrite:
  - Mock-craftsman humblebrags (*"Obsessively handcrafted for human workflows"*).
  - Vague poetic metaphors (*"Where ideas take flight"*).
  - Fabricated precision metrics (`94.8%`, `3.7x`) unless backed by real provided data or explicitly marked as `<!-- mock -->`.

---

## 3. Typography Rules & Anti-Clichés

- **Sans Display Defaults**: Move beyond default Inter. Prefer **Geist**, **Cabinet Grotesk**, **Satoshi**, **Outfit**, or **PP Neue Montreal**.
- **Display Serif Discipline**: Do not use serifs simply because a brief mentions "creative" or "luxury". Use serifs only when explicitly requested by brand guidelines or publication briefs. Specifically avoid default LLM serif reaches (`Fraunces`, `Instrument Serif`).
- **Same-Family Emphasis**: When emphasizing a key word in a headline, use **italic or bold in the same font family**. Do NOT inject a mismatched serif word into a sans headline.
- **Italic Descender Clearance**: When using italic display text with descender letters (`g`, `j`, `p`, `q`, `y`), ensure `leading-[1.15]` and `pb-1` to prevent glyph clipping.

---

## 4. Color Calibration & Palette Anti-Slop

- **One Accent Rule**: 1 primary accent color per view, with saturation calibrated under 80%.
- **Anti-Lila / Anti-Purple Glow**: Avoid default AI purple-neon buttons, glowing radial halos, and violet gradients.
- **Ban the Beige + Brass Cliché**: For premium consumer briefs, avoid defaulting to warm paper beige (`#f5f1ea`) + brass/clay (`#b08947`) + espresso dark text.
  - **Fresh Alternatives**:
    - **Cold Luxury**: Silver-grey (`#f0f2f5`), chrome borders, deep slate ink (`#0f172a`).
    - **Forest & Bone**: Deep pine ink (`#06231a`), crisp bone background (`#f8faf7`), emerald accent.
    - **Cobalt & Crisp White**: Deep cobalt blue (`#1e40af`) on ultra-clean white (`#ffffff`).
    - **Terracotta & Slate**: Warm rust accent on neutral cool grey base.
- **Color Consistency Lock**: Once a background hue and accent are chosen, maintain the tone throughout the entire page.

---

## 5. Structural & Rhythm Rules

- **Anti-Center Bias**: When `DESIGN_VARIANCE > 4`, avoid centered hero layouts. Use 50/50 splits, asymmetric typography, or left-aligned copy with right-aligned product workbench.
- **Bento Cell Count Rule**: Bento grids MUST have exactly as many cells as there is real content (3 items → 3-cell layout; 5 items → 5-cell layout). Never insert blank empty tiles as visual filler.
- **Bento Diversity**: Bento cards must not be identical white-on-white text boxes. Include real product previews, solid tinted backgrounds, code snippets, or interactive toggles.
- **Zigzag Alternation Cap**: Do not chain more than 2 consecutive alternating left-image / right-text blocks. Break rhythm with full-width statements, bento grids, or data strips.
- **Max 1 Marquee per Page**: If a horizontal scrolling strip is used (for logos or badges), allow at most ONE per page. Multiple marquees create sensory clutter.
