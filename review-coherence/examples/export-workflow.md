# Export Workflow Coherence Review

## Input Context

A new report export opens a full-page “Export Job” editor. Elsewhere, exports use a menu, say “Download,” and finish inline. The new flow queues large files, which is a real behavioral difference, but small files also enter the editor.

## Coherence Assessment

The queued workflow needs distinct feedback, but the artifact creates a second export concept for every case. This review compares the new flow with the established product behavior; user evidence was not supplied.

## Findings

### One action teaches two unrelated concepts

- Evidence: comparable report actions are labeled “Download,” while the new action is “Create Export Job.”
- Coherence gap: terminology and concept.
- Why it matters: users must decide whether Download and Export Job are different outcomes before they can act.
- Smallest meaningful correction: retain the established Export/Download language and introduce queue status only after a file actually requires asynchronous processing.
- Confidence: high.

### Small exports inherit unnecessary workflow

- Evidence: every export opens an editor even when no options or waiting are required.
- Coherence gap: flow and whole-product drift.
- Why it matters: a local architecture detail becomes user-facing complexity and breaks a familiar direct action.
- Smallest meaningful correction: keep direct export for ordinary cases; route only large or configurable exports into the queued state.
- Confidence: high.

### Progress feedback lacks continuity

- Evidence: the editor closes into a generic jobs page with no return path to the report.
- Coherence gap: flow.
- Why it matters: users lose the context that explains which report produced the file.
- Smallest meaningful correction: preserve report name and a return link in the queued state.
- Confidence: medium.

## Cross-Cutting Pattern

The implementation exposes queue mechanics as a new product model instead of integrating the necessary difference into the existing export concept.

## Preserve

- Background processing and visible progress for genuinely large files.

## Open Questions

- Which export sizes or options actually require asynchronous handling?
- Do users understand “Download” and “Export” as the same action elsewhere?
