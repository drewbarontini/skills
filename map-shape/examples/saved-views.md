# Shape: Saved Views

## Context

People repeatedly rebuild the same report filters. A saved view should let them return to a useful configuration without turning the first release into a general configuration platform.

## Surface

- [A] Save the current filters with a name.
- [A] List and apply saved views.
- [D] Decide whether one view can be the default.
- [Q] Who can see a saved view?
- [R] Existing filters may become invalid when fields change.
- [U] Whether people need sharing in the first release.
- [A] Persist the filter configuration.

## Structure

### Persistence

- Store a named filter configuration.
- Validate fields when loading.

### Management (depends on Persistence)

- Save and list views.
- Rename or delete a view.

### Application (depends on Persistence and Management)

- Apply a view to the report.
- Show which view is active.

## Slices

### Save and Reapply Personal View

- Value: a user can save current filters and use them again.
- Boundary: In—name, save, list, apply; Out—sharing, descriptions, folders, default views.
- Dependencies: persistence, validation, and the existing filter model.
- Independence test: the same user can complete a useful save-and-return flow without sharing or administration.

### Manage Personal Views

- Value: a user can rename or remove obsolete views.
- Boundary: In—rename and delete; Out—bulk operations and restoration.
- Dependencies: the first slice.
- Independence test: useful after saved views exist, but not required to validate the core value.

## Simplification

- Keep: personal named views and visible active state.
- Reduce: name only; use existing filter validation.
- Defer / remove: sharing, folders, descriptions, default views, and bulk management.

## Sequence

1. Save and Reapply Personal View — the smallest complete value unit, with persistence built inside the slice.
2. Manage Personal Views — follows only if use reveals management friction.

## Remaining Uncertainty

- Whether invalidated filters should be dropped, flagged, or prevent loading.
- Whether repeated requests for sharing justify a separate future slice.
