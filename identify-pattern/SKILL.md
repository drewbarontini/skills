---
name: identify-pattern
description: Turn observations, repeated experiences, tensions, stories, or examples into a transferable Pattern. Use when recurrence may reveal a relationship worth preserving; do not use to generalize a single unsupported anecdote or merely summarize a topic.
metadata:
  author: drewbarontini
  version: "0.2.0"
  systems: "claritorium, knowflow"
  models: "inquiry-formation, knowledge-integration"
---

# Identify Pattern

Given meaningful experience or observations, identify a recurring relationship, test whether it transfers, and articulate a Pattern that can guide understanding and action.

## Use This Skill When

- A Signal, story, tension, or repeated experience seems to contain a durable relationship.
- Several examples appear related, but the transferable meaning is not yet clear.
- A team wants to understand why something keeps happening or what can be applied elsewhere.

Do not use this skill merely to summarize, categorize topics, name a one-time event, or turn a preference into a universal rule. If recurrence is not supported, preserve the input as a Signal or frame an Inquiry instead of claiming a Pattern.

## Method

1. **Preserve the experience.** Extract concrete observations and examples before interpreting them. Mark inferred claims as interpretations.
2. **Find recurrence.** Look for the relationship that repeats—not just a repeated subject, phrase, outcome, or theme. Ask what changes with what, what enables what, or what tension keeps reappearing.
3. **Separate instance from relationship.** Remove details that only belong to the originating case while retaining the conditions that make the relationship true.
4. **Test transferability.** Check the candidate against at least two contexts when evidence permits. Look for a counterexample, boundary, or condition that would make the claim too broad.
5. **Distill the meaning.** Write the descriptive Pattern first. Then derive its Philosophy, Principle, and contextual Practices without collapsing these layers together.
6. **Name it.** Use a concise two- or three-word noun phrase that names the Pattern as a reusable concept. Prefer two words when they preserve the meaning; use three when the distinction requires it. Avoid sentences, claims, instructions, questions, and slogans. The title names the concept; the Pattern statement describes the relationship. Read the title aloud in the construction **“the [Name] Pattern.”** If that phrase does not sound natural, the name is not finished. Prefer clarity and useful rhythm over novelty, branding, alliteration, or an acronym.
7. **Compress only if helpful.** Add a Formula only when it makes the relationship easier to understand. Do not add mathematical decoration to a qualitative idea.

Read [references/pattern-anatomy.md](references/pattern-anatomy.md) when the layers are difficult to separate, evidence is weak, or Pattern maturity or promotion is being assessed.

## Output

Use this form when a supported Pattern is present:

```markdown
# [Name]

## Pattern
[The recurring, transferable relationship.]

## Philosophy
[Why recognizing this relationship matters.]

## Principle
[What should generally guide judgment or action.]

## Practice
- [A contextual way to act on the Principle.]

## Formula
[Optional compressed representation. Omit when it adds no clarity.]

## Evidence and Boundaries
- Originating examples: [...]
- Transfer contexts: [...]
- Conditions or limits: [...]
- Confidence: [supported | tentative]
```

Keep the core Pattern usable without the evidence section, but retain enough traceability to show that the abstraction is earned.

If the evidence is insufficient, output:

- **Candidate Pattern** — the tentative relationship, clearly labeled.
- **What supports it** — the available observation or examples.
- **What is missing** — recurrence, transfer evidence, or boundary conditions.
- **Next Inquiry** — a question that could test the candidate.

## Maturity and Promotion

Emerging and Developing are candidates; Established is the full Pattern threshold. Canonical is a rare architectural designation for an Established Pattern, not a higher quality score. Promotion requires recurrence, transferability, evidence and boundaries, complete articulation, and a distinct contribution, plus a meaningful structural contribution through synthesis, support for a Model, or independently durable understanding. A Model relation alone is neither required nor sufficient. Use the detailed criteria and promotion check in the reference before assessing readiness to publish; do not infer maturity from age or accumulated attention.

## Quality Bar

A strong result:

- abstracts beyond the originating example without erasing important conditions;
- names an actual relationship rather than a topic, category, slogan, or isolated outcome;
- transfers across contexts and acknowledges credible limits;
- keeps Pattern descriptive, Philosophy interpretive, Principle prescriptive, and Practice contextual;
- has a clear, memorable, non-gimmicky two- or three-word noun-phrase name that reads naturally as **“the [Name] Pattern”**; and
- uses a Formula only when the compression preserves meaning.
