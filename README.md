# Skills

Portable AI Agent Skills derived from [Claritorium](https://github.com/drewbarontini/claritorium) and [Equilio](https://github.com/drewbarontini/equilio).

This repository is an executable capability layer. It operationalizes recurring work from those bodies of knowledge; it does not reproduce or replace their Systems and documentation.

## The Knowledge Architecture

- **Systems** organize understanding.
- **Models** explain reality.
- **Patterns** capture recurring transferable relationships.
- **Skills** perform recurring jobs.

The atomic unit of a Skill is:

> Given this kind of input, perform this transformation, and produce this recognizable output.

A Skill belongs here only when an agent can recognize its trigger, perform one primary job with a repeatable method, produce a concrete output, and evaluate the result by observable qualities.

## Provenance

Claritorium and Equilio are the canonical sources. Individual Skills declare relevant Systems and Models in `SKILL.md` metadata; provenance is many-to-many and does not determine the repository structure. Supporting references summarize only the context needed to perform the job and link back to canonical material where useful.

The repository follows the open [Agent Skills specification](https://agentskills.io/specification). Metadata values are strings for compatibility with the specification, including comma-separated provenance when a Skill draws from multiple sources.

## Skill Catalog

| Skill | Job |
| --- | --- |
| [`identify-pattern`](identify-pattern/) | Turn observations or repeated experience into a tested, transferable Pattern. |
| [`frame-inquiry`](frame-inquiry/) | Frame or reframe an Inquiry's Current Inquiry, Working Theory, and Next Move. |
| [`design-experiment`](design-experiment/) | Design a bounded test of a Working Theory with a review handoff back to the Inquiry. |
| [`compare-perspectives`](compare-perspectives/) | Use genuinely distinct perspectives to expose tension and form better integrated judgment. |
| [`map-shape`](map-shape/) | Turn an initial product understanding into a coherent Problem / Solution / Scopes pitch through adaptive interviewing and sketch or prototype feedback. |
| [`map-product-anatomy`](map-product-anatomy/) | Turn a software product surface or flow into a compact, versionable anatomy of Screens, Components, Actions, States, and Flows. |
| [`review-coherence`](review-coherence/) | Find meaningful product drift, contradictions, and model gaps, then recommend focused corrections. |
| [`classify-work`](classify-work/) | Give product work clear coordinates for Type, Impact, Landscape, form, and routing. |

Each Skill contains its entrypoint, a representative example, and lightweight eval prompts and rubric. Some Skills add a focused reference when the method or taxonomy benefits from progressive disclosure.

## Install and Use

Agent Skills clients discover a directory by its `SKILL.md`; installation locations and invocation syntax vary by client.

1. Clone this repository or download a release.
2. Copy or link the desired Skill directory into a location your compatible agent scans for Skills.
3. Ask for the job in ordinary language, or invoke the Skill explicitly if your client supports explicit invocation.

For repository-scoped use, compatible clients commonly scan `.agents/skills/`. Consult the client documentation before choosing a global or project location.

## Propose a Skill

Open an issue or pull request that describes the recurring trigger, single transformation, recognizable output, repeatable method, evaluation criteria, and source provenance. Start with the smallest useful Skill; do not create one Skill per System or Model for symmetry. See [CONTRIBUTING.md](CONTRIBUTING.md) for the acceptance checklist and expected files.
