# AI Context

This document exists specifically for an AI assistant resuming work on this project in a new session, where the only available context is the repository's files. Read this alongside `PROJECT_STATE.md`.

## Who this project is for

The project owner is a Business Operations Manager with 20+ years in Operations Management, PMP certified, OCI AI certified, with strong interest in AI, enterprise automation, correspondence intelligence, OCR, NLP, workflow automation, and visualization. The project is being built both to learn deeply and to serve as a flagship GitHub/LinkedIn portfolio piece.

**Preferences:** professional, structured, well documented, scalable, enterprise-grade thinking.
**Dislikes:** messy code, unplanned features, marketing hype, unverified technical claims.

## Operating rules for this project

1. Every sprint produces working software — never leave a sprint half-finished.
2. The repository is the source of truth, not chat memory. Always ask for or read the current files before making changes.
3. Documentation is updated every sprint — all eleven documents listed below, when relevant.
4. No copied code. Everything must be explainable.
5. Quality over quantity.
6. Every feature must improve learning (the actual educational value of the platform), not just look impressive.
7. If a feature doesn't belong in the current version, it goes to `BACKLOG.md` — don't half-build it.
8. Don't spend multiple responses just planning. Every response should either produce working files or improve existing ones.
9. If HTML/code files are uploaded, modify them rather than recreating everything from scratch, unless a major architectural refactor has already been explicitly agreed.
10. Before adding any feature, the test is: "Does this make Knowledge Explorer better?" If yes, implement it now. If no, backlog it.

## The eleven documents and what each one is for

| File | Purpose |
|---|---|
| `README.md` | Public-facing overview |
| `PROJECT_STATE.md` | Current snapshot — read this first |
| `CHANGELOG.md` | Version history |
| `ROADMAP.md` | Sprint plan and future packs |
| `SPRINT_LOG.md` | Per-sprint goal/delivered record |
| `BACKLOG.md` | Deferred features |
| `DECISIONS.md` | Why things were built the way they were (ADRs) |
| `ARCHITECTURE.md` | How it's built now and how it will evolve |
| `AI_CONTEXT.md` | This file |
| `JOURNEY.md` | Narrative story of the project, for portfolio storytelling |
| `VISION_HISTORY.md` | How the vision itself has evolved over time |

## Product vision, in one paragraph

Knowledge Explorer is a domain-independent interactive learning platform. Knowledge is supplied entirely through "Knowledge Packs" — the engine itself should never need code changes to support a new subject, only new data. AI is the first pack; PMP is the second; Cloud Computing, Python, Networking, DevOps, Data Science, Cyber Security, and Enterprise Automation are planned after that.

## How to start a new session on this project

1. Ask for (or read, if provided) `PROJECT_STATE.md` and the current `index.html` (or, from Sprint 2 onward, the full current file set).
2. Confirm the current sprint from `PROJECT_STATE.md` and `ROADMAP.md`.
3. Check `DECISIONS.md` before proposing anything that might contradict a settled ADR.
4. Check `BACKLOG.md` before adding a feature that isn't clearly in the current sprint's scope.
5. Implement, don't just plan. Update the relevant documentation files as part of the same response, not as an afterthought.
