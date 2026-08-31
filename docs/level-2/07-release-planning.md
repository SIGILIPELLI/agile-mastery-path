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

## Exercise

Given a fixed release date 12 weeks away (six 2-week sprints), a
must-have backlog of 130 points, and a team velocity history of 18, 20, 17,
22, 19 (range 17–22): (1) compute best- and worst-case sprint forecasts,
(2) state whether the date is safe, tight, or at risk, (3) propose one
concrete scope or date change if it's tight or at risk, and (4) describe
what you'd re-check at the sprint-3 mark to confirm the plan is still on
track.
