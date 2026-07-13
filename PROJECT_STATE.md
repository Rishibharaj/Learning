# Project State

**This is the single most important file for resuming work.** If you are an AI assistant picking this project back up, read this file and `docs/AI_CONTEXT.md` first.

Last updated: Sprint 1

---

## Where things stand

- **Current sprint:** Sprint 1 — complete
- **Current version:** `v0.2.0`
- **Current deliverable:** `index.html` — a single-file, professional-quality Knowledge Explorer with the AI Knowledge Pack embedded in it
- **Next sprint:** Sprint 2 — split the single file into a modular architecture (`css/`, `js/`, `assets/`, `packs/`)

## Completed sprints

| Sprint | Outcome |
|---|---|
| Sprint 0 | Vision, architecture decisions, roadmap, documentation strategy, repo structure — all decided, no code yet |
| Sprint 1 | Raw Plotly sunburst prototype (`AI.html`) transformed into the first version of Knowledge Explorer |

## What exists right now

- `index.html` — the entire application: layout, styling, data, and interaction logic in one file
- Full documentation set (this file and its siblings, listed below)
- No `css/`, `js/`, `packs/` folders yet — that split is Sprint 2 scope, not done yet

## What Sprint 1 delivered

See `SPRINT_LOG.md` for the full breakdown. Summary: navigation, search, theme toggle, breadcrumb trail, dynamic knowledge cards, responsive layout, footer, About and Roadmap views, auto text sizing on the chart.

## What Sprint 1 deliberately did NOT do

- Did not split the file into a modular structure (that's Sprint 2, by design — see `DECISIONS.md` ADR-002)
- Did not add a second Knowledge Pack (PMP is Sprint 4)
- Did not add persistence (theme choice resets on reload — see `DECISIONS.md` ADR-005)
- Did not add any Backlog features (quizzes, notes, profiles, etc. — see `BACKLOG.md`)

## Known issues / open questions

- No automated tests yet (not expected until the codebase is modularized in Sprint 2)
- License is not yet chosen — README currently says "TBD"
- No real GitHub repository URL exists yet, so none is referenced anywhere in the docs

## How to resume this project in a new session

1. Read this file, then `docs/AI_CONTEXT.md`.
2. Skim `docs/ARCHITECTURE.md` for how the current file is put together.
3. Check `ROADMAP.md` for what Sprint 2 (or whichever sprint is next) is supposed to deliver.
4. Check `docs/BACKLOG.md` to make sure you're not accidentally pulling a backlog item into scope early.
5. Provide the current `index.html` (and any other current files) at the start of the session — this project's rule is that the repository, not chat memory, is the source of truth.
