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

Ask: **If this scope shipped and work stopped here, could someone complete something useful?** Each scope must provide independently releasable, usable end-user value on top of the product already available. Dependencies on earlier released scopes are valid; dependency on future work for basic usefulness is not. Combine interdependent pieces into one scope. Database, API, and interface layers are usually build units within a scope, not separate scopes.

Name each scope with a compressed, memorable, Title Case, two- or three-word name, followed by a plain action-oriented shorthand. For example: **View Recall** — *Save and return to a view.* Keep the name stable as milestone and feature language; naming does not make the scope a canonical Pattern.

## Simplify

Ask: **What is the smallest version of each slice that still delivers value?**

Show subtraction. Mark which states, fields, controls, permissions, variants, or edge cases are deferred and why the reduced slice remains useful. Cheap execution is not evidence that added scope is valuable.

## Sequence

- **Build units** are pieces that can be implemented or deployed separately, including backend preparation and work behind flags.
- **Value units** are the scopes that can be released to create usable end-user value.

Sequence scope releases by value and dependencies. Keep technical staging in optional Delivery notes within its scope. Preparatory changes can be live in production before the scope is exposed to users; deploying those changes does not count as delivering the scope's value. Combine pieces that only become valuable together into one scope rather than presenting them as separate scope releases.

## Detailed Shape Map

Use this form when a detailed map is requested or the relationships need more visibility than the default pitch provides. The five shaping steps remain the method; this is an optional representation of the same understanding.

```markdown
# Shape: [Name]

## Context
[Problem, opportunity, user value, evidence, appetite, and constraints.]

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
### [Scope Name] — [Action-oriented shorthand]
- Value: [...]
- Boundary: In [...]; Out [...]
- Dependencies: [...]
- Independence test: [Useful if released on top of the existing product and no further work follows.]

## Simplification
- Keep: [...]
- Reduce: [...]
- Defer / remove: [...]

## Sequence
1. [Scope release, with any preparatory build units distinguished] — because [...]

## Remaining Uncertainty
- [Question, consequence, and next action.]
```

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
