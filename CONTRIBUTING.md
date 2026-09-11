# Contributing

Propose capabilities, not documentation categories. A contribution should make a recurring job executable while preserving the language and philosophy of its canonical sources.

## Skill Acceptance Checklist

A Skill is ready to propose when every answer below is yes:

- **Recurring trigger** — Can an agent reliably recognize when the Skill applies?
- **Singular primary job** — Does it perform one central transformation rather than represent an entire System, Model, role, or broad capability?
- **Distinctive, repeatable method** — Does the source material provide a method or judgment that improves on generic prompting?
- **Recognizable output** — Can a user tell what artifact or decision the Skill will produce?
- **Evaluable quality** — Can reviewers observe whether the method and judgment were applied well without matching exact wording?
- **Executable value** — Is it more than documentation, a glossary, generic advice, or a prompt that simply asks the agent to “think deeply”?
- **Meaningful provenance** — Does it identify the relevant existing Systems, Models, Patterns, or practices without inventing conceptual layers?
- **Appropriate boundary** — Does it say when not to invoke or overreach where adjacent work could be confused?
- **Focused scope** — Is it small enough for an agent to activate and execute reliably?

If a proposal fails the checklist, it may belong as a Pattern, Model, System, reference, example, or improvement to an existing Skill instead.

## Expected Structure

```text
skill-name/
  SKILL.md
  examples/
  evals/
  references/   # only when deeper task-specific context is useful
```

`SKILL.md` must follow the open Agent Skills format, including a folder-matching lowercase hyphenated `name` and a description that says both when to invoke the Skill and what job it performs.

Include metadata where appropriate:

```yaml
metadata:
  author: drewbarontini
  version: "0.1.0"
  systems: "claritorium, equilio"
  models: "value-creation"
```

Keep metadata values as strings for Agent Skills specification compatibility. Do not force one-to-one provenance.

## Evals

Every Skill must include lightweight semantic evals with:

- obvious positive cases;
- ambiguous cases;
- cases where the Skill should avoid overreaching;
- at least one concrete poor output or failure mode; and
- a rubric based on observable characteristics of sound method and judgment.

Do not grade exact headings or phrases when different wording could perform the job equally well.

## Writing Guidance

- Preserve established terminology and capitalization.
- Link focused references from `SKILL.md` at the moment they become useful.
- Do not duplicate large sections of Claritorium or Equilio documentation.
- Do not add placeholder directories, ornamental formulas, or new taxonomies to make a Skill appear complete.
- Make uncertainty and source gaps visible rather than filling them with invented concepts.

Before submitting, validate each Skill's frontmatter and directory name, inspect every reference link, and run representative eval prompts against the actual Skill instructions.
