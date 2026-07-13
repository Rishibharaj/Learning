# Journey

A narrative record of how Knowledge Explorer came together — useful for a portfolio write-up or README storytelling later.

## Sprint 0 — Deciding what this actually is

The project started from a single working prototype: a Plotly sunburst chart of AI concepts, built to help make sense of a genuinely large field — from data preprocessing all the way through deployment, monitoring, and ethics. Before writing more code, the question was what this should *become*. The answer: not an "AI cheat sheet," but a platform. A domain-independent engine where AI is simply the first subject loaded into it, with PMP — a second area of deep, certified expertise — proving the model works for more than one field.

That sprint produced no new code. It produced the rules: ship working software every sprint, keep the repository as the single source of truth, document as you go, and never let a feature sneak in that doesn't clearly belong yet.

## Sprint 1 — Making the prototype feel real

The starting point worked, but looked and behaved like a prototype: a static two-panel layout, a plain header, and a details panel that only knew how to display raw text. Sprint 1's job was to make it feel like software someone would actually want to explore — without touching its underlying architecture yet.

That meant: real navigation instead of a single scrolling page, a way to search across topics instead of hunting through the chart, a breadcrumb trail so drilling five levels deep never feels disorienting, and a detail card that separates a topic's description from its use case instead of dumping both as one HTML blob. It also meant a deliberate visual identity — a dark graphite base with teal and amber accents, and a breadcrumb trail set in monospace type that doubles as the project's one signature element, tying the UI back to the "workflow/pipeline" idea the AI pack itself is about.

Underneath, the sunburst, the topic data, and the domain structure are untouched from the original prototype. Sprint 1 was about presentation and interaction — proving the *experience* was worth building further before investing in the architecture split.

## What's next

Sprint 2 turns this single file into a real project structure. Sprint 3 goes back into the AI content itself and deepens it. Sprint 4 is the actual proof of the whole idea: adding PMP as a second Knowledge Pack, with zero changes to the engine.
