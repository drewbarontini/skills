---
name: frame-inquiry
description: Frame or reframe an Inquiry from ambiguity, a Signal, tension, assumption, or partially formed idea. Use when the current question, Working Theory, or next learning move needs clarification.
metadata:
  author: drewbarontini
  version: "0.1.0"
  systems: "claritorium, knowflow"
  models: "inquiry-formation"
---

# Frame Inquiry

Given an ambiguous situation, meaningful Signal, or existing Inquiry, clarify the Current Inquiry, Working Theory, and Next Move so the investigation can continue across thinking environments.

## Boundaries

Use this skill when understanding must precede an answer. Do not use it to decorate a decided solution with a question, conduct the investigation, or answer the Inquiry prematurely.

If the input is a straightforward factual question with a known retrieval path, answer it directly. If it is only a broad topic, find the tension or uncertainty before framing the Inquiry.

When reframing an existing Inquiry, read its current state and relevant Sources and Working Material first. Preserve its identity, relationships, and useful context; revise the framing where the supplied evidence warrants it. This skill frames the investigation rather than conducting it.

## Method

1. **Preserve the Signal.** State what was observed, experienced, or reported without adding a cause.
2. **Separate interpretation.** Identify conclusions, explanations, or judgments already layered onto the observation.
3. **Remove solution capture.** Rewrite requests framed around a proposed feature or remedy so the underlying problem remains open.
4. **Expose assumptions.** Separate what is believed from what evidence currently supports.
5. **Find the live uncertainty.** Ask what, if learned, could materially change understanding or the next decision.
6. **Set a useful boundary.** Name the population, context, behavior, or time window only when it improves investigability.
7. **Frame the Current Inquiry.** Prefer an open question that reality can inform. When revisiting an Inquiry, explain any material change in the question or Working Theory. Avoid questions so broad they cannot guide a next move or so narrow they merely confirm a belief.
8. **Choose the next move.** Identify the smallest action likely to improve the Working Theory. When useful, choose the Thinking Space and Thinking Mode that best support the action. If cognitive work is not enough and contact with reality is required, the Next Move may become a bounded Experiment; do not design the full Experiment unless requested.

Read [references/thinking-spaces.md](references/thinking-spaces.md) when Space or Mode would clarify the Next Move, or when deciding whether further cognitive work or an Experiment would help most.

## Output

```markdown
## Current Inquiry
[One focused, open, investigable question.]

## Working Theory
[Current belief, explicitly provisional; if none is supported yet, say so.]

## Next Move
[The smallest action likely to improve the Working Theory.]

## Signal
[Observation or tension that led here; include when useful.]

## Assumptions and Evidence
- Assumption: [...]
- Evidence: [...]
- Unknown: [...]

## Boundary
[Relevant context, population, or scope; omit if unnecessary.]

## Sources
[Relevant sources and links, when available.]

## Working Material
[Relevant excerpts, quotes, notes, or other developing material; link rather than copy when useful.]
```

Keep Current Inquiry, Working Theory, and Next Move as the core state, with enough context to understand them. Use the other fields only when they add investigative value. Sources identify what is being engaged with; Working Material holds what was extracted or developed along the way. Neither automatically qualifies as durable Knowledge. Preserve source provenance and retain only the context needed for continuity.

Next Move remains the primary action output; Space and Mode are optional orientation, not additional required Markdown headings. If useful, mention them within Next Move. When an execution environment exposes equivalent structured fields, populate optional `Active Space` and `Active Mode` only when clearly implied by the action.

## Quality Bar

A strong Inquiry:

- grows from a concrete Signal or clearly named uncertainty;
- distinguishes observation from interpretation and assumption from evidence;
- investigates the problem rather than validating a proposed solution;
- is open enough to discover something unexpected and bounded enough to guide evidence gathering;
- could change the Working Theory or next decision; and
- resists answering itself.

For an existing Inquiry, a strong result makes the changed understanding visible without creating a duplicate record or accumulating every temporary artifact.
