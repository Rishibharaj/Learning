# Sprint Log

## Sprint 0 — Foundation

**Goal:** Establish the project's vision and rules before writing application code.

**Delivered:**
- Product vision (domain-independent platform, AI as first Knowledge Pack, PMP second)
- Architecture direction (Knowledge Pack model, no engine changes for new subjects)
- Roadmap through Sprint 4 and beyond
- Documentation strategy — the eleven-document set this project maintains
- GitHub strategy, sprint methodology, repository structure

**Notes:** Planning only. The AI sunburst prototype (`AI.html`) already existed as the starting point for Sprint 1 and was not built during Sprint 0.

---

## Sprint 1 — Polished single-file prototype

**Goal:** Improve the existing HTML prototype before modularizing it — better layout, navigation, typography, search, theme toggle, interactions, and documentation, without splitting files yet.

**Delivered:**
- Professional layout with sticky top navigation (Explore / About / Roadmap)
- Full-text topic search with jump-to-topic
- Light / dark theme toggle, applied to both the UI and the chart
- Live breadcrumb trail synced to the sunburst's current zoom level, with click-to-jump
- Dynamic knowledge cards (domain tag, description, use case) replacing the static side panel
- Every sunburst node — including the root — routed through the same click-handling path
- Auto text sizing via Plotly `uniformtext`
- Refined, harmonized domain color palette
- Fully responsive layout (chart stacks above detail panel on narrow screens)
- Footer with version number and links to About / Roadmap
- About view (project explanation, Knowledge Pack list) and Roadmap view (sprint plan, future packs, backlog) added directly in the single file
- Full documentation set created: `PROJECT_STATE.md`, `SPRINT_LOG.md`, `BACKLOG.md`, `DECISIONS.md`, `ARCHITECTURE.md`, `AI_CONTEXT.md`, `JOURNEY.md`, `VISION_HISTORY.md`, plus `README.md`, `ROADMAP.md`, `CHANGELOG.md`

**Deferred to later sprints (see `BACKLOG.md` and `ROADMAP.md`):**
- Splitting into `css/`, `js/`, `assets/`, `packs/` (Sprint 2)
- Theme preference persistence — deliberately not added yet (see `DECISIONS.md` ADR-005)
- Any second Knowledge Pack (PMP — Sprint 4)
- Any of the "future modules" (quizzes, notes, profiles, etc.)

**Notes:** The underlying AI topic dataset (labels, hierarchy, summaries, use cases) is unchanged from the uploaded prototype — Sprint 1 scope was presentation and interaction, not content expansion. Content expansion is Sprint 3.
