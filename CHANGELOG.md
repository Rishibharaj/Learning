# Changelog

All notable changes to this project are documented here. Format loosely follows [Keep a Changelog](https://keepachangelog.com/); versioning is pre-1.0 semantic (`0.MINOR.PATCH`) until the first stable multi-pack release.

## [0.2.1] — Sprint 1 patch

### Fixed
- Detail card and the (now-removed) domain legend were overlapping — a CSS rule for `.detail-empty` was overriding the `hidden` attribute, so the empty-state placeholder never actually disappeared when a topic was selected. Added a global `[hidden] { display: none !important; }` rule so the `hidden` attribute always wins.
- Several sunburst segments were missing their text labels. `uniformtext.mode: 'hide'` was hiding any label that didn't fit at one uniform size across the whole chart. Switched to `mode: 'show'` so every segment keeps a visible label.

### Removed
- Domains legend panel (redundant with the domain tag already shown on each knowledge card) — removed from HTML, CSS, and JS.

## [0.2.0] — Sprint 1

### Added
- Top navigation bar with Explore / About / Roadmap views
- Full-text search across all topics with jump-to-topic behavior
- Light / dark theme toggle
- Live breadcrumb trail with click-to-jump, reflecting the current position in the sunburst hierarchy
- Dynamic knowledge cards showing domain tag, description, and use case for the selected topic
- "Reset view" control to zoom the map back out to the root
- About view describing the project and the Knowledge Pack model
- Roadmap view listing sprint plan, future packs, and backlog
- Footer with version number and quick links
- Full documentation set: `PROJECT_STATE.md`, `SPRINT_LOG.md`, `BACKLOG.md`, `DECISIONS.md`, `ARCHITECTURE.md`, `AI_CONTEXT.md`, `JOURNEY.md`, `VISION_HISTORY.md`

### Changed
- Visual design overhauled: new type system (Space Grotesk / Inter / JetBrains Mono), new dark/light color tokens, new domain color palette
- Chart now uses Plotly `uniformtext` for automatic label sizing
- Chart border/background now respond to the active theme
- Every sunburst node (including the root) is confirmed clickable and routed through the same detail/breadcrumb rendering path

### Notes
- Still a single `index.html` file by design — see `docs/DECISIONS.md` ADR-002
- Underlying AI topic data is unchanged from the Sprint 0 prototype; only presentation and interaction changed

## [0.1.0] — Sprint 0

### Added
- Initial AI topic dataset and Plotly sunburst prototype (`AI.html`) — uploaded starting point, not built during Sprint 0 itself
- Product vision, architecture decisions, roadmap, documentation strategy, sprint methodology, Knowledge Pack strategy, and repository structure — all defined, no application code changed
