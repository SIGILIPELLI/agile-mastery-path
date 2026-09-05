# 07 · Release Planning

Sprints answer "what are we doing next"; release planning answers "when
will stakeholders actually get something, and what will it contain." This
module covers building a release plan that stays honest as reality departs
from the original guess.

## Release planning inputs

| Input | Source | Role in the plan |
|---|---|---|
| Prioritized backlog | Product Owner | Defines *what*, in order of value |
| Velocity range | Module 06 | Defines *how much* per sprint, realistically |
| Fixed constraints | Business (date, budget, compliance deadline) | Defines the boundary the plan must fit |
| Dependencies | Architecture, other teams | Defines sequencing constraints |
| Risk register | Team + stakeholders | Defines what could blow up the plan |

## Two planning shapes

| Shape | Fixed | Variable | Best when |
|---|---|---|---|
| Date-driven | Release date | Scope (what fits by that date) | Marketing launch, compliance deadline, trade show |
| Scope-driven | Feature set (MVP) | Date (ships when the scope is done) | New product where date has no external driver |

Most real releases are a hybrid: a target date the business would like, and
a scope the business needs — release planning's job is to show, honestly,
whether both can hold, and if not, which one has to give.

## Building the plan

1. Order the backlog by value and dependency.
2. Slice it into a "must-have" (true MVP) and "nice-to-have" tier.
3. Using the velocity range, forecast how many sprints the must-have tier
   takes (min–max, as in Module 06).
4. Compare the forecast to the fixed constraint. If the range clears the
   date comfortably, add nice-to-have items. If not, cut scope, not
   quality — never compress the Definition of Done to hit a date.
5. Re-forecast every sprint using updated velocity and remaining backlog —
   a release plan is a living forecast, not a one-time Gantt chart.

## A worked example

A team needs to ship a compliance feature by a hard regulatory date 10
weeks out (5 two-week sprints). The must-have backlog is 95 points; average
velocity is 19 (range 15–24).

- Forecast: 95 ÷ 19 ≈ 5 sprints — exactly matches the fixed date, with the
  worst-case (15/sprint) reading closer to 7 sprints.
- The team flags this at the release-planning session: the plan is *tight*,
  not safe. Two options are proposed: cut two nice-to-have items already
  scoped into the "must-have" pile by mistake (found on re-review), or add
  a contingency sprint by moving the internal soft-launch date.
- The business chooses to trim scope: two lower-value compliance edge cases
  move to a fast-follow release after the deadline, which the legal team
  confirms is acceptable.
- Each sprint, the team re-forecasts; by sprint 3, actual velocity of 21–23
  confirms the trimmed scope will land on time with margin.

The plan didn't just publish a date — it exposed the actual risk two months
before it would have surfaced as a missed deadline.

## How It Actually Works

A release plan built on a velocity *range* rather than a single average
number is doing real risk-quantification work — it's converting "will we
make the date" from a guess into a probability statement the business can
actually act on.

**Why the worst-case number, not the average, is what determines whether a
date is "safe" or "tight."** The average (95÷19≈5 sprints) matching the date
exactly means there is roughly a coin-flip chance of landing later than plan
— by definition, half of a team's historical sprints fall below their own
average. The worst-case forecast (95÷15≈7 sprints) is what actually answers
"what happens if this release behaves like our worst recent sprints twice in
a row," which is not a rare or unfair scenario — it's within the team's own
observed range. Calling the plan "tight" rather than "on track" is the
correct read specifically because the fixed date sits at the *median* of the
outcome distribution, not comfortably inside the safe end of it.

**Why cutting scope, not the Definition of Done, is the only sound lever
under date pressure.** The math above forecasts sprints needed *given a
fixed, unchanging notion of "done."* If a team instead compresses the DoD
under deadline pressure (skips review, cuts test coverage) to hit the same
date with the same point total, they haven't actually reduced the work —
they've just moved it past the deadline, into defect-fixing sprints that
don't show up in this forecast at all (this is Module 05's DoD-erosion
mechanism, now happening under external date pressure instead of internal
velocity pressure). Trimming the scope itself (removing the two edge cases)
is the only move that genuinely reduces the points that must clear the
line, which is why the worked example's business explicitly chooses that
lever over the alternative.

**Why re-forecasting every sprint, not once, is what makes the plan
trustworthy.** A forecast made once at kickoff is a single sample of a
noisy process projected far into the future — as sprints 1 and 2 complete,
the team gains *actual, current-project* velocity data, which is a strictly
better predictor of sprints 3-5 than a 6-sprint historical average from a
different piece of work. Re-forecasting isn't admitting the original plan
was wrong; it's the mechanism by which the plan gets *more* accurate as
uncertainty resolves — which is exactly why the sprint-3 check in the
worked example (actual velocity 21-23) is able to upgrade the plan's status
from "tight" to "on track with margin" using real information the original
forecast couldn't have had.

## Exercise

Given a fixed release date 12 weeks away (six 2-week sprints), a
must-have backlog of 130 points, and a team velocity history of 18, 20, 17,
22, 19 (range 17–22): (1) compute best- and worst-case sprint forecasts,
(2) state whether the date is safe, tight, or at risk, (3) propose one
concrete scope or date change if it's tight or at risk, and (4) describe
what you'd re-check at the sprint-3 mark to confirm the plan is still on
track.
