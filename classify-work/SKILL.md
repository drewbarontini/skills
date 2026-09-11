---
name: classify-work
description: Give product work clear coordinates by identifying its Type, Impact, Product Landscape location, work form, and routing state. Use when an item needs to become legible before prioritization, grouping, or movement through a Work Registry.
metadata:
  author: drewbarontini
  version: "0.1.0"
  systems: "claritorium, equilio"
  models: "value-creation, strategic-momentum"
---

# Classify Work

Given a product work item and available context, state what kind of work it is, why it matters, where it lives, and how it should move. Classification creates understanding, not a commitment to execute.

## Required Discipline

- Choose exactly one **Type**: Idea, Task, Fix, Improvement, or Bet.
- Describe **Impact** from supplied evidence. Do not invent a scoring scale, magnitude, or priority.
- Map **Landscape** using an existing Product Landscape: Region → Zone → Context. Do not fabricate product taxonomy.
- Add a **Work Form** only when the item belongs to a larger container: Batch, Stream, or Project.
- Recommend a **Route** from the established lanes when enough context exists.

Read [references/work-taxonomy.md](references/work-taxonomy.md) before classifying ambiguous items, grouped work, or routing.

## Method

1. Clarify the title and one-sentence description enough to understand the work.
2. Determine Type from the item's current intent and certainty—not its size, urgency, or eventual destination.
3. State Impact: who or what is affected, what changes if the work is done or ignored, and what evidence supports that judgment.
4. Locate the item in the supplied Landscape at the deepest supported level.
5. Determine whether it is standalone, part of a Batch, an Experiment within a Stream, or work within a committed Project.
6. Recommend its current Route: Triage, Radar/Backlog, Queue, In Progress, In Review, or Done. Use Canceled, Duplicate, or Deleted when appropriate.
7. Explain ambiguity and likely reclassification triggers. Work can evolve as understanding increases.

## Output

```markdown
## Work Classification
- Title: [...]
- Type: [Idea | Task | Fix | Improvement | Bet]
- Impact: [affected people/system, consequence, and evidence]
- Landscape: [Region → Zone → Context | unresolved]
- Work Form: [Standalone | Batch | Stream | Project | unresolved]
- Route: [Triage | Radar/Backlog | Queue | In Progress | In Review | Done | Canceled | Duplicate | Deleted]

## Rationale
[Brief explanation, including ambiguous alternatives.]

## Missing Context
- [...]

## Reclassify When
- [New information or decision that would change the coordinates.]
```

Keep the result compact. Omit explanatory sections when the classification is unambiguous.

## Quality Bar

A strong classification uses the established taxonomy, distinguishes Type from Impact and routing, maps rather than invents the Landscape, treats classification as current and revisable, explains ambiguous cases, and gives downstream people or agents enough context to place and move the work coherently.
