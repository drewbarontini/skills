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

## 6. Poor Output / Failure Mode

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
