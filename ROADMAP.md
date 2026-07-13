# Roadmap

Knowledge Explorer ships in small sprints. Every sprint produces working software — nothing stays half-built between sessions.

## Sprint plan

### ✔ Sprint 0 — Foundation
Product vision, architecture decisions, roadmap, documentation strategy, sprint methodology, Knowledge Pack strategy, and repository structure. No application code.

### ✔ Sprint 1 — Polished single-file prototype
Transform the raw AI sunburst prototype into a professional, usable experience: navigation, search, theme toggle, dynamic knowledge cards, breadcrumb trail, responsive layout, footer, About and Roadmap views. Still a single `index.html` file by design.

### ○ Sprint 2 — Modular architecture
Split the application into:

```
index.html
css/
js/
assets/
packs/
docs/
```

Define the Knowledge Pack data contract (what a pack must supply: topics, hierarchy, summaries, use cases, domain colors, and pack metadata) so the engine can load any pack without code changes.

### ○ Sprint 3 — Expand the AI Knowledge Pack
Deepen the existing pack: more topics, refined summaries, richer and more specific use cases, possibly deeper hierarchy levels.

### ○ Sprint 4 — PMP Knowledge Pack
Build the second Knowledge Pack using the contract defined in Sprint 2, with **no changes to the engine**. This sprint is the real test of the domain-independent architecture.

## Future Knowledge Packs (post Sprint 4)

- Cloud Computing
- Python
- Networking
- DevOps
- Data Science
- Cyber Security
- Enterprise Automation

## Future modules (not scheduled yet)

These are explicitly out of scope until there's a specific sprint for them — see `docs/BACKLOG.md`:

- Learning Mode
- Career Roadmaps
- Quizzes
- Flashcards
- Notes
- Bookmarks
- User Profiles
- Progress Tracking
- Enterprise Case Studies
