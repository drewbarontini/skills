# Coherence Review Lenses

Use only the lenses relevant to the artifact.

## Product Intent

- Does the artifact make its essential value visible?
- Does added surface area serve that value or obscure it?
- Is the local solution aligned with the broader product direction?

## Concepts and Terminology

- Does one concept have multiple names?
- Does one name refer to different concepts?
- Has a new local abstraction duplicated an existing one?
- Do labels reflect the model the product actually uses?

## Behavior and Interaction

- Do similar things behave similarly?
- Are differences meaningful and perceivable?
- Are controls, defaults, consequences, and reversibility consistent?
- Do states and feedback explain what happened?

## Model Mismatch

Model Mismatch occurs when feedback or predicted behavior conflicts with the system's actual behavior, revealing a gap between the person's mental model and the product's model.

Treat feedback as evidence of understanding, not a specification. Verify whether the system is defective, the interface teaches the wrong model, terminology imports a conflicting convention, or the person lacks necessary context. Then correct the smallest source of mismatch.

## Flow and Seams

- Are entry, transition, and exit points continuous?
- Do empty, loading, error, success, and permission states follow the same conceptual rules?
- Does the artifact preserve context across handoffs?
- Does a locally complete feature become incomplete in the full journey?

## Whole-Product Drift

- Have repeated local solutions produced parallel patterns for the same job?
- Is the product accumulating rather than integrating?
- Would subtraction or reuse create a more coherent whole?
- Has accelerated output outrun shared understanding, judgment, or review?

## Finding Types

- **Contradiction** — two rules cannot both be understood as true.
- **Inconsistency** — comparable elements follow different rules without meaningful reason.
- **Model gap** — the product does not make a necessary concept or relationship legible.
- **Model Mismatch** — the interpreter's expectation conflicts with the system's model.
- **Drift** — accumulated local changes weaken continuity across the whole.
- **Friction** — the model may be coherent, but effort or interruption obscures value.

## Canonical Sources

- `equilio/models/quality-refinement.md` — surface the signal, move with shared context, increase the contrast.
- `equilio/patterns/product-equilibrium.md` — creation/refinement imbalance and whole-product review.
- [Product Equilibrium](https://drewbarontini.com/newsletter/64-product-equilibrium/) — Experience Unification and Editorial Passes.
- [Pattern Library](https://drewbarontini.com/patterns/) — Model Mismatch.
