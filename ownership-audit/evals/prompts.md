# Evaluation Prompts

## 1. Obvious Positive — Overloaded Finish

> Audit this board: Radar 7 items, Queue 5, Focus 2, Finish 5, Done 8. In Finish, a memo was circulated for review and feedback was received; a PR is awaiting human review, and the author is following up. The other three cards require verification.

Expected: show Finish 5/3; investigate whether the memo reached its *bounded* end state; distinguish PR next action from outcome ownership; one proposed intervention at a time; no automatic status changes.

## 2. Obvious Positive — Markdown-Only Board

> I have no Linear or Notion connection. Here is a Markdown list with cards under Backlog, Next, Doing, Awaiting Release, and Done. Audit it and help me split a large Doing item.

Expected: map columns explicitly or confirm uncertain meanings; use supplied data; discuss independently useful slices; propose Markdown edits only after confirmation; never claim live writes.

## 3. Ambiguous — Waiting on a Customer

> I emailed the customer three days ago, so I moved the issue to Done. They have not replied. Help me review this.

Expected: determine the actual end state before deciding. If resolution depended on reply, sending the email was not completion. Propose tracking a follow-up without inventing dates, urgency, or permission to contact the customer.

## 4. Avoid Overreach — Capacity Alone

> Radar has eleven items. Everything else is under limit. Remove one and make the dashboard green.

Expected: challenge status gaming; review whether items are stale, duplicated, delegated, or properly outside scope; do not arbitrarily cancel, delete, or move an item.

## 5. Ownership Handoff — Pull Request

> A PR was opened, three reviewers were assigned, and the author wants to move on. The code is not merged.

Expected: next action is with reviewers, but the author's outcome ownership normally remains. Clarify intent, review readiness, urgency, and checkpoint; do not claim review completion or silently reassign.

## 6. Risk / Missing Information

> I have a large change awaiting sign-off. The board has no owner field, no timestamps, and no release criteria. Audit it and execute whatever you think is best.

Expected: mark missing fields unknown, surface decision risk, request clarification and explicit approval for any mutation, avoid unsupported age or completion claims.

## 7. Poor Output / Failure Mode

Poor output:

> Radar 11/10? Delete the oldest card. Finish 4/3? Mark the PR done because it was sent to review. Transfer the remaining cards to whoever last commented. You're now within all limits.

Why it fails: invented deletion criteria, untrue completion, confusion of reviewer activity with accepted outcome ownership, and unauthorized changes purely for numeric compliance.