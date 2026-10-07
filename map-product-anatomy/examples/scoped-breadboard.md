# Example: Pitch Scopes to a Breadboard

## Supplied Context

A proposed pitch defines **Project Entry**: open an existing project and inspect its tasks, and **Task Creation**: add a task to that project. Task Creation follows the Project Entry release. The user requests an Anatomica map followed by a breadboard.

Projects contains ProjectList and ProjectRow. Opening a row leads to ProjectDetail, which contains TaskList and AddTaskButton. Add opens NewTaskModal on that screen. The modal contains TaskNameField and SubmitButton. Successful submission closes the modal and the task list shows the new task. Failed submission is unresolved.

## Anatomica

```text
# Scope: Project Entry and Task Creation

[Projects]
  ::ProjectList
    ::ProjectRow
      .open() => [ProjectDetail]

[ProjectDetail]
  ::TaskList
  ::AddTaskButton
    .add() => ::NewTaskModal@open
  ::NewTaskModal
    @open
      ::TaskNameField
      ::SubmitButton
        // On successful submission: close the modal and add the task to TaskList.
        .submit() => ::NewTaskModal@closed
    @closed
```

## Scope Associations

- **Project Entry:** Projects, ProjectList, ProjectRow, and the shared ProjectDetail with TaskList.
- **Task Creation:** The same ProjectDetail, AddTaskButton, NewTaskModal, and the updated TaskList.

## Unknowns

- What failed submission does to the modal, its contents, and the SubmitButton.

## Breadboard Guide

This is a medium-neutral drawing guide, not a rendered board.

1. Underline Projects and ProjectDetail as place headings, listing their relevant components and affordances beneath each. Labeled containers are also valid. Keep ProjectDetail shared across scopes, or identify repeated scope-row views as the same Screen.
2. Show NewTaskModal as a component of ProjectDetail, with TaskNameField and SubmitButton beneath or inside it. It may sit beside the screen to make connections legible, with its ownership labeled; an underlined heading does not make it a Screen.
3. Draw an `.open()` arrow from ProjectRow to ProjectDetail. Draw an `.add()` arrow from AddTaskButton to NewTaskModal's open state. Draw a successful `.submit()` arrow to its closed state and note the supported TaskList update.
4. Place “Failed submission?” beside SubmitButton. Keep the unresolved branch visible without creating an Error or Success screen.
5. Label the scope associations, using rows or panels if helpful. Use muted notes for displayed information and consequences, such as “TaskList shows the new task.” If a separate ProjectDetail (task added) view clarifies this update, mark it as a state view of the same Screen. Use spacing to clarify connections rather than decide the final interface layout.

With a requested and available drawing tool, render this structure and inspect the resulting labels, ownership, arrows, and Unknown annotation. If the user chooses paper, the guide is sufficient.

## Revision from a Returned Sketch

If the sketch presents NewTaskModal as a new Screen, correct its label and ownership; this is a representation error, not a product decision. If the user instead chooses to replace the modal with a dedicated Task Creation screen, update the anatomy and breadboard, then revise Solution and Task Creation's boundaries in the same pitch. The existing scope name can remain if its user value is unchanged. Neither choice resolves failed submission without supporting context.
