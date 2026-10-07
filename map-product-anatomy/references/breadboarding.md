# Breadboarding from Anatomica

Use this reference for the optional continuation **Pitch → Anatomica → Breadboard → Revise**. The grammar remains defined in [anatomica.md](anatomica.md); a breadboard is another representation of the same product structure, not new notation or a detailed visual specification.

## Start from the Scoped Experience

Read the pitch or source context before drawing. Preserve scope names, intended user value, boundaries, and unresolved questions. Map only the supported screens, components, actions, states, and flows; distinguish existing behavior from proposed intent.

For several scopes, show where each begins and ends and where it shares a screen or component with another scope. Scope rows or panels can make progression legible. Prefer one shared representation of a screen; if separate scope panels repeat it for legibility, identify those as views of the same screen. Do not introduce duplicate product concepts to make isolated diagrams look complete.

## Translate the Structure

| Anatomica element | Breadboard representation |
| --- | --- |
| Screen | Place represented by an underlined heading or labeled container for a top-level surface or context. |
| Component | Labeled affordance or structural part beneath or within its owning place or component. |
| Action | Label on the relevant affordance or its outgoing arrow. |
| State | Annotation or distinct view of the owning screen/component when behavior meaningfully changes. |
| Flow | Directed arrow from the triggering action to its supported destination. |

Keep the anatomy's names identifiable in the drawing. Use only the affordances necessary to understand the flow. Positions should communicate ownership and connections; they do not settle the final visual layout.

A lightweight text style uses underlined place names, plain affordance labels beneath them, and muted annotations for displayed information, conditions, and consequences. Connect arrows to the specific affordance rather than the whole place; the action label may be on the affordance or arrow without duplicating it. Label supported conditional branches near their paths. Keep annotations visually distinct from controls, using a small legend when needed. Underlines, boxes, and colors are presentation choices, not additional Anatomica syntax or required UI design.

A place heading may name a Screen, a component such as a modal, or a state view; preserve its Anatomica identity. For example, ProjectDetail and ProjectDetail (task added) can be views of the same Screen. Identify the changed state without inventing a second screen or implying navigation where only an in-place update occurs.

An arrow may navigate to a Screen, open or focus a Component, chain an Action, or change a State. Preserve that destination type. A modal can be shown inside or beside its screen for legibility, but label it as a component of that screen. Do not promote it to a Screen or invent a navigation arrow for an in-place state change.

If an Action has no supported destination, show the affordance and place a question beside it. Do not invent a success screen, error state, or route. Candidate answers may be drawn when exploration is requested, with each alternative explicitly identified as provisional.

## Draw in the Requested Medium

With an available drawing connector such as tldraw, use its current tools and documentation to render the breadboard. Inspect the target before updating an existing board and preserve unrelated content. Reuse the mapped area where possible so revisions stay recognizable.

With paper or an unavailable connector, provide a compact drawing guide based on the same places, affordances, action labels, and questions. State what was actually produced. Tool choice does not change the method or become a prerequisite for shaping.

When rendering programmatically, inspect the resulting drawing using the tool's available view or readback. Check readable labels, component ownership, arrow attachment to the intended affordance and destination, and visible uncertainty. Do not treat successful shape creation alone as proof that the diagram communicates the flow.

## Trace and Revise

Trace a concrete journey from entry to useful outcome, including supported branches, overlays, state changes, and connections across scopes. Compare the visual path with the text map and pitch. Identify missing transitions, ambiguous actions, contradictory concepts, or newly discovered dependencies.

Correct rendering mistakes in the drawing. When supplied sketches or discussion change the intended behavior, revise the anatomy and drawing together. If the change affects the problem, solution, value boundary, or release independence, revise the corresponding parts of the same pitch as well. Preserve scope names unless the scope's meaning changes; explain a consequential rename.

Keep unresolved choices visible and distinguish a proposed resolution from an accepted decision. Neither text completeness nor a coherent diagram proves demand, feasibility, or successful user interaction. End with the smallest useful next question, sketch, or prototype rather than filling every gap speculatively.

See [the scoped breadboard example](../examples/scoped-breadboard.md) when shared-screen ownership, modal states, or the revision loop need a concrete illustration.
