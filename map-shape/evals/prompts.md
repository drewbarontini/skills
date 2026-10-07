# Evaluation Prompts

## 1. Obvious Positive — Interview a Fuzzy Feature

> Customers want reusable dashboard configurations. Here is everything I know: they rebuild filters weekly, and I imagine saved views, sharing, and defaults. Interview me until we have enough to sketch.

Expected characteristics: reflects provisional understanding, asks a focused consequential question and waits, distinguishes evidence from proposed additions, and contributes narrowing judgment. Develops the pitch as answers arrive rather than inventing a completed solution.

## 2. Obvious Positive — Enough Context to Draft

> Shape a pitch for personal saved views. Support examples show analysts rebuilding the same weekly filters. They should name, save, find, and apply their own views within the existing report. One short prototype pass; no sharing, defaults, or folders. Invalid saved filters need investigation in the prototype. Give me the areas to work through.

Expected characteristics: drafts directly with a one- or two-sentence Problem, one short Solution paragraph, and named Scopes; preserves the five shaping steps without exposing every intermediate list; combines saving and applying into one independently useful scope; retains invalid-filter uncertainty in optional Open Questions and bounds it for investigation. Uses Title Case, two- or three-word scope names, action-oriented shorthand, brief descriptions, and Boundaries. Does not delay a useful pitch with a questionnaire or treat prototype readiness as production readiness.

## 3. Ambiguous — Missing Problem

> Shape an AI assistant for our app.

Expected characteristics: probes the situation and desired user outcome before assuming chat, automation, new screens, or a feature set. Does not fabricate demand or produce a false complete pitch.

## 4. Continue — Sketch Contradicts the Pitch

> Here is our saved-views pitch: personal views only, save and return, no defaults. My sketch opens the report with the last saved view automatically applied. It still shows the view as active after someone edits its filters. What do we need to resolve?

Expected characteristics: resumes the existing pitch, notices the implicit default and ambiguous meaning of active, prioritizes the consequential conceptual question, and updates the pitch after clarification. Does not validate drawn decisions by their presence or restart discovery from scratch.

## 5. Stopping — Ready to Sketch, Not Yet to Prototype

> We know who needs this and why, and have picked personal save-and-return. We have not decided where views live or how changed fields affect loading. Keep interviewing until every edge case is settled.

Expected characteristics: explains which uncertainty is better addressed through sketching, names areas and questions to draw, and distinguishes sketch readiness from prototype readiness. Does not insist on resolving every detail verbally or silently choose invalid-filter behavior.

## 6. Direct Prototype — No Drawing Connection

> We have a coherent core journey and explicit boundaries. The remaining question is whether people can find the saved-view control. Let's test that in a prototype; I don't use tldraw.

Expected characteristics: identifies the prototype as the next useful action, retains the question in the scope, and avoids requiring a sketch, drawing tool, or exhaustive specification. The skill shapes the handoff rather than generating code unasked.

## 7. Detailed Shape Map Requested

> Shape these notes as a detailed map: invite teammate, roles?, email delivery risk, create workspace, accept invite, SSO later, decide account ownership, empty state.

Expected characteristics: provides the detailed Shape Map, preserves mixed item types and dependencies, finds an end-to-end collaboration flow, and retains unanswered ownership and permission questions. The pitch default does not override the requested format.

## 8. Avoid Overreach — Implementation Request

> The saved-views pitch is approved and bounded. Produce database tables, API routes, React components, estimates, and sprint tickets.

Expected characteristics: recognizes detailed implementation planning as downstream and does not force another shaping interview. If this skill is applied, limits its contribution to a requested handoff rather than inventing architecture or estimates.

## 9. Avoid Horizontal Scopes

> Split the work into database, backend, frontend, and QA phases.

Expected characteristics: distinguishes deployable build units from user-facing scopes. Combines pieces that need each other into one independently releasable, useful scope; staged technical work belongs in optional Delivery notes. Dependencies on earlier released scopes are valid, but future work cannot be required for a scope's basic usefulness.

## 10. Production Deployment Without User Value

> Scope one creates storage behind a flag. Scope two adds a save button. Scope three lets users reopen saved filters. Each can deploy separately, so name these as three scopes.

Expected characteristics: combines the pieces into a save-and-return scope because neither hidden storage nor a save-only interface delivers the intended value independently. Preserves deployment staging in Delivery rather than forbidding backend-only releases or treating the flag as a completed user scope.

## 11. Naming and Compact Scope Structure

> Give our saved-views scopes short, brandable names for milestones, plus shorthand and clear boundaries. Rename/delete comes after the existing save-and-return release.

Expected characteristics: gives each scope a memorable, Title Case, two- or three-word name with a plain shorthand and one or two sentences of user value. Uses H2 scope headings and H3 Boundaries; avoids cryptic branding and the old Outcome / Connections / Resolve next checklist. Recognizes rename/delete as independently useful on top of an earlier release.

## 12. Problem Size and Optional Subsections

> We know one analyst recreates report filters each Monday, but do not know how widespread it is. Keep the pitch tight. Personal-only views are a deliberate choice to avoid sharing complexity, not an externally imposed restriction.

Expected characteristics: reflects frequency and recurring setup cost within one or two Problem sentences without inventing reach or numbers. Keeps Solution to a short paragraph; distinguishes limits in Constraints, accepted consequences in Tradeoffs, and unresolved evidence in Open Questions. Omits subsections with no consequential content instead of filling them for symmetry.

## 13. Shareable Pitch and Portable Sketch List

> I want to shop this pitch around, then take each scope onto paper or into my drawing app and work out the experience. I will bring sketches back if they change the direction.

Expected characteristics: produces a pitch understandable without the interview transcript, with scopes that identify usable value, the supported core interactions to sketch, boundaries, and scope-associated Open Questions. Keeps the tight three-section format, requires no drawing connection, and treats the scopes themselves as the working list rather than adding a duplicate sketch plan. Returned sketches can revise the problem, approach, and scopes in the same pitch without being mistaken for validated demand.

## 14. Poor Output / Failure Mode

Poor output:

> Answer these twenty questions before I can help. The final pitch will have Problem, Appetite, Solution, Risks, Scopes, and Technical Plan. Scope 1 is database; scope 2 is API; scope 3 is UI. Each scope is delivered as soon as it deploys, even if users cannot complete the flow. Sharing is required because it appeared in your initial notes. Once every edge case is specified, we can sketch.

Why it fails: burdens the user with a fixed questionnaire, overrides the compact output, creates horizontal scopes, confuses deployment with delivered value, treats suggestions as requirements, hides judgment, and postpones drawing until it can no longer contribute to shaping.
