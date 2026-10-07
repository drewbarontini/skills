---
name: map-shape
description: Shape a fuzzy product problem into a coherent pitch through adaptive interviewing, scope reduction, and sketch or prototype feedback. Use when user-facing work needs a clear problem, rough solution, and bounded scopes before implementation planning.
metadata:
  author: drewbarontini
  version: "0.2.0"
  systems: "claritorium, equilio"
  models: "value-creation"
---

# Map Shape

Given an initial understanding of a product problem, develop a bounded, coherent pitch that makes the next sketch or prototype useful. Use an adaptive interview to discover what matters, preserve unresolved questions, and refine the same pitch as new evidence appears.

## Boundaries

Shape the user experience before specifying implementation. Do not invent requirements, evidence, or settled decisions to complete the document. This skill clarifies existing understanding; it does not replace user research, feasibility testing, detailed technical planning, estimation, or code generation. If an answer needs contact with reality, identify the smallest useful sketch, prototype, or evidence-gathering action rather than prolonging the interview.

## Interview and Synthesis

1. **Orient from what is supplied.** Read the initial notes and any existing pitch, sketches, or prototype. Reflect the apparent problem, proposed direction, constraints, and most consequential uncertainty. Separate observations, assumptions, proposals, and decisions.
2. **Ask the next useful question.** Ask one focused question at a time, or a small pair when inseparable, then wait for the answer. Choose the question whose answer could most change the problem, solution, or boundary. Do not repeat answered questions or run a fixed questionnaire. Probe concrete situations, desired outcomes, product fit, appetite, and gaps in the user's journey as needed.
3. **Contribute judgment.** Offer provisional interpretations, smaller alternatives, and tradeoffs grounded in the supplied context. Explain why a choice matters. Challenge a proposed feature when the underlying problem or value is unclear; do not silently convert a suggestion into a requirement.
4. **Synthesize as understanding changes.** Keep a living pitch rather than waiting for exhaustive certainty. Briefly reflect consequential decisions and remaining uncertainty. If the supplied context is already sufficient, draft directly and ask only questions that materially affect the shape.
5. **Use sketches and prototypes inside the loop.** When a spatial or interactive question would benefit from drawing, name the area and what the sketch should resolve. When sketches or a prototype return, trace the user journey, compare it with the pitch, expose contradictions or missing transitions, and revise the same pitch. Do not restart the interview or treat a drawn choice as validated user evidence.

## Canonical Method

Use these five steps to develop the shape, revisiting earlier steps as answers and artifacts change it. They guide the reasoning; they do not require five separate interview rounds or five output sections.

1. **Surface** — Create a flat list of everything. Tag each item as Action, Decision, Question, Risk, or Unknown. Nothing is in or out of scope yet.
2. **Structure** — Build relationships in the list. Anchor root nodes, nest sub-items, and link dependencies. Discover relational groups rather than imposing an operational plan.
3. **Slice** — Identify meaningful user-facing scopes and test the usable flow each contributes. A scope names an outcome or interaction, not just a screen or technical layer. Identify which scopes can stand alone and which deliver value together.
4. **Simplify** — Reduce each slice to the smallest version that still delivers value. Remove, defer, or narrow scope explicitly.
5. **Sequence** — Explain the useful order for sketching or prototyping, distinguishing dependencies and build units from what must come together to deliver user value.

Read [references/shape-mapping.md](references/shape-mapping.md) when a detailed Shape Map, slice-independence test, or implementation-planning handoff is useful.

## Output

The default output is a living pitch with exactly three main sections:

```markdown
# Pitch: [Name]

## Problem
[Who encounters what problem, in which concrete situation, and the desired outcome.]
[Evidence, consequential assumptions, and appetite or other constraints; mark unknowns.]

## Solution
[Rough approach, core elements, fit with the existing product, and the user journey.]
[Key decisions, exclusions, risks, and unresolved conceptual questions.]

## Scopes
### [User-facing scope]
- Outcome: [What the user can accomplish.]
- Boundary: [Included, narrowed, and excluded behavior.]
- Connections: [Dependencies, shared concepts, or scopes that deliver value together.]
- Resolve next: [Question and the interview, sketch, prototype, or evidence needed to answer it; omit if none.]

[Useful order and why. State whether enough is understood to sketch or prototype, and what remains unresolved.]
```

Keep assumptions and questions in the section they affect rather than adding a fourth section. Omit empty fields; do not pad the pitch to imply certainty. Keep visual detail open unless it affects the concept or interaction. Provide the detailed Shape Map when explicitly requested or needed to expose relationships; produce a Shape Prompt only for a requested planning or execution handoff.

## Readiness and Stopping

- **Enough to sketch:** The problem and desired outcome are clear enough, a plausible direction is bounded, and the areas to draw and questions those drawings should resolve are named.
- **Enough to prototype:** The core journey can be traced coherently, essential boundaries and relationships are explicit, and remaining uncertainty can be investigated safely within the proposed prototype. Call out assumptions that could overturn the concept or viability instead of declaring them resolved.

Pause the interview at the useful next action. Distinguish uncertainty that needs resolving before proceeding from uncertainty best investigated through a sketch or prototype. Do not equate readiness with a complete specification, verified demand, or production readiness. Do not require sketches when a prototype is the better next move. If drawing tools such as tldraw are available and the user requests drawing, use the scopes and questions to guide the canvas; the skill must also work without a drawing connection.

## Quality Bar

A strong result asks consequential questions without exhausting the user, preserves the five shaping steps, produces a concise Problem / Solution / Scopes pitch, defines recognizable user value, subtracts meaningful scope, makes relationships and order visible, fits the existing product's concepts, retains uncertainty, and explains the next useful action. Returned sketches or prototypes should improve the same pitch rather than create a disconnected specification.
