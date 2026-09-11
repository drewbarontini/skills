# Mobile Search Classification

## Input

> On mobile, applying a date filter and then reopening Search clears the selected date. Desktop retains it. We have five related mobile search defects, but no existing parent item. Product Landscape: Discovery → Search → Mobile. Customers mention the problem weekly. Engineering has not accepted it for this week.

## Work Classification

- Title: Preserve date filters when reopening mobile Search
- Type: Fix
- Impact: mobile customers lose their search state and must repeat work; the weekly reports and five related defects suggest recurring, multi-item friction, but usage breadth is unknown.
- Landscape: Discovery → Search → Mobile
- Work Form: Batch candidate with the five related mobile Search Fixes, if they share a coherent surface and can be handled as focused improvements.
- Route: Radar/Backlog

## Rationale

Desktop behavior and the stated expectation make this a Fix rather than an Improvement. The related defects may justify a Batch, but grouping should wait until their relationship is verified. It remains outside Queue because no near-term commitment was provided.

## Missing Context

- Number and importance of affected mobile users.
- Whether all five defects share the same underlying surface or owner.

## Reclassify When

- Move to Queue when the team commits it to the near-term horizon and assigns an owner.
- Use a Batch when the related issues form a focused, executable unit.
- Reclassify as Improvement if clearing the filter is current intended behavior and the request changes that behavior.
