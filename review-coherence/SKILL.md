---
name: review-coherence
description: Review a product experience, design, feature, workflow, or related artifact for meaningful drift, inconsistency, model gaps, and contradictions. Use to protect the coherence of the whole and recommend the smallest meaningful corrections, not for subjective aesthetic critique.
metadata:
  author: drewbarontini
  version: "0.1.0"
  systems: "claritorium, equilio"
  models: "quality-refinement"
---

# Review Coherence

Given a product artifact and enough surrounding context, determine whether its concepts, language, behavior, and value form a legible whole for its interpreter.

## Boundaries

Review the artifact in context, not as an isolated screen or local implementation. Ground findings in comparable behavior, stated intent, user evidence, or contradictions visible in the artifact. Do not default to personal taste, trend-based critique, pixel polish, or speculative redesign.

If the surrounding product model is unavailable, distinguish observed internal contradictions from comparisons that still need evidence.

## Method

1. **Establish intent and interpreter.** State what the artifact is for, who must make sense of it, and what evidence is available.
2. **Find internal rules.** Identify the concepts, terms, states, actions, and feedback the artifact teaches.
3. **Compare similar things.** Check whether similar objects and actions look, behave, and are named similarly—and whether different things are distinguishable.
4. **Trace the user's mental model.** Predict what a user would expect, compare it with the product's actual model, and diagnose Model Mismatch rather than implementing feedback literally.
5. **Look across seams.** Check transitions, empty/loading/error/success states, permissions, entry and exit points, and connections to the rest of the product.
6. **Test whole-product fit.** Ask whether a locally reasonable solution introduces duplicate concepts, contradictory patterns, terminology drift, or complexity that weakens the whole.
7. **Prioritize meaningful gaps.** Rank by interpretive or systemic consequence, not visual conspicuousness.
8. **Recommend the smallest correction.** Prefer removal, simplification, reuse, or alignment with an existing rule before adding a new pattern.

Read [references/coherence-lenses.md](references/coherence-lenses.md) for review lenses and finding types.

## Output

```markdown
## Coherence Assessment
[Overall judgment, scope, interpreter, and evidence limits.]

## Findings
### [Finding]
- Evidence: [...]
- Coherence gap: [behavior | terminology | concept | model mismatch | flow | whole-product drift]
- Why it matters: [...]
- Smallest meaningful correction: [...]
- Confidence: [high | medium | low]

## Cross-Cutting Pattern
[What the findings reveal about the system as a whole; omit if none.]

## Preserve
- [What is already coherent and should remain.]

## Open Questions
- [Evidence needed before changing the artifact.]
```

## Quality Bar

A strong review shows evidence, compares against a discernible rule or model, distinguishes systemic coherence from aesthetic preference, explains user and product consequences, notices AI-accelerated local drift where present, and recommends focused corrections that strengthen the whole without unnecessary redesign.
