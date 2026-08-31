# 03 · Backlog Refinement

Sprint Planning runs long, stories get pulled in half-understood, and
developers discover missing acceptance criteria mid-sprint — almost every
one of these traces back to refinement not happening, or happening too
shallow. This module treats refinement as its own discipline.

## What refinement actually produces

Refinement (formerly "grooming") is the ongoing activity of taking backlog
items from "idea" to "ready to pull into a sprint." It is not a single
meeting — it's a habit, ideally consuming no more than 10% of team capacity
per sprint, spread across short working sessions.

| Refinement activity | Output | Who drives it |
|---|---|---|
| Splitting large items | Stories small enough to fit in one sprint | PO + team together |
| Adding acceptance criteria | Testable "done" conditions per story | PO, validated by team |
| Estimating | Story points or sizing for prioritization | Whole team |
| Ordering | Backlog sequence reflecting value and dependency | Product Owner |
| Removing stale items | A backlog that reflects current reality | Product Owner |

## The Definition of Ready as refinement's exit criteria

A story is "ready" for Sprint Planning when the team can forecast it with
confidence. A practical checklist:

| Criterion | Why it matters |
|---|---|
| Independent | Doesn't silently depend on another unstarted story |
| Negotiable | Not a rigid spec — room to discuss the "how" |
| Valuable | Ties to a real user or business outcome |
| Estimable | Team has enough shared understanding to size it |
| Small | Fits comfortably inside one sprint |
| Testable | Has explicit acceptance criteria |

(This is the INVEST model, applied specifically as a refinement gate — see
Module 05 for the full Definition of Ready/Done relationship.)

## Splitting techniques

Large stories ("epics") are the most common refinement blocker. Useful
splitting axes:

| Axis | Example |
|---|---|
| Workflow steps | "Checkout" → browse cart, apply coupon, pay, confirm |
| Business rules / variations | "Discounts" → percentage-off, first order, bulk |
| Data boundaries | "Import users" → CSV import, then API import |
| CRUD operations | "Manage products" → create, then edit, then archive |
| Happy path vs. edge cases | Ship the common case first; edge cases as follow-up stories |

## A worked example

A team's backlog has a single item, "Improve search," sized at "too big to
estimate," sitting untouched for three sprints. In a 30-minute refinement
session:

1. The PO explains the underlying goal: users abandon search when results
   feel irrelevant.
2. The team splits along workflow steps: (a) add relevance ranking by
   purchase history, (b) add typo tolerance, (c) add filter-by-category,
   (d) add "no results" suggestions.
3. Each split story gets acceptance criteria — e.g., (b) "a search for
   'shose' returns shoe results" — and gets estimated at 3–5 points instead
   of "unknown."
4. The PO reorders: (a) and (b) go first since they address the actual
   abandonment cause found in analytics; (c) and (d) move to a later sprint.

The backlog goes from one unmovable epic to four independently shippable,
estimated, ordered stories in one session.

## Exercise

Take an epic-sized backlog item (real or invented, e.g. "add
notifications"). (1) Pick a splitting axis from the table and split it into
3–5 stories. (2) Write one acceptance criterion per story. (3) Run each
split story through the six-point Definition of Ready checklist and flag
any that still fail a criterion. (4) State how you'd resolve the failing
criterion before the story enters a sprint.
