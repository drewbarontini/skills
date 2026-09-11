# Evaluation Prompts

## 1. Obvious Positive — Similar Things Behave Differently

> Review a product where deleting a dashboard is immediate, deleting a report asks for confirmation, and deleting a folder moves it to Trash. All three use the same trash icon and “Delete” label.

Expected characteristics: identifies consequence/reversibility mismatch, explains expectation risk, and recommends the smallest coherent rule rather than universal confirmation by reflex.

## 2. Obvious Positive — Terminology Drift

> The product calls groups “Workspaces” in navigation, “Organizations” in billing, and “Teams” in invitations. Review coherence.

Expected characteristics: traces whether these are one or multiple concepts, avoids assuming a rename alone solves the model, and asks for domain evidence.

## 3. Ambiguous — No Product Context

> Review this isolated settings mockup for coherence.

Expected characteristics: assesses internal rules, labels comparison claims as limited, and requests relevant neighboring patterns rather than inventing them.

## 4. Avoid Aesthetic Default

> I dislike the rounded cards. Perform a coherence review.

Expected characteristics: does not elevate preference into a finding unless the cards create a discernible inconsistency, hierarchy problem, or model gap.

## 5. Model Mismatch

> Users ask for a Save button, but the editor autosaves correctly. Review the experience.

Expected characteristics: treats feedback as evidence of an expectation gap, checks status/feedback and conventions, and does not automatically add the button.

## 6. Poor Output / Failure Mode

Poor output:

> The screen feels dated. Use more whitespace, brighter colors, rounded corners, and animations to make it coherent.

Why it fails: it supplies subjective aesthetic prescriptions without evidence, a comparative rule, an interpreter model, or a connection to whole-product coherence.
