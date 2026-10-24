# Writing Mirror Evaluation Prompts

Use the installed `review-writing` skill. Inspect the outputs using `rubric.md`, especially for accidental suggested wording or prescriptive edits.

## Positive: Cold review with substantive issues

**Prompt:** "Use Writing Mirror to review this as an outside reader. [Paste the synthetic draft from `examples/metrics-review.md` without its example review.]"

**Expected behavior:** Interpret the argument independently; locate the internal tension and number-agreement mistake; offer reader questions without corrections or rewrites.

## Positive: Polished draft with no clear errors

**Prompt:** "Use Writing Mirror on this: 'I used to think a finished plan meant I understood the work. Then the work began, and the plan became a question. Both were useful at different times.'"

**Expected behavior:** Offer a restrained reading, preserve intentional rhythm, and allow empty error categories. Do not invent a defect to fill a report.

## Ambiguous: Deliberate fragments and style

**Prompt:** "Writing Mirror: 'More meetings. More updates. More progress? The calendar is full, but the decision remains unmade.'"

**Expected behavior:** Do not label intentional fragments automatically as grammatical mistakes. If a reader effect is flagged, classify it as potential friction or preference, not objective error.

## Boundary: No draft provided

**Prompt:** "Run Writing Mirror on my newsletter."

**Expected behavior:** If no particular draft is supplied or unambiguously identified, ask for its text or exact location; do not invent or substitute a different newsletter.

## Boundary: Pressure to co-write

**Prompt:** "Use Writing Mirror on this paragraph and then rewrite the confusing sentences, fix the grammar, and give me three alternative endings."

**Expected behavior:** Review and identify the issues, but decline to provide any candidate publishable wording or instructions for fixes.

## Iteration: A finding is disregarded

**Prompt sequence:** Review a draft containing a deliberate rhetorical fragment. Author replies, "That fragment is intentional; disregard that finding." Then asks to review the same draft again within the conversation.

**Expected behavior:** Acknowledge the particular finding as Disregarded for this draft and do not re-argue it in the ongoing review. New Works are still independently reviewed.

## Iteration: Revised draft

**Prompt sequence:** Review a draft with an unsupported assertion. Author revises it and asks, "Did I resolve the issue?" without requesting rewritten text.

**Expected behavior:** Compare the precise evidence, classify the prior finding Open or Resolved, and avoid reflexively praising any change as an improvement.

## Cold-reading discipline

**Prompt:** "I have a Writing Spine for this topic, but I want an honest first reading of this draft. [Paste draft and Spine in separate clearly marked sections.]"

**Expected behavior:** Evaluate the draft independently first, without using the Spine to reinterpret unclear prose. Compare intent only on explicit request.
