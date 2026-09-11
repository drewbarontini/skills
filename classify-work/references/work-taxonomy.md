# Work Taxonomy

## Type

Each item gets exactly one Type based on what it is now:

- **Idea** — vague but directional; a hunch, question, or observation to explore rather than execute.
- **Task** — a discrete supporting unit of effort that is not directly actionable product behavior.
- **Fix** — known expected behavior does not work as expected; includes bugs, broken flows, and regressions.
- **Improvement** — a known effort to make existing behavior or quality better, often in usability, performance, or coherence.
- **Bet** — an intentional investment and tradeoff to create product value amid uncertainty; commonly represented by a Project and generative of Tasks, Fixes, and Improvements.

Type can evolve. An Idea may gather enough context to become a Bet. A supposed Fix may be an Improvement when the current behavior matches its specification but should change.

## Impact

The requested classification includes Impact, but the canonical public Work Registry source defines **Priority** as its third layer rather than a formal Impact taxonomy. Preserve Impact without inventing levels:

- Who or what is affected: customers, product, business, team, or system.
- Current consequence or unrealized value.
- Breadth, depth, frequency, or urgency only when supported.
- Evidence and uncertainty.

Impact explains why the work matters. It does not by itself set commitment, sequence, or priority.

## Product Landscape

Use the organization's existing hierarchy:

- **Region** — broad product territory.
- **Zone** — a meaningful area inside a Region.
- **Context** — the specific surface or situation.

Map only as deeply as the evidence and supplied taxonomy allow. “Search → Mobile” may be valid only if Search and Mobile are actual Landscape coordinates for that product.

## Work Forms

- **Batch** — a lightweight container for related, focused Fixes and Improvements on a product surface.
- **Stream** — an intentional container for focused Experiments designed to resolve a tension; it ends in resolution or escalation.
- **Project** — a concentrated, committed body of work designed to deliver meaningful product value. In the Project Engine it moves through Align → Clarify → Model → Build → Learn.

Do not use a container merely because several items share a label. Look for coherent relations, appropriate energy, and current understanding.

## Routes

- **Triage** — captured but not yet accepted, classified, and routed.
- **Radar / Backlog** — acknowledged someday/maybe work without current commitment.
- **Queue** — near-term committed work, commonly constrained to the current week and assigned to one owner.
- **In Progress** — actively being worked; limit work in flight.
- **In Review** — technical, quality, or acceptance review.
- **Done** — completed work.
- **Canceled** — no longer valid.
- **Duplicate** — already represented elsewhere.
- **Deleted** — unnecessary noise without registry value.

Lanes represent increasing commitment. When work is blocked and no longer active, return it to Queue or Radar rather than hiding the bottleneck in In Progress.

## Canonical Sources

- [Work Registry](https://drewbarontini.com/newsletter/75-work-registry/) — Capture → Classify → Route → Evolve → Elevate; Types and routes.
- [Work Formation](https://drewbarontini.com/newsletter/84-work-formation/) — Aggregation → Activation → Stabilization; Batches, Streams, and Projects.
- `equilio/models/strategic-momentum.md` — alignment, purposeful execution, and fast feedback loops.
