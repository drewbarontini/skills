# Example: Shaping Saved Views

## Initial Input

> People repeatedly rebuild the same report filters. I think we need saved views, maybe sharing and a default view too. Help me interview this into something I can sketch.

## Interview Excerpt

**Agent:** The apparent problem is returning to a useful report without rebuilding its filters. Personal saved views may solve that; sharing and defaults introduce additional decisions. Walk me through a concrete recent instance of the problem.

**User:** An analyst recreates the same weekly report filters each Monday. We have seen this in support conversations. They want to return to their own setup; nobody has shown us a sharing need yet.

**Agent:** That supports a personal save-and-return flow first. What effort is this worth, and what would you deliberately leave out to keep it small?

**User:** One short prototype pass. Name, save, and reopen are enough. Leave out sharing, folders, and defaults. Renaming or deleting can follow.

**Agent:** We can now sketch that core flow. The important unresolved behavior is what happens when a saved filter references a field that has changed. I would make that visible in the sketch rather than assume loading always succeeds.

## Resulting Pitch

The reported support evidence below comes from the illustrative user input; it is not independently verified.

```markdown
# Pitch: Personal Saved Views

## Problem

Analysts rebuild the same report filters to return to a recurring report. The supplied support examples describe one analyst recreating a weekly configuration each Monday. The desired outcome is returning to that configuration without rebuilding it.

Appetite: one short prototype pass. Evidence supports personal reuse; a need for sharing remains unproven.

## Solution

Let a user name and save the current report filters, then find and apply that view when returning to the report. Reuse the existing report and filter concepts. Make the active view visible.

Keep the first pass personal. Exclude sharing, folders, descriptions, and default views. Defer renaming and deletion until the core flow has been tried.

Applying a view whose fields have changed remains unresolved. Sketch that case and compare warning, partial application, and blocked application before choosing behavior.

## Scopes

### Save and return to a personal view
- Outcome: an analyst can save a configuration and return to it later.
- Boundary: name, save, find, apply, and see the active view; no sharing or defaults.
- Connections: saving and applying deliver value together and depend on the existing report/filter model.
- Resolve next: sketch where saving and finding belong in the report, how the active view is represented, and what happens when a saved filter is invalid.

### Manage personal views — deferred
- Outcome: remove or rename a view that is no longer useful.
- Boundary: individual rename and delete; no bulk management or restoration.
- Connections: depends on saved views existing; not required to test the core save-and-return value.
- Resolve next: observe the prototype before deciding whether management belongs in the next pass.

Sketch the save-and-return journey first, including invalid filters. Enough is understood to sketch; readiness to prototype depends on bounding the invalid-filter behavior. The prototype can test interaction coherence but cannot establish demand for sharing.
```

## Continuing with a Sketch

If a returned sketch automatically applies a saved view but still labels it active after the user edits its filters, trace the meaning of “active.” Ask whether the edited configuration remains the saved view or becomes an unsaved variation. Resolve that conceptual mismatch and update Solution and the first scope in the same pitch.
