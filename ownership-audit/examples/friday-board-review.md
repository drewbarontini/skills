# Friday Ownership Board Review

## Input

The user provides this Markdown board. The five stages and limits are already agreed.

| Column | Card | Owner | End state / current context |
| --- | --- | --- | --- |
| Radar | Update onboarding copy | Ari | Needs problem framing |
| Radar | Explore mobile export | Ari | No commitment |
| Queue | Billing receipt fix | Sam | Ready to start next week |
| Queue | Support digest | Mei | Summarize recurring issues |
| Focus | Trial conversion analysis | Ari | Draft analysis in progress |
| Focus | Team meeting improvements | Mei | Prototype in use |
| Finish | Strategy memo | Ari | End state: circulate for review; circulated and reviewed |
| Finish | Citation rendering PR | Sam | End state: merged and deployed; human review requested |
| Finish | Customer FAQ | Mei | End state: approved FAQ; approval still pending |
| Finish | Email provider configuration | Lee | End state: working configuration; validation still needed |
| Done | Fix account access error | Sam | Shipped and verified |

The user asks: "What is stuck and what should I do?"

## Expected Audit

**Capacity:** Radar 2/10 · Queue 2/5 · Focus 2/3 · Finish 4/3 · Done 1.

**Observation:** Finish is over its limit. The memo may have met its bounded end state. The PR remains Sam's responsibility despite the reviewer having the next action. There are no timestamps, so the audit cannot claim any card is "three days old" or overdue.

**First intervention to discuss:**

- **Card:** Strategy memo
- **Recommendation:** Complete *if* its intended deliverable was merely to circulate the memo and receive an initial review. Create a new card only if a distinct follow-on decision or revision is needed.
- **Why:** Finishing the actual bounded outcome frees space without pretending a larger strategy project is done.
- **Question:** "Was circulation and initial review the agreed end state, or are substantive revisions still part of this card?"

Then address the citation rendering PR. A reviewer assignment transfers the next action, not automatically Sam's responsibility for completion. Sam can clarify urgency, check review status, and agree a follow-up checkpoint. Do **not** transfer outcome ownership or mark the PR Done.

## Good Behavior

- Makes the capacity issue immediately visible.
- Asks one consequential question at a time.
- Distinguishes the completed memo deliverable from a potentially new work item.
- Preserves the PR author's ownership across a review handoff.
- Requests confirmation before changing the supplied Markdown or a connected board.

## Failure Example

"Finish is over capacity. Cancel the FAQ and mark the PR done because review has been requested."

This makes numbers look better by falsifying outcomes. The FAQ is still awaiting approval, and the PR has not been merged or deployed.