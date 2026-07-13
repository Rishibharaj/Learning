# Decisions

Architecture Decision Records (ADRs) for Knowledge Explorer. Each entry captures a choice, why it was made, and what it rules out — so future sessions don't relitigate settled questions or silently drift from them.

---

### ADR-001 — Domain-independent Knowledge Pack architecture
**Decision:** The application engine has no built-in knowledge of any subject. All topic data (hierarchy, summaries, use cases, colors) is supplied by a "Knowledge Pack." AI is the first pack; PMP is the second.
**Why:** The long-term goal is a platform that scales to many subjects without rewriting code. This is the central bet the whole project is built on.
**Rules out:** Hard-coding subject-specific logic (e.g. "if topic contains 'PMP'") anywhere in the engine.

### ADR-002 — Improve the existing HTML before modularizing
**Decision:** Sprint 1 improves the single-file prototype in place. The split into `css/`, `js/`, `assets/`, `packs/` happens in Sprint 2, not Sprint 1.
**Why:** Per project rules, every sprint must ship working software, and the fastest path to a materially better working product was polishing what already worked rather than re-architecting and polishing simultaneously.
**Rules out:** Introducing a build step, bundler, or multi-file structure in Sprint 1.

### ADR-003 — Plotly Sunburst as the core visualization engine
**Decision:** Keep Plotly.js's sunburst chart as the primary way to render a Knowledge Pack's hierarchy, rather than replacing it with a custom D3 build or a different chart type.
**Why:** It already does hierarchical drill-down, hover text, and click-to-zoom out of the box, and the existing dataset is already shaped for it (`labels` / `parents` arrays).
**Rules out:** Custom-built visualization work in the near term. Revisit only if a future pack's data doesn't fit a strict tree (e.g. cross-links between topics).

### ADR-004 — Visual identity: dark graphite base, teal/amber accents, three-typeface system
**Decision:** Design tokens are: background `#0F1419` (dark) / `#F5F6F8` (light); accent `#5EEAD4` teal (dark) / `#0C9C8C` (light); secondary accent `#F0B429` amber (dark) / `#B9790A` (light). Typography: Space Grotesk for display, Inter for body, JetBrains Mono for breadcrumbs, tags, and other utility text.
**Why:** The subject is a technical workflow/pipeline; the mono-font breadcrumb trail doubles as the project's one signature visual element, echoing the "workflow" concept the AI pack itself is about. Deliberately avoided a warm-cream-and-terracotta or near-black-with-single-neon look, since both read as generic AI-generated defaults.
**Rules out:** Ad-hoc color or font choices in future sprints — extend this token set rather than introducing new ones per screen.

### ADR-005 — No persistence layer in Sprint 1
**Decision:** Theme choice and any other UI state reset on page reload. No `localStorage` or backend.
**Why:** The current deliverable is a portfolio-facing static prototype; adding persistence now would be scope creep ahead of the Sprint 2 architecture split, and is explicitly listed in `BACKLOG.md` instead.
**Rules out:** Silently adding storage-dependent features before this decision is revisited.

### ADR-006 — Pre-1.0 versioning
**Decision:** Version numbers follow `0.MINOR.PATCH` until the platform has more than one working Knowledge Pack and the modular architecture is in place. Sprint 1's release is `v0.2.0`.
**Why:** Calling a single-pack, single-file prototype `v1.0` would overstate its maturity for a portfolio audience that includes engineers evaluating the project seriously.
**Rules out:** Jumping to `1.0.0` before Sprint 4 (PMP pack) and Sprint 2 (modular architecture) are both done.
