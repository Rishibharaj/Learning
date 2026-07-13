# Architecture

## Current architecture (Sprint 1)

Everything lives in a single `index.html`: markup, CSS, and JavaScript in one file, with Plotly.js and Google Fonts loaded from a CDN. There is no build step and no framework.

The file is organized into four logical layers, even though it's one physical file:

1. **Data layer** — `labels`, `parents`, `summaries`, `domainColor` arrays/objects. This is the AI Knowledge Pack's content, currently inlined directly in the `<script>` block.
2. **Rendering layer** — builds the Plotly sunburst trace from the data layer, and builds the legend and detail card markup.
3. **Interaction layer** — click handling on the chart, breadcrumb generation and click-to-jump, search, theme toggle, and view (tab) switching.
4. **Presentation layer** — CSS custom properties (design tokens) driving both light and dark themes; all colors, spacing, and type are defined as variables, not hard-coded per rule.

## Data model (current)

A topic is represented across three parallel structures, keyed by label:

- `labels[]` — every topic name, root first
- `parents[]` — each topic's parent name, same index as `labels`; root's parent is `""`
- `summaries{}` — `label → "description<br><b>Use Case:</b> use case text"`
- `domainColor{}` — top-level domain name → hex color
- `domainChildren{}` (derived) — maps each domain to its children, used to color every descendant by its domain

This is a flat tree encoded as two parallel arrays, which is exactly what Plotly's sunburst trace expects natively.

## Planned architecture (Sprint 2)

```
Knowledge-Explorer/
├── index.html              # shell: layout, nav, containers — no inline data or heavy logic
├── css/
│   └── styles.css          # design tokens + all component styles
├── js/
│   ├── app.js               # bootstraps the app, wires up nav/search/theme
│   ├── chart.js              # Plotly sunburst setup + interaction
│   ├── pack-loader.js         # fetches and validates a Knowledge Pack
│   └── ui.js                  # detail card, breadcrumb, legend rendering
├── assets/
│   └── (icons, images if any)
├── packs/
│   └── ai/
│       └── pack.json          # the data currently inlined in index.html
└── docs/
    └── (this documentation set)
```

### Knowledge Pack data contract (proposed for Sprint 2)

A pack should be a single JSON file with, at minimum:

```json
{
  "id": "ai",
  "name": "AI",
  "version": "1.0.0",
  "labels": ["...", "..."],
  "parents": ["", "..."],
  "summaries": { "Topic Name": { "description": "...", "useCase": "..." } },
  "domainColors": { "Domain Name": "#hex" }
}
```

Splitting `description` and `useCase` into separate fields (rather than one string with an embedded `<br><b>Use Case:</b>`) is planned for the Sprint 2 migration — the current inline-HTML-in-data approach in Sprint 1 was inherited from the original prototype and is a known rough edge, tracked here rather than fixed mid-sprint.

`pack-loader.js` will validate that `labels.length === parents.length`, that every parent (except the root's) exists in `labels`, and that every label has an entry in `summaries`.

### Why this split, specifically

- `chart.js` isolated from `ui.js` so the visualization library could be swapped later without touching card/breadcrumb rendering.
- `pack-loader.js` is the one place that knows how to fetch and validate a pack — this is the seam that makes "no engine changes for new packs" (ADR-001) actually true, and the seam Sprint 4 will exercise for the PMP pack.
- CSS stays in one file rather than per-component for now; only split further if it grows unwieldy.
