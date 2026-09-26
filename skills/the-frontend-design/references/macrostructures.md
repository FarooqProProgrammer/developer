# UI Macrostructures Catalog

Different product briefs demand distinct structural shapes. Never default to the same generic centered landing page template.

---

## 1. Primary Macrostructures

### 1. Bento Grid (Modular / Density-Led)
- **Best for**: Feature-rich SaaS, multi-utility tools, analytical dashboards.
- **Structure**: Asymmetric CSS Grid (2-col, 3-col, or 4-col spans) where cards vary in height and width.
- **Visual Anchor**: One large hero tile (col-span-2) showing a live preview or metric, flanked by compact metric & status cards.

### 2. Split Studio (Two-Column Asymmetric)
- **Best for**: Creative tools, developer utilities, hardware/product showcases.
- **Structure**: Sticky left panel with headline, concise brief, and primary CTA; scrollable right column with rich interactive components, live code, or product visuals.
- **Visual Anchor**: High-contrast split layout with distinct surface shades.

### 3. Marquee Hero (Scale & Impact)
- **Best for**: High-impact launches, bold consumer apps, brand-led landing pages.
- **Structure**: Massive headline (>48px / `text-5xl` to `text-7xl`) leading immediately into a prominent full-width UI viewport or preview container.
- **Visual Anchor**: High-character display typography paired with generous top/bottom whitespace.

### 4. Stat-Led / Metric-First (Data-Driven)
- **Best for**: FinTech, infrastructure, cybersecurity, enterprise platforms.
- **Structure**: Key performance indicators (99.99%, sub-10ms, $10M+) prominently positioned directly below or beside the main value proposition before feature breakdowns.
- **Visual Anchor**: Monospace tabular numbers, sparkline charts, and minimal borders.

### 5. Long Document / Editorial
- **Best for**: Technical documentation, research tools, essays, manifestos.
- **Structure**: Single-column reading container (`max-w-3xl mx-auto`), serif or high-legibility display headers, prominent pull-quotes, and refined margin notes.
- **Visual Anchor**: Typographic hierarchy, generous leading (`leading-relaxed`), and subtle hairline dividers.

### 6. Workbench / IDE / Console
- **Best for**: Developer tools, terminal utilities, code generators, internal tools.
- **Structure**: Multi-pane layout with compact toolbars, collapsible sidebars, and monospace code/data viewports.
- **Visual Anchor**: Dense information architecture, subtle border grids, and status badges.

---

## 2. Choosing the Right Macrostructure

| Product Category | Recommended Macrostructure | Macrostructure to Avoid |
|---|---|---|
| Developer Tool / API | **Workbench** or **Split Studio** | Full-viewport centered consumer hero |
| FinTech / Infra | **Stat-Led** or **Bento Grid** | Playful illustrative card grid |
| Design Tool / Studio | **Marquee Hero** or **Split Studio** | 3-column equal icon grid |
| Research / Docs | **Long Document** | Heavy Bento grid |
