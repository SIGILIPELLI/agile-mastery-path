# 10 · Capstone — Run a Mock 1-Week Sprint Plan

This capstone combines every Level 1 module into one deliverable: a
complete, realistic 1-week sprint plan for a small product, built the same
way a real team would build one. A 1-week sprint (instead of the more common
2-week length) is used here deliberately, to keep the capstone scoped to
something you can finish in one sitting while still exercising every piece
of the process.

## The scenario

You're the sole Scrum Master/facilitator for a 3-person team building a
**personal budgeting app**. The team has just finished onboarding — this is
their first sprint, so there's no historical velocity yet, only capacity to
plan against.

## Step 1: Write the Product Goal and a starting backlog

Before any sprint exists, there must be a Product Goal (Module 4) — the
single objective the whole backlog serves:

> **Product Goal**: "Let a user track their spending against a monthly
> budget without needing a spreadsheet."

Given that goal, here is a starting, ordered Product Backlog (Module 7 —
INVEST-checked, each with acceptance criteria):

| # | Story | Acceptance criteria (abridged) |
|---|---|---|
| 1 | As a user, I want to log an expense with amount, category, and date, so I can build a spending history. | Amount must be > 0; category is chosen from a fixed list; date defaults to today but is editable. |
| 2 | As a user, I want to set a monthly budget per category, so I know my spending limits. | Budget is a positive number per category; can be edited any time; applies starting the current month. |
| 3 | As a user, I want to see my remaining budget per category, so I know what I can still spend. | Remaining = budget − sum of expenses this month, per category; updates immediately after logging an expense. |
| 4 | As a user, I want a warning when I'm within 10% of a category's budget, so I can adjust spending before overshooting. | Warning shown on the category view; not a blocking action; recalculated on every expense entry. |
| 5 | As a user, I want to see a simple bar chart of spending by category for the current month, so I can spot patterns at a glance. | One bar per category; updates when an expense is added; empty categories still shown at zero. |

## Step 2: Estimate with Planning Poker (Module 8)

The team (2 developers, 1 designer/QA hybrid) estimates using the Fibonacci
scale:

| # | Story | Dev A | Dev B | QA/Design | Final (after discussion) |
|---|---|---|---|---|---|
| 1 | Log an expense | 3 | 2 | 3 | 3 |
| 2 | Set a monthly budget | 3 | 3 | 2 | 3 |
| 3 | See remaining budget | 2 | 5 | 3 | 3 *(Dev B's 5 reflected a misunderstanding — thought this required a new API; resolved to reusing story 1's data)* |
| 4 | Budget-warning threshold | 2 | 2 | 3 | 2 |
| 5 | Spending bar chart | 5 | 8 | 8 | 8 *(no existing charting library on the project — new dependency, higher uncertainty)* |

## Step 3: Establish capacity for a 1-week (5 working day) sprint

| Person | Days available | Focus factor | Effective capacity |
|---|---|---|---|
| Dev A | 5 | 0.8 | 4.0 days |
| Dev B | 4 (1 day on-call) | 0.8 | 3.2 days |
| QA/Design | 5 | 0.7 | 3.5 days |
| **Total** | | | **10.7 effective person-days** |

With no historical velocity yet, the team uses a rough rule of thumb for a
first sprint: plan conservatively, targeting roughly 1.5–2 points per
effective person-day for unfamiliar work — giving a target range of
**16–21 points** for this first sprint.

## Step 4: Pull the Sprint Backlog and set the Sprint Goal

Pulling from the top: stories 1, 2, 3, and 4 total 3 + 3 + 3 + 2 = **11
points**. Story 5 (the bar chart, 8 points) would bring the total to 19 —
within the target range, but it introduces a brand-new charting dependency
in the team's very first sprint together. The team decides, as a
first-sprint risk-management call, to **leave story 5 out** and instead pull
a smaller, lower-priority story from further down the backlog (not shown
above) worth 3 points — landing at **14 points total**, deliberately below
the 16–21 target range, because a new team's first sprint is exactly the
situation where under-committing is the safer error.

> **Sprint Goal**: "A user can log expenses, set category budgets, and see
> whether they're within budget."

## Step 5: Plan the week's Daily Scrums and the Sprint Review

