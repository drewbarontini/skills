# Product Anatomy: Report Editing Flow

## Input context

The Reports screen contains a report list. The list is empty when no reports exist and ready otherwise. Each report appears as a row; opening a row leads to the Report Detail screen.

Report Detail contains an editor with a Save button. The button begins idle. Saving moves the button into a saving state. The notes do not describe what happens when saving succeeds or fails, or where the user goes next.

## Anatomica

```text
# Scope: Open and save an existing report

[Reports]
  ::ReportList
    @empty
    @ready
    ::ReportRow
      .open() => [ReportDetail]

[ReportDetail]
  ::Editor
    ::SaveButton
      @idle
        .save() => @saving
      @saving
```

## Unknowns

- What state follows `@saving` when the save succeeds or fails.
- Whether saving keeps the user on `[ReportDetail]` or leads elsewhere.
