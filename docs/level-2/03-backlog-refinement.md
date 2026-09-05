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

## How It Actually Works

Refinement's real function is moving *uncertainty-resolution* work out of
the expensive, time-pressured Sprint Planning meeting and into a cheap,
unpressured setting — the "10% of capacity" figure is the price of buying
back much larger costs later.

**Why an un-refined story blows up Sprint Planning specifically.** When a
story arrives at Planning without acceptance criteria or a split, the room
has to do that analysis live, with everyone present and the sprint's start
time on the line — which is the single most expensive setting in the whole
cadence to be doing discovery work in (multiply the analysis time by every
person in the room, who's now idle while two people hash out scope). This is
mechanically identical to the timeboxing problem in Module 01: a 6-hour
Planning session isn't a facilitation failure, it's unrefined backlog items
consuming the meeting's time budget doing work that a 30-minute refinement
session earlier in the sprint could have done with just the PO and one or
two developers.

**Why splitting along the *right* axis is what actually produces
independence, not the act of splitting itself.** Splitting "Improve search"
by workflow step (relevance ranking, typo tolerance, filtering) works
because each resulting piece touches a different part of the underlying
system and can be built, tested, and shipped without the others existing —
the split follows a real seam in the software. A team that instead splits
"Improve search" into "backend work" and "frontend work" hasn't achieved
independence at all — the frontend piece is unusable without the backend
piece finishing first, so "two stories" is really one story with a
mid-point checkpoint, and Sprint Planning will discover the hidden coupling
when the frontend story can't actually be pulled on its own.

**Why the Definition of Ready has to be an exit gate, not a wish list.** A
checklist that's advisory rather than enforced degrades under sprint-start
time pressure — when Planning is running long and item 6 "looks close
enough," the temptation is to pull it in anyway and hope the gaps surface
cheaply. They don't: an ambiguous acceptance criterion discovered on day 1
costs a clarifying conversation; the same gap discovered on day 8, after
code has been written against the wrong interpretation, costs a rewrite.
Treating Ready as a hard gate (not "ready enough") is what keeps that
discovery cost on the cheap side of the sprint boundary instead of the
expensive side.

## Exercise

Take an epic-sized backlog item (real or invented, e.g. "add
notifications"). (1) Pick a splitting axis from the table and split it into
3–5 stories. (2) Write one acceptance criterion per story. (3) Run each
split story through the six-point Definition of Ready checklist and flag
any that still fail a criterion. (4) State how you'd resolve the failing
criterion before the story enters a sprint.
