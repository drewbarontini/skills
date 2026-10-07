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
# Problem

For recurring weekly reports, an analyst rebuilds the same filter configuration each Monday, repeating setup before they can use the report.

# Solution

Let users name and save their current report filters, then find and apply a saved view when returning to the existing report. Make the active view visible.

## Constraints

- One short prototype pass; personal views only, with sharing, folders, descriptions, and defaults excluded.

## Tradeoffs

- Personal-only reuse leaves any cross-user reuse manual in exchange for avoiding sharing and permission complexity in the first release.

## Open Questions

- **View Recall:** Where should saving and finding views live, and how should the active view appear?
- **View Recall:** What happens when a saved filter references a changed field? Compare warning, partial application, and blocked application in the sketch before choosing behavior.

# Scopes

Release View Recall first. View Control remains deferred until use reveals management friction.

## View Recall

*Save and return to a view.*

Analysts can save a filter configuration and reopen it later, avoiding repeated setup for recurring reports. Work through saving from the existing report, selecting a saved view on return, and recognizing the active view in the sketches.

### Boundaries

- **Includes:** Naming, saving, finding, applying, and identifying the active view.
- **Excludes:** Renaming and removing saved views.

### Delivery

- Configuration persistence may deploy behind a flag first. Enable the complete save-and-return flow before counting this scope as delivered.

## View Control

*Rename or remove saved views.*

Analysts can rename a view or remove one they no longer need, keeping their saved configurations understandable and relevant. Work through finding a saved view and choosing rename or remove without leaving the management path ambiguous.

### Boundaries

- **Includes:** Individual rename and delete.
- **Excludes:** Bulk management and restoration.

### Constraints

- Requires View Recall to be released; deferred until its use reveals a management need.
```

Enough is understood to sketch View Recall, including invalid filters. Readiness to prototype depends on bounding that behavior; the prototype does not establish demand for sharing.

## Continuing with a Sketch

If a returned sketch automatically applies a saved view but still labels it active after the user edits its filters, trace the meaning of “active.” Ask whether the edited configuration remains the saved view or becomes an unsaved variation. Resolve that conceptual mismatch and update Solution and View Recall in the same pitch.
