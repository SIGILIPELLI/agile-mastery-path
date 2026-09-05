# 09 · A Simple Sprint-Planning Exercise

This module is a bridge between the concepts covered so far (Scrum's
events, user stories, story points) and the Level 1 capstone, which asks you
to build a full mock sprint plan. Here, we walk through the mechanics of a
single Sprint Planning session end-to-end, using a small, complete example,
so the capstone is an extension of something you've already practiced, not
a cold start.

## What Sprint Planning actually has to produce

Recall from Module 4: Sprint Planning produces two committed things — a
**Sprint Goal** (the single objective) and a **Sprint Backlog** (the specific
items pulled in to achieve it, sized to fit the team's known capacity).

| Input to the session | Output of the session |
|---|---|
| Ordered Product Backlog | A Sprint Goal, in one sentence |
| Team's known capacity (people, days available, focus factor) | A Sprint Backlog: the specific stories pulled in |
| Historical velocity (if any sprints have run before) | A sanity check that total points pulled ≈ historical velocity |

## Step 1: Establish capacity

A 4-person team runs a 2-week (10 working day) sprint. One developer has 2
days of planned leave.

| Person | Days available | Focus factor (meetings/interruptions) | Effective capacity |
|---|---|---|---|
| Dev A | 10 | 0.8 | 8 days |
| Dev B | 8 | 0.8 | 6.4 days |
| Dev C | 10 | 0.8 | 8 days |
| QA | 10 | 0.7 (more context-switching across stories) | 7 days |
| **Total** | | | **29.4 effective person-days** |

## Step 2: Check historical velocity

The team's last three sprints delivered 21, 25, and 23 story points.
Average velocity ≈ **23 points**. Because capacity this sprint (29.4
person-days) is roughly in line with the last three sprints' typical
capacity, the team plans to pull in **about 23 points** — not more, just
because the backlog has more available.

## Step 3: Pull stories from the top of the backlog

| # | Story | Points | Running total |
|---|---|---|---|
| 1 | As a user, I want to reset my password via email, so I can regain access without support help. | 5 | 5 |
| 2 | As a returning customer, I want my shipping address pre-filled at checkout, so I don't re-type it. | 3 | 8 |
| 3 | As a user, I want an inline error when my card number is invalid, so I don't submit a doomed order. | 5 | 13 |
| 4 | As an admin, I want to export the last 30 days of orders as CSV, so I can reconcile with accounting. | 8 | 21 |
| 5 | As a user, I want a "remember this device" checkbox at login, so I skip 2FA on trusted devices. | 3 | 24 |

At item 5, the running total (24) slightly exceeds the target of 23. The
team discusses: item 5 is independent and lower priority than the rest, so
they leave it out and stop at item 4 (21 points) — deliberately landing
*under* historical velocity rather than over it, since over-committing is
the more common and more damaging failure mode.

## Step 4: Write the Sprint Goal

A good Sprint Goal is a single sentence that gives the pulled stories a
shared purpose — not just "do these four tickets." Here:

> **Sprint Goal**: "Reduce checkout friction and failed logins for returning
> customers."

Notice stories 1, 2, and 3 clearly serve this goal; story 4 (CSV export for
accounting) doesn't obviously fit it. This is a real, common tension — the
team decides to keep item 4 in this sprint anyway (it's time-sensitive for
month-end accounting) but explicitly flags in Planning that it's an
exception to the Sprint Goal, not a hidden scope-creep item. A Sprint Goal
doesn't have to capture 100% of the backlog — it exists so that when
priorities shift mid-sprint, the team has something specific to protect.

## Step 5: Confirm capacity vs. commitment

21 points against a team that has historically delivered 21–25 points on
similar capacity is a defensible commitment — not padded, not over-stretched.
If the pulled total had come out to 35 points against a 23-point average
velocity, that would be a clear over-commitment signal the team should
correct *before* the sprint starts, not discover on day 9.

## How It Actually Works

Sprint Planning's mechanics only work because velocity and the Sprint Goal
are doing two different, complementary jobs — one is a statistical
constraint, the other is a semantic one — and conflating them is where most
sprint failures actually originate.

**Why velocity is a forecast, not a target.** Historical velocity (21, 25,
23) is a sample of a noisy process, not a fixed capability rating. Planning
to *exactly* 23 every sprint would be treating the average as if it were
guaranteed, ignoring that any individual sprint might land at 18 or 28 just
from normal variance (an unplanned production incident, an easier-than-
expected story). This is why Step 3 deliberately stops *under* the average
(21, not 24): the team is pricing in the same variance a bank prices into an
interest rate — planning to the average and hoping for good luck is how
teams end up in a chronic cycle of missed commitments, because roughly half
of all sprints will, by definition, fall below any average.

**Why the capacity math (focus factor) exists at all.** "10 days available"
overstates real coding capacity because it silently assumes 100% of a
person's calendar goes to sprint work — but meetings, code review for other
people's work, and context-switching are real, recurring costs that don't
show up as a line item anywhere else. QA's lower focus factor (0.7 vs 0.8)
isn't an arbitrary number — it reflects that QA typically context-switches
across more stories per day than a developer heads-down on one ticket, and
context-switching has a real, measurable cost (each switch requires
reloading mental context, which is why multitasking reduces net output even
though it feels productive). Skipping this adjustment is the single most
common cause of a sprint that looks correctly planned on paper but runs out
of real hours by day 7.

**Why the Sprint Goal has to tolerate an exception, mechanically.** A goal
that must cover 100% of pulled stories forces the team into a bad choice
whenever a genuinely time-sensitive but off-goal item (the CSV export) needs
to ship this sprint: either distort the goal into something vague enough to
cover everything (which destroys its usefulness as a filter for mid-sprint
scope decisions), or refuse legitimate, time-boxed work to preserve
narrative purity. Explicitly flagging item 4 as a named exception keeps the
goal sharp enough to actually do its job — protecting stories 1-3 if
priorities shift mid-sprint — without pretending the real world only
produces on-theme work.

## Exercise

Using the same format as above, run your own mini Sprint Planning session:
(1) invent a 3–5 person team with realistic capacity and a focus factor, (2)
state a plausible historical average velocity, (3) write 4–6 backlog stories
with story points and pull them in order until you're close to (not over)
the velocity target, (4) write a one-sentence Sprint Goal that most — but
not necessarily all — of your pulled stories serve, and explicitly call out
any story that's an exception to the goal and why it's still included.
Finally, state your final committed point total and compare it explicitly
against your stated historical velocity.
