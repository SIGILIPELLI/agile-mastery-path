# 04 · Scrum Roles, Events & Artifacts

Scrum is the single most widely adopted Agile framework, and it works
because it's built from a small, fixed set of parts — three roles (called
"accountabilities" in the current Scrum Guide), five events, and three
artifacts — each with one clear job. Learn these ten pieces precisely and
you can recognize (and diagnose) Scrum anywhere it's implemented, correctly
or not.

## The three roles

| Role | Accountable for | Not accountable for |
|---|---|---|
| Product Owner | Maximizing product value; ordering the Product Backlog; single voice on what "done" is worth building next | *How* the work gets built, or estimating technical effort |
| Scrum Master | The team's effective use of Scrum; removing impediments; coaching the organization | Directing the team's day-to-day technical work or assigning tasks |
| Developers | Building a usable Increment each Sprint; managing their own work within the Sprint | Deciding *what* to build — that's the Product Owner's call |

The most common role failure is a Product Owner who is really a project
manager in disguise — assigning tasks to individual developers and dictating
*how* work happens — which collapses the self-organization principle from
Module 3 and turns Scrum into Waterfall with a two-week clock.

## The five events

| Event | Timebox (2-week sprint) | Purpose |
|---|---|---|
| Sprint | Fixed container | Everything else happens inside it; a new one starts immediately after the last ends |
| Sprint Planning | ≤4 hours | Team selects Product Backlog items and forms a Sprint Goal and Sprint Backlog |
| Daily Scrum | 15 minutes | Developers inspect progress toward the Sprint Goal and re-plan the next 24 hours |
| Sprint Review | ≤2 hours | Inspect the Increment with stakeholders; adapt the Product Backlog based on feedback |
| Sprint Retrospective | ≤1.5 hours | Team inspects itself — process, people, tools — and plans concrete improvements |

Two details trip up most first-time practitioners. First, the **Daily Scrum
is not a status report to the Scrum Master or a manager** — it's the
Developers re-planning their own next 24 hours; if the Scrum Master is
running it like a status meeting, that's a role failure from the table
above. Second, **the Sprint Review is not a demo for its own sake** — its
actual output is an updated Product Backlog, because stakeholder feedback is
supposed to change what happens next.

## The three artifacts, and the commitment behind each

| Artifact | What it is | Its "commitment" (the quality bar it must meet) |
|---|---|---|
| Product Backlog | Ordered list of everything that might be needed in the product | The **Product Goal** — a single objective the whole backlog is working toward |
| Sprint Backlog | The Product Backlog items selected for this Sprint, plus the plan to deliver them | The **Sprint Goal** — the single objective this specific sprint exists to achieve |
| Increment | A concrete, usable step toward the Product Goal | The **Definition of Done** — a shared, standing checklist of what "usable" means |

These three commitments matter more than the artifacts themselves. A
Product Backlog with no Product Goal is just a to-do list with no direction.
A Sprint Backlog with no Sprint Goal is just a batch of unrelated tickets —
which means when priorities shift mid-sprint, there's no shared objective to
protect, and the sprint dissolves into ad-hoc reshuffling.

## A worked example: one sprint end-to-end

A 5-person team building a mobile banking app runs a 2-week sprint:

1. **Sprint Planning (Day 1, morning)**: The Product Owner presents the top
   of the Product Backlog. The team commits to a Sprint Goal — "users can
   view their last 90 days of transactions, filterable by category" — and
   pulls 6 backlog items into the Sprint Backlog to achieve it.
2. **Daily Scrum (Days 2–9)**: Each morning, Developers sync on what's done,
   what's next, and any blockers — e.g., Day 4's standup surfaces that the
   categorization API returns an undocumented null field, which two
   developers pair on fixing that afternoon.
3. **Sprint Review (Day 10, morning)**: The team demos the filterable
   transaction view to the Product Owner and two stakeholders from Customer
   Support. Support flags that customers frequently ask about *pending*
   transactions, which aren't shown — that becomes a new, re-prioritized
   Product Backlog item, not a mid-sprint scope change.
4. **Sprint Retrospective (Day 10, afternoon)**: The team notes the
   undocumented-null-field incident cost half a day and agrees to add "API
   contract review with backend team" as a Sprint Planning checklist item
   going forward.

## Exercise

Design a Sprint Backlog for a 2-week sprint for a team of your choosing
(pick a real or invented product). Write: (1) a specific Sprint Goal in one
sentence, (2) 4–6 Product Backlog items pulled into this sprint that clearly
serve that goal, (3) one Definition of Done with at least five checkable
criteria, and (4) one plausible mid-sprint incident (like the null-field
example) that would come up in a Daily Scrum, plus how the team should
handle it without breaking the Sprint Goal. Then write one Sprint Review
outcome — a piece of stakeholder feedback that changes the Product Backlog
for next sprint, without being smuggled into the current sprint.
