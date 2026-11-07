---
name: ownership-audit
description: Audit an ownership board or work list for capacity, stalled flow, unclear ownership, and missing next moves; then guide approved interventions. Use for weekly work reviews, overloaded Kanban boards, or conversational work reshaping across Linear, Notion, Markdown, and other accessible sources.
metadata:
  author: drewbarontini
  version: "0.1.0"
  systems: "equilio"
  models: "strategic-momentum"
  patterns: "continuous-ownership"
  toolkit: "https://app.notion.com/p/4110a102c722813b9257c859ab57e793"
---

# Ownership Audit

Given an accessible board or supplied work list, reveal the current capacity and flow of work, then help the user choose and apply proportionate interventions. Preserve **Continuous Ownership**: passing someone the next action does not necessarily transfer responsibility for the outcome.

## Board Vocabulary

Use **Ownership Board** for the visual whole, **columns** for stages, **cards** for bounded work, **flow** for movement toward completion, **constraints** for capacity limits, and **interventions** for deliberate changes.

| Generic column | Meaning | Default maximum |
| --- | --- | ---: |
| Radar | Work worth tracking but not yet selected | 10 |
| Queue | Next-up commitments | 5 |
| Focus | Work currently being advanced | 3 |
| Finish | Ready for completion: validation, approval, release, or closure | 3 |
| Done | The bounded end state was reached | None |

These limits are **configurable defaults**, not universal rules. Map the actual source stages to these meanings; for example, Backlog → Radar, In Progress → Focus, In Review → Finish. Ask before assuming an ambiguous mapping. Keep canceled or stale work distinct from Done.

## Method

1. **Inspect.** Identify the source and scope; read its current cards. Capture the column, owner, intended end state, recent activity, blocker or dependency, and next move when available. Keep source links. Mark missing fields as unknown; never fill them with guesses.
2. **Assess.** Show card counts against the user's configured column limits. Look for over-capacity stages, aging cards (only if timestamps support it), unclear ownership, weak end states, waiting without a follow-up plan, and work too broad to finish. Treat counts as visible volume, not equal amounts of effort.
3. **Intervene.** Surface at most three consequential findings and collaboratively examine **one card at a time**. Recommend an intervention only when it improves truthful flow or the actual outcome. Include the rationale, tradeoff, and the next ownership checkpoint.
4. **Apply.** If the user wants changes, propose exact updates and request confirmation before creating, editing, closing, canceling, assigning, or moving cards. Use available native tools or provide an edit for a supplied Markdown list. Preserve existing links, relationships, and relevant history.
5. **Recheck.** Read the changed source when possible. Report what changed, remaining constraints, and who will follow up on dependencies.

## Five Interventions

- **Complete** — Move a card to Done only after its explicit, bounded end state is met. Completion is not the same as sending, handing off, or simply stopping.
- **Defer** — Remove work from a near-term commitment or active focus because it is not currently worth advancing. Keep it visible in the appropriate earlier stage; clarify when to reconsider it.
- **Split** — Close a genuinely finished, independently useful part and open a separate card for the remaining outcome, or split a too-large active card into independently trackable results. Do not mark an unfinished whole as complete.
- **Transfer** — Change the accountable owner only when responsibility for the outcome is genuinely accepted. Assigning a reviewer or awaiting a customer reply is normally a next-action handoff, not ownership transfer.
- **Cancel** — Explicitly close work that is stale, unnecessary, or superseded, with the reason preserved. Cancellation is not completion and must not be used to make column counts look healthy.

Normal forward movement between columns does not require a special intervention.

## Decision Discipline

Before recommending an action, check:

- **Understand:** Outcome, context, and constraints. What is the work actually meant to accomplish?
- **Evaluate:** Impact, reversibility, and confidence. What is the cost of acting **and** waiting? Who must be involved?
- **Act:** Decide, run a bounded test, or involve the appropriate person. Keep the next ownership checkpoint visible.

Escalate when authority, risk, or missing evidence warrants it. Avoid treating every dependency as a reason to wait.

## Response Shape

Use a compact board snapshot and a short discussion:

```markdown
## Capacity
Radar: 4/10 · Queue: 5/5 · Focus: 2/3 · Finish: 4/3 · Done: 7

## What Needs Attention
- [Evidence-backed bottleneck or ownership gap]

## Next Intervention
Card: [title/link]
End state: [known outcome or unknown]
Recommendation: [Complete | Defer | Split | Transfer | Cancel | Advance]
Why: [effect on outcome and flow]
Next checkpoint: [what, who, when if known]
Question: [one consequential decision]
```

When changes are approved, append **Applied** and **Still Open** with verification. For a read-only audit, stop at recommendations.

## Boundaries

- Do not silently mutate an external board or generate work to satisfy arbitrary quotas.
- Do not invent age, priority, accountability, or completion criteria.
- Do not conflate a reviewer/customer dependency with relinquishing ownership.
- Do not hide important work by moving it to an untracked state merely to meet limits.
- Adapt to the source's existing taxonomy; this Skill reviews board-level flow. Use [Classify Work](../classify-work/SKILL.md) for classification of an individual product work item when needed.
- If no connected board is available, ask for a Markdown list or export and continue without pretending to have live state.

## Provenance

Canonical Toolkit method: [Ownership Audit](https://app.notion.com/p/4110a102c722813b9257c859ab57e793). Newsletter development context: [Continuous Ownership](https://app.notion.com/p/4100a102c72281dc8f57e3e483535442).