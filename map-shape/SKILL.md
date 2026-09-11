---
name: map-shape
description: Turn a fuzzy product problem or opportunity into a coherent, valuable, simplified, and sequenced shape of work. Use when product work needs boundaries and vertical slices before implementation planning.
metadata:
  author: drewbarontini
  version: "0.1.0"
  systems: "claritorium, equilio"
  models: "value-creation"
---

# Map Shape

Given a product problem or opportunity, use Shape Mapping to discover the work's relationships, isolate deliverable value, reduce scope, and establish an order of operations without prematurely specifying implementation.

## Boundaries

Shape Mapping is for clarifying what should be built and how the value can be bounded. It is not a substitute for product discovery, detailed technical planning, task estimation, or code generation. Do not invent product requirements to make the shape look complete; retain Questions, Risks, and Unknowns.

## Canonical Method

Follow these five steps in order, revisiting earlier steps as new information appears:

1. **Surface** — Create a flat list of everything. Tag each item as Action, Decision, Question, Risk, or Unknown. Nothing is in or out of scope yet.
2. **Structure** — Build relationships in the list. Anchor root nodes, nest sub-items, and link dependencies. Discover relational groups rather than imposing an operational plan.
3. **Slice** — Find vertical slices of value. Name each slice, define its boundary, and test whether it can stand alone as a usable flow—not merely a technical capability.
4. **Simplify** — Reduce each slice to the smallest version that still delivers value. Remove, defer, or narrow scope explicitly.
5. **Sequence** — Create the order of operations. Distinguish build units from value units and bundle slices when users only receive meaningful value from them together.

Read [references/shape-mapping.md](references/shape-mapping.md) for the detailed tests and the optional Shape Prompt form.

## Output

```markdown
# Shape: [Name]

## Context
[Problem, opportunity, user value, and why it matters.]

## Surface
- [A] Action
- [D] Decision
- [Q] Question
- [R] Risk
- [U] Unknown

## Structure
### [Root / Group] (depends on [...])
- [...]

## Slices
### [Slice Name]
- Value: [...]
- Boundary: In [...]; Out [...]
- Dependencies: [...]
- Independence test: [...]

## Simplification
- Keep: [...]
- Reduce: [...]
- Defer / remove: [...]

## Sequence
1. [Build unit or value bundle] — because [...]

## Remaining Uncertainty
- [...]
```

Produce a Shape Prompt only when the user needs a handoff into planning or execution. The Shape Map remains the primary output.

## Quality Bar

A strong shape preserves the five canonical steps, makes relationships and dependencies visible, defines end-to-end slices of recognizable value, subtracts meaningful scope, distinguishes build order from release value, retains uncertainty, and is concrete enough to guide product work without pretending implementation decisions are settled.
