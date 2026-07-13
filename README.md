# Knowledge Explorer

**An interactive, domain-independent learning platform.**

Knowledge Explorer renders any subject as a navigable sunburst map — click into a topic, read a plain-language summary and a real-world use case, and see exactly where it sits in the wider field. The engine knows nothing about any particular subject; all of that lives in a **Knowledge Pack**.

> Status: **Sprint 1 complete** · Version `v0.2.0` · First pack: **AI**
https://rishibharaj.github.io/Learning/
---

## Current features (Sprint 1)

- Professional layout with a top navigation bar (Explore / About / Roadmap)
- Full-text search across every topic, with jump-to-topic
- Light / dark theme toggle
- Interactive sunburst map (Plotly) — every node, including the root, is clickable
- Live breadcrumb trail showing your current position in the hierarchy, with click-to-jump
- Dynamic knowledge cards: domain tag, description, and use case for the selected topic
- Auto text sizing on the chart (Plotly `uniformtext`) so labels stay legible at any zoom depth
- Fully responsive layout, down to mobile
- Footer with version info and quick links to About / Roadmap

## Tech stack

- HTML5 / modern CSS (custom properties, no framework)
- Vanilla JavaScript (ES6+)
- [Plotly.js](https://plotly.com/javascript/) for the sunburst visualization
- Google Fonts: Space Grotesk (display), Inter (body), JetBrains Mono (utility/mono)

No build step. No frameworks. Open `index.html` in a browser and it runs.

## Running locally

```bash
# clone the repo, then just open the file
open index.html        # macOS
start index.html        # Windows
xdg-open index.html     # Linux
```

Or serve it with any static server if you prefer:

```bash
python3 -m http.server
```

## Project structure (current — Sprint 1)

```
Knowledge-Explorer/
├── index.html          # entire application (Sprint 2 will split this up)
├── README.md
├── ROADMAP.md
├── CHANGELOG.md
├── docs/
│   ├── PROJECT_STATE.md
│   ├── SPRINT_LOG.md
│   ├── BACKLOG.md
│   ├── DECISIONS.md
│   ├── ARCHITECTURE.md
│   ├── AI_CONTEXT.md
│   ├── JOURNEY.md
│   └── VISION_HISTORY.md
└── LICENSE
```

The single-file structure is intentional for Sprint 1 (see `docs/DECISIONS.md`, ADR-002). Sprint 2 splits this into `css/`, `js/`, `assets/`, and `packs/` without changing behavior.

## Knowledge Packs

| Pack | Status |
|---|---|
| AI | Live |
| PMP | Planned — Sprint 4 |
| Cloud Computing, Python, Networking, DevOps, Data Science, Cyber Security, Enterprise Automation | Backlog |

See `ROADMAP.md` for the full sprint plan.

## Documentation

- [`ROADMAP.md`](./ROADMAP.md) — sprint plan and future packs
- [`CHANGELOG.md`](./CHANGELOG.md) — version history
- [`docs/PROJECT_STATE.md`](./docs/PROJECT_STATE.md) — current snapshot (read this first if resuming work)
- [`docs/ARCHITECTURE.md`](./docs/ARCHITECTURE.md) — how it's built and how it will evolve
- [`docs/DECISIONS.md`](./docs/DECISIONS.md) — architecture decision records
- [`docs/BACKLOG.md`](./docs/BACKLOG.md) — deferred features

## License

TBD — to be finalized before public release.

## Author

Built by an operations and AI practitioner (PMP-certified, OCI AI-certified) as an open-source portfolio project and a genuine learning tool.