| Day | Planned focus | Daily Scrum check |
|---|---|---|
| Mon | Sprint Planning (this document); Dev A starts story 1 | — |
| Tue | Dev A finishes story 1; Dev B starts story 2 | Any blockers on expense-entry validation? |
| Wed | Dev B finishes story 2; QA starts testing story 1 | Is story 3 blocked on story 1's data model? |
| Thu | Dev A starts story 3; Dev B starts story 4 | Is the 10%-threshold story 4 ready to test yet? |
| Fri (AM) | Finish stories 3–4; QA final pass | Any story at risk of not meeting Definition of Done? |
| Fri (PM) | Sprint Review + Retrospective | — |

**Sprint Review agenda**: demo expense logging, budget setting, and the
remaining-budget view live to a stakeholder (a friend or family member
acting as a test user); ask specifically whether the 10% warning threshold
feels useful or annoying, since that's a subjective product call, not a
technical one — direct input for what the Product Backlog does next.

**Sprint Retrospective agenda**: revisit the Dev B story-3 estimation
mismatch from Step 2 — was there a way to catch that misunderstanding before
Planning Poker, e.g. a quick technical walkthrough of story 1's data model
before estimating story 3? Commit to one concrete change for the next
sprint.

## How It Actually Works

This capstone's real lesson is that a first sprint for a brand-new team has
to be planned differently from sprint four, because the one input every
later technique depends on — historical velocity — doesn't exist yet, and
every step above is a specific workaround for that missing data point.

**Why "1.5-2 points per person-day" is a deliberately conservative proxy,
not a real formula.** With no velocity history, the team has no evidence for
how their specific points-to-hours ratio behaves — so they substitute an
industry rule-of-thumb, and lean it toward the pessimistic end on purpose.
This matters mechanically: an over-commitment in sprint one doesn't just cost
that sprint, it also produces a *corrupted* first velocity data point (a
missed 19-point commitment reads differently than a met 14-point one), and
every subsequent sprint's planning in Module 9 depends on trusting that
number. Landing safely under-target isn't caution for its own sake — it's
protecting the integrity of the data the whole rest of the process runs on.

**Why the story-3 estimation mismatch is exactly the kind of risk Planning
Poker is supposed to catch — and almost didn't.** Dev B's 5 (versus 2 and 3
from the others) came from believing story 3 required a new API, when it
actually just reused story 1's data model — a scope misunderstanding, not a
genuine complexity disagreement. This is precisely why the outlier gets
asked to explain their number instead of being averaged away: averaging (2,
5, 3) to a smoothed ~3.3 would have hidden the misunderstanding entirely,
while surfacing it let the team correct a wrong mental model *before* the
sprint started, for the cost of one conversation, instead of during
implementation, for the cost of Dev B redesigning an API that was never
needed.

**Why leaving the charting story out is a dependency-risk decision, not a
capacity one.** At 19 points, story 5 fits inside the numeric target range —
but a brand-new team's first-ever use of a new charting library is exactly
the kind of unknown-unknown that historical velocity has never priced in
(there's no history to price it against). Substituting a smaller, better-
understood story preserves the point total's meaning: 14 points of familiar-
shaped work is a much more honest first data point than 19 points that
includes an unbounded integration risk, because the whole point of measuring
velocity is to make future capacity predictable, and one wildcard story
undermines exactly that.

## Capstone deliverable — what to produce

Following the exact structure above, but for a product of your own choosing
(not budgeting — pick something different), produce:

1. A one-sentence Product Goal and a 5-item ordered Product Backlog with
   acceptance criteria.
2. A Planning Poker table with at least one deliberate estimation
   disagreement and its resolution.
3. A capacity table for a realistic 3-person team over a 1-week sprint.
4. A pulled Sprint Backlog with a running point total, checked against a
   stated target range, including at least one item you deliberately leave
   out and your reasoning.
5. A one-sentence Sprint Goal.
6. A 5-day plan naming what happens each day and one specific Daily Scrum
   question per day.
7. A Sprint Review agenda naming one specific, non-generic question you'd
   ask a real stakeholder.
8. A Sprint Retrospective agenda that references a specific event from your
   own plan (not a generic "communicate better" item).
