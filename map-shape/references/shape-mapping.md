# Shape Mapping Reference

## Surface

Create visibility before imposing order. Capture large and small items in a single flat list:

- **Action** — something to do.
- **Decision** — something to decide.
- **Question** — something to answer.
- **Risk** — something to watch.
- **Unknown** — something to learn.

Do not filter for scope yet. Add new items as later passes expose missing work.

## Structure

Discover a causal map:

1. Anchor root nodes.
2. Nest sub-items under the relationship they serve.
3. Link dependencies explicitly.

Group by what belongs together, not by department, implementation layer, or delivery status unless that relationship is intrinsic to the product.

## Slice

Convert structures into independent units of value:

1. Name the slice.
2. Define the boundary.
3. Test independence.

Ask: **What can we build and ship entirely independently?** A valid slice should create a usable flow. Database, API, and interface layers are usually parts of a vertical slice, not separate value slices.

## Simplify

Ask: **What is the smallest version of each slice that still delivers value?**

Show subtraction. Mark which states, fields, controls, permissions, variants, or edge cases are deferred and why the reduced slice remains useful. Cheap execution is not evidence that added scope is valuable.

## Sequence

- **Build units** are slices defined as they can be built.
- **Value units** are what can be delivered to create real user value.
- A **bundle** combines slices that only become valuable together.

Sequence dependencies while looking for foundations that can safely ship independently. Do not call a technical layer a release merely because it can be deployed.

## Optional Shape Prompt

Use this only for a requested implementation-planning handoff:

```markdown
Feature: [Name]

Context:
[Why this exists and how it fits the system]

Capabilities:
- [...]

Behavior:
- States: [...]
- Actions: [...]
- Transitions: [...]
- Feedback: [...]
- Constraints: [...]

Uncertainty:
- Risks: [...]
- Questions: [...]

Task:
[What the receiving agent should produce]
```

The Shape Prompt should express the validated shape, not fill gaps with speculative requirements.

## Canonical Sources

- [Shape Mapping](https://drewbarontini.com/newsletter/83-shape-mapping/) — Surface → Structure → Slice → Simplify → Sequence and the Shape Prompt.
- `equilio/models/value-creation.md` — Name the real problem, shape with intention, ship early and often.
