---
name: map-product-anatomy
description: Map a product surface, flow, or shaped feature into compact Anatomica, with an optional breadboard of screens, affordances, and action-labeled transitions. Use when product structure and flow need to become inspectable before visual design or implementation.
metadata:
  author: drewbarontini
  version: "0.2.2"
  systems: "claritorium, equilio"
  models: "clarity-codex, value-creation"
---

# Map Product Anatomy

Given a software product surface, workflow, or shaped feature, use Anatomica to make its structure and behavior inspectable as text. When a structural drawing is useful and requested, translate that anatomy into a breadboard and use what it reveals to revise the anatomy and any source pitch.

## Boundaries

Map the product that is supported by the supplied evidence. Do not invent screens, states, actions, or flows to make the map look complete. Preserve assumptions and unknowns explicitly.

For a proposed feature, map supported intent from its pitch and scopes as provisional structure, distinguishing existing behavior, proposed decisions, and unresolved choices. A complete-looking map or drawing does not establish user demand or validate the proposal.

This Skill describes product anatomy; it does not replace product discovery, visual design, technical architecture, or implementation planning.

## Grammar

```text
[Screen]::Component.SubComponent@state.action() => [dest] | ::Component | .action() | @state
```

Read [references/anatomica.md](references/anatomica.md) for the notation and source conventions.

## Method

1. **Set the boundary** — Name the product surface, workflow, or slice being mapped. When starting from a pitch, read its scopes, boundaries, and Open Questions; preserve the scope names and identify which parts of the anatomy each covers. Make shared surfaces and connections between scopes visible. Do not imply full-product coverage when only part of the system is known.
2. **Identify Screens** — Capture top-level product surfaces and contexts with `[Screen]`.
3. **Decompose Components** — Represent structural parts with `::Component`. Nest only when hierarchy clarifies containment.
4. **Expose States** — Add `@state` where rendering or behavior materially changes. Put the state at the narrowest level that owns it.
5. **Attach Actions** — Represent user or system behaviors with `.action()`. Prefer stable product verbs over implementation events.
6. **Connect Flows** — Use `=>` to make movement between screens, components, actions, or states explicit.
7. **Normalize the language** — Keep names consistent across repeated objects and behaviors. Prefer the smallest notation that preserves the real structure.
8. **Check against reality** — Identify missing transitions, contradictory states, unclear ownership, or unsupported assumptions rather than filling them in speculatively. For proposed work, check against the supplied intent and boundaries while keeping unvalidated choices provisional.

## Optional Breadboard

Read [references/breadboarding.md](references/breadboarding.md) when the user wants a breadboard or a structural drawing of the flow.

1. **Translate the anatomy.** Show places with underlined headings or labeled containers, relevant Components and affordances beneath their owning place, and supported Flows as arrows originating from the relevant affordance and labeled with their Actions. Use brief annotations for displayed information, conditions, and consequences. Retain meaningful States at their owning screen or component; a distinct view of the same place is not a new Screen. A modal stays a component, and a state transition need not lead to another screen.
2. **Preserve identity and uncertainty.** Keep product and scope names aligned across pitch, text, and drawing. Show shared screens and cross-scope connections. Keep missing destinations or unsettled behavior visibly unresolved instead of drawing invented answers.
3. **Create the editable breadboard.** A breadboard request calls for an actual editable canvas, preferably in tldraw; use Excalidraw when tldraw is unavailable, or another medium explicitly chosen by the user. Use an available connector or supported native-file workflow, then inspect the result and provide its link or file. Keep placement schematic and detail limited to structure and flow. If neither tool can produce the canvas, explain the access limitation and leave the drawing incomplete; text guidance alone does not fulfill the breadboard request. Text-only anatomy remains valid when no breadboard is requested.
4. **Trace and reconcile.** Walk through the user journey in the breadboard. Check labels, containment, and arrow endpoints against the anatomy. Use supplied discoveries or decisions to revise the same anatomy and pitch, explaining consequential changes to the problem, approach, or scopes. Proposed alternatives remain marked as alternatives until chosen; drawing them is not evidence of demand.

## Output

```text
# Scope: [surface or flow]

[Screen]
  ::Component
    @state
      .action() => [Destination]
```

After the notation, include:

```markdown
## Assumptions
- [...]

## Unknowns
- [...]

## Observations
- [Only meaningful structural inconsistencies or gaps exposed by the map.]
```

Omit empty sections.

The Anatomica map remains the primary output. A requested breadboard is an editable canvas companion to that map, with scope associations and unresolved questions retained and its link or native file provided. Keep the source pitch's Problem / Solution / Scopes format; the anatomy and breadboard are separate working artifacts, not extra pitch sections. Include a brief account of meaningful gaps or changes when the drawing reveals them.

## Quality Bar

A strong product anatomy:

- is legible as plain text;
- uses Anatomica consistently;
- distinguishes Screens from Components and States from Actions;
- makes important transitions explicit;
- represents only supported product behavior;
- keeps naming stable across the map;
- surfaces uncertainty rather than hiding it; and
- is compact enough to diff and evolve alongside the product.

A strong breadboard preserves the anatomy's identities and uncertainty, makes affordances and action-labeled connections legible, and reveals gaps without implying a detailed interface design. Revisions should keep the pitch, anatomy, and drawing aligned.
