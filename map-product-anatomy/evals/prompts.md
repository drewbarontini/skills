# Evaluation Prompts

## 1. Obvious Positive — Defined Product Flow

> Map this product anatomy: The Projects screen contains a project list made of project rows. The list is empty when there are no projects and ready otherwise. Opening a project row leads to Project Detail. Project Detail contains a task list and an Add Task button. Selecting Add Task opens a New Task modal. The modal can be open or closed; submitting it returns to Project Detail.

Expected characteristics: valid Anatomica; correct Screen, Component, State, and Action distinctions; explicit transitions; and stable naming for repeated concepts.

## 2. Obvious Positive — Existing Product Notes

> Turn these notes into Product Anatomy: account page / profile info / editing? click Edit opens edit profile modal. modal has name field + Save. Save closes modal, account page shows new name. also says profile card in two places—probably same thing. loading state belongs to save button. cancel closes it. Don't know what failed save does.

Expected characteristics: converts the evidence into compact structure, normalizes repeated concepts such as `ProfileCard`, and preserves the loading state, close flows, and unknown failed-save behavior.

## 3. Ambiguous — Missing Behavior

> Map a Search screen with a query field, results list, and result rows. A note says “results can be selected,” but it does not say what selection does. Empty and loading behavior are also unspecified.

Expected characteristics: maps the known screen and component hierarchy, surfaces missing destinations and states as Unknowns, and does not fabricate flows.

## 4. Avoid Overreach — Implementation Request

> For a team invitation flow, produce the React components, API routes, database schema, service boundaries, and Product Anatomy.

Expected characteristics: keeps Product Anatomy focused on product structure and behavior; does not turn Anatomica into implementation architecture or invent technical decisions.

## 5. Avoid Category Confusion

> Map this: Checkout contains a Payment Form. The form can be valid or invalid. Its Submit button is disabled while the form is invalid. Pressing Submit moves to Order Confirmation. A designer refers to “Disabled” as a page and “Submit” as a control.

Expected characteristics: represents `Checkout` and `OrderConfirmation` as Screens, `PaymentForm` and `SubmitButton` as Components, `@valid`, `@invalid`, and `@disabled` at their narrowest owning levels, and `.submit()` as an Action with an explicit transition.

## 6. Shaped Scopes to Breadboard

> Our pitch has Project Entry (open an existing project and inspect tasks) and Task Creation (add a task to an existing project). Projects contains ProjectList and ProjectRow; opening a row leads to ProjectDetail. ProjectDetail contains TaskList and AddTaskButton. Add opens NewTaskModal, which contains a name field and SubmitButton. Successful submission closes the modal and the list shows the new task; failed submission is unresolved. Map this in Anatomica and breadboard it in tldraw.

Expected characteristics: preserves the scope names and supported intent, shows shared ProjectDetail and its components, keeps NewTaskModal a component with states, and labels arrows with the triggering actions and correct destination types. Renders when the requested connector is available and inspects the result; otherwise accurately reports what was produced. Keeps failed submission unresolved. Does not turn the diagram into a wireframe or introduce new notation.

## 7. Unknown Destination in a Drawing

> Breadboard this anatomy: Search has QueryField and ResultList with ResultRow. Selecting a result is supported, but its destination is unknown. I want to see that gap rather than choose behavior yet.

Expected characteristics: shows the screen, relevant affordances, and a question beside the selection action. Does not invent a Result Detail screen or treat an Unknown annotation as a real Screen. Candidate answers stay marked as alternatives if requested.

## 8. Returned Sketch Changes the Pitch

> Our personal-saved-views pitch excludes defaults and sharing. The scope View Recall maps saving and reopening within Report. The new sketch auto-applies the last view and introduces SharedViewPicker. Reconcile it with the pitch and anatomy.

Expected characteristics: identifies the new default-like behavior and sharing concept as proposed changes, explains their effect on boundaries and user value, and asks for or uses an explicit decision before treating them as settled. Reconciles accepted changes across the same pitch, anatomy, and drawing; does not treat drawing as evidence of demand.

## 9. Text-Only Anatomy

> Map the defined project flow in Anatomica only. I will sketch it on paper later.

Expected characteristics: delivers compact text anatomy without requiring a connector, creating a board, or forcing the breadboard continuation. Preserves enough names, transitions, and Unknowns for later manual sketching.

## 10. Visual Overlay Mistaken for Navigation

> The anatomy has AddTaskButton opening NewTaskModal on ProjectDetail. A returned breadboard puts NewTaskModal in a separate rectangle labeled as a Screen and draws submit navigating to a new Success screen. Fix the representation; we have not chosen a new success destination.

Expected characteristics: preserves modal ownership and component identity despite its visual position, corrects the unsupported Success screen, and retains unsettled submit behavior as an Unknown. Distinguishes a rendering correction from a new product decision.

## 11. Lightweight Places and State Views

> Use underlined place names with affordances listed beneath them, muted explanatory notes, and arrows from the relevant actions. ProjectDetail has TaskList and AddTaskButton. Add opens NewTaskModal on ProjectDetail. Successful submission closes the modal and updates TaskList. Show the scopes in separate rows; a repeated ProjectDetail (task added) view should help explain the update.

Expected characteristics: honors the text-based drawing style without requiring boxes; distinguishes place headings from Anatomica Screens; preserves NewTaskModal as a component and ProjectDetail (task added) as a view of the same Screen. Arrows originate at the relevant affordances, with action labels there or on the arrows. Annotations explain the list update rather than become controls. Scope rows retain shared identity rather than inventing separate screens or navigation. Unknown behavior remains unresolved.

## 12. Poor Output / Failure Mode

Poor output:

```text
[ReportList]
  ::Loading
    .SaveButton()
  ::ReportDetails
    @click
    .save() => [Dashboard]

[report-detail]
  ::SaveControl@done

[Dashboard]
  ::SaveSuccessBanner@visible
    .dismiss()

// The report is also represented here as a second complete branch.
[Reports]
  ::Report
    ::SaveButton@finished
```

Why it fails: it treats a component as a Screen, a state as a Component, and an action as a state; it uses inconsistent names for Report Detail and Save Button; it invents loading, completion, Dashboard, and success-banner behavior; and it hides the actual open-and-save transitions beneath redundant, unsupported structure.

Another poor output: creates separate ProjectDetail concepts for each scope, promotes NewTaskModal to a Screen, adds a Success screen to close an unknown arrow, and leaves the pitch unchanged after introducing sharing. It mistakes drawing convenience for product structure and fragments the intended experience.
