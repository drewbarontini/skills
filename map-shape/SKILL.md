---
name: map-shape
description: Shape a fuzzy product problem into a concise Problem / Solution / Scopes pitch through adaptive interviewing and sketch or prototype feedback. Use when work needs a clear problem, rough solution, and named scopes of independently releasable user value before implementation planning.
metadata:
  author: drewbarontini
  version: "0.3.0"
  systems: "claritorium, equilio"
  models: "value-creation"
---

# Map Shape

Given an initial understanding of a product problem, develop a bounded, coherent pitch that makes the next sketch or prototype useful. Use an adaptive interview to discover what matters, preserve unresolved questions, and refine the same pitch as new evidence appears.

## Boundaries

Shape the user experience before specifying implementation. Do not invent requirements, evidence, or settled decisions to complete the document. This skill clarifies existing understanding; it does not replace user research, feasibility testing, detailed technical planning, estimation, or code generation. If an answer needs contact with reality, identify the smallest useful sketch, prototype, or evidence-gathering action rather than prolonging the interview.

## Interview and Synthesis

1. **Orient from what is supplied.** Read the initial notes and any existing pitch, sketches, or prototype. Reflect the apparent problem, proposed direction, constraints, and most consequential uncertainty. Separate observations, assumptions, proposals, and decisions.
2. **Ask the next useful question.** Ask one focused question at a time, or a small pair when inseparable, then wait for the answer. Choose the question whose answer could most change the problem, solution, or boundary. Do not repeat answered questions or run a fixed questionnaire. Probe concrete situations, desired outcomes, problem size (reach, frequency, or consequence), product fit, appetite, and gaps in the user's journey as needed. Do not invent counts or quantify what the evidence cannot support.
3. **Contribute judgment.** Offer provisional interpretations, smaller alternatives, and tradeoffs grounded in the supplied context. Explain why a choice matters. Challenge a proposed feature when the underlying problem or value is unclear; do not silently convert a suggestion into a requirement.
4. **Synthesize as understanding changes.** Keep a living pitch rather than waiting for exhaustive certainty. Briefly reflect consequential decisions and remaining uncertainty. If the supplied context is already sufficient, draft directly and ask only questions that materially affect the shape.
5. **Use sketches and prototypes inside the loop.** When a spatial or interactive question would benefit from drawing, name the area and what the sketch should resolve. When sketches or a prototype return, trace the user journey, compare it with the pitch, expose contradictions or missing transitions, and revise the same pitch. Do not restart the interview or treat a drawn choice as validated user evidence.

## Canonical Method

Use these five steps to develop the shape, revisiting earlier steps as answers and artifacts change it. They guide the reasoning; they do not require five separate interview rounds or five output sections.

1. **Surface** — Create a flat list of everything. Tag each item as Action, Decision, Question, Risk, or Unknown. Nothing is in or out of scope yet.
2. **Structure** — Build relationships in the list. Anchor root nodes, nest sub-items, and link dependencies. Discover relational groups rather than imposing an operational plan.
3. **Slice** — Define each scope as independently releasable, usable end-user value on top of the product already available. Ask: if this scope shipped and work stopped here, could someone complete something useful? Combine pieces that need each other before providing value into one scope. A scope may depend on an earlier released scope; it must not depend on a future scope to become useful. Give it a stable, Title Case, two- or three-word name suitable for milestones and shared feature language, followed by an action-oriented shorthand.
4. **Simplify** — Reduce each slice to the smallest version that still delivers value. Remove, defer, or narrow scope explicitly.
5. **Sequence** — Order scopes by value and dependencies, and identify the useful next sketch or prototype. Distinguish build units from value units: backend preparation or work behind a feature flag may ship before a scope is available, but production deployment alone does not deliver the scope. Keep such staging inside that scope's optional Delivery notes.

Read [references/shape-mapping.md](references/shape-mapping.md) when a detailed Shape Map, slice-independence test, or implementation-planning handoff is useful.

## Output

The default output is a living pitch with exactly three main sections. Use H1 for Problem, Solution, and Scopes, H2 for each scope name, and H3 for sections within a scope. The feature name can be the document title.

```markdown
# Problem

[One or two sentences: who encounters what difficulty, in which situation, and why it matters. Convey reach, frequency, or consequence when supported.]

# Solution

[One short paragraph: the high-level approach and core behavior, fitting the existing product.]

## Constraints

- [Feature-wide limits, appetite, or exclusions; omit this subsection when unnecessary.]

## Tradeoffs

- [What is deliberately accepted by choosing this approach and why; omit when unnecessary.]

## Open Questions

- [Consequential unresolved questions, identifying the affected scope when useful; omit when empty.]

# Scopes

[Order by useful releases; explain dependencies or deferrals briefly only when needed.]

## [Scope Name]

*[Action-oriented shorthand.]*

[One or two sentences describing what users can accomplish after this scope is released and the value it provides.]

### Boundaries

- **Includes:** [Behavior necessary to deliver that value.]
- **Excludes:** [Nearby behavior deliberately outside this scope.]

### Constraints

- [Scope-specific dependencies or limits; omit when unnecessary.]

### Delivery

- [Staging, flags, or preparatory steps worth making explicit; omit when unnecessary.]
```

Keep Problem to one or two sentences and Solution to one short paragraph before any optional subsections. Constraints state limits; Tradeoffs explain accepted consequences; Open Questions preserve uncertainty. Do not add a subsection merely for symmetry or repeat feature-wide content within each scope.

For each scope, use a memorable, compressed name without cryptic branding; let the shorthand explain the capability immediately. Keep names stable across the pitch, sketches, and milestones. Description and Boundaries are standard; scope Constraints and Delivery are optional. Omit unsupported or empty fields instead of filling them with invented decisions. Do not restore the old Outcome / Connections / Resolve next checklist. Put consequential assumptions and questions under Solution, and state the next action or readiness briefly with the pitch rather than adding a fourth main section.

Keep visual detail open unless it affects the concept or interaction. Provide the detailed Shape Map when explicitly requested or needed to expose relationships; apply the same user-value release test to its slices. Produce a Shape Prompt only for a requested planning or execution handoff.

## Readiness and Stopping

- **Enough to sketch:** The problem and desired outcome are clear enough, a plausible direction is bounded, and the areas to draw and questions those drawings should resolve are named.
- **Enough to prototype:** The core journey can be traced coherently, essential boundaries and relationships are explicit, and remaining uncertainty can be investigated safely within the proposed prototype. Call out assumptions that could overturn the concept or viability instead of declaring them resolved.

Pause the interview at the useful next action. Distinguish uncertainty that needs resolving before proceeding from uncertainty best investigated through a sketch or prototype. Do not equate readiness with a complete specification, verified demand, or production readiness. Do not require sketches when a prototype is the better next move. If drawing tools such as tldraw are available and the user requests drawing, use the scopes and questions to guide the canvas; the skill must also work without a drawing connection.

## Quality Bar

A strong result asks consequential questions without exhausting the user, preserves the five shaping steps, keeps Problem and Solution tight, and defines named scopes of independently releasable user value. It subtracts meaningful scope, makes boundaries and order visible, distinguishes deployment from delivered value, fits existing product concepts, retains uncertainty without padding sections, and explains the next useful action. Returned sketches or prototypes should improve the same pitch rather than create a disconnected specification.
