---
name: map-product-anatomy
description: Turn a software product surface or flow into a compact, versionable anatomy of Screens, Components, Actions, States, and Flows using Anatomica. Use when product structure needs to become inspectable before pixels, code, or detailed implementation.
metadata:
  author: drewbarontini
  version: "0.1.0"
  systems: "claritorium, equilio"
  models: "clarity-codex, value-creation"
---

# Map Product Anatomy

Given a software product surface, workflow, or slice, use Anatomica to make its structure and behavior inspectable as text without prematurely specifying implementation.

## Boundaries

Map the product that is supported by the supplied evidence. Do not invent screens, states, actions, or flows to make the map look complete. Preserve assumptions and unknowns explicitly.

This Skill describes product anatomy; it does not replace product discovery, visual design, technical architecture, or implementation planning.

## Grammar

```text
[Screen]::Component.SubComponent@state.action() => [dest] | ::Component | .action() | @state
```

Read [references/anatomica.md](references/anatomica.md) for the notation and source conventions.

## Method

1. **Set the boundary** — Name the product surface, workflow, or slice being mapped. Do not imply full-product coverage when only part of the system is known.
2. **Identify Screens** — Capture top-level product surfaces and contexts with `[Screen]`.
3. **Decompose Components** — Represent structural parts with `::Component`. Nest only when hierarchy clarifies containment.
4. **Expose States** — Add `@state` where rendering or behavior materially changes. Put the state at the narrowest level that owns it.
5. **Attach Actions** — Represent user or system behaviors with `.action()`. Prefer stable product verbs over implementation events.
6. **Connect Flows** — Use `=>` to make movement between screens, components, actions, or states explicit.
7. **Normalize the language** — Keep names consistent across repeated objects and behaviors. Prefer the smallest notation that preserves the real structure.
8. **Check against reality** — Identify missing transitions, contradictory states, unclear ownership, or unsupported assumptions rather than filling them in speculatively.

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
