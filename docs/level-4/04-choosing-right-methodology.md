# 04 · Choosing the Right Methodology per Project Type

No single methodology is correct everywhere. A master-level practitioner
matches the approach to the nature of the work instead of applying one
framework by default across every project a portfolio contains.

## The core question: how well is the work understood?

| Work characteristic | Implication for methodology |
|---|---|
| Requirements well understood, low uncertainty, regulatory/fixed deadline | Predictive (waterfall-like) approaches can work fine — the cost of upfront planning is low relative to the risk of change |
| Requirements emerge through use, high uncertainty, fast feedback available | Iterative/agile approaches earn their overhead by cutting the cost of being wrong |
| Continuous flow of similarly-sized work, no discrete "projects" | Kanban fits better than sprint-based Scrum |
| Deep technical unknowns need investigation before any plan is credible | A time-boxed spike or discovery phase precedes methodology selection |

## A decision framework

| Question | If yes → | If no → |
|---|---|---|
| Can the full scope be specified correctly today? | Lean predictive | Lean iterative |
| Will stakeholders see and react to work before completion? | Iterative unlocks real value from that feedback | Predictive loses little by skipping it |
| Is the cost of a late-discovered mistake severe (safety, compliance, irreversible)? | Add upfront verification/gates regardless of overall approach | Ship small increments and learn |
| Is work discrete, project-shaped, with a defined end? | Scrum-style iteration | Kanban-style continuous flow |

## Common mismatches and their symptoms

| Mismatch | Symptom |
|---|---|
| Agile applied to fixed, well-understood regulatory filing work | Ceremonies feel like theater; the "iteration" never actually changes course because there's nothing to learn |
| Waterfall applied to a genuinely exploratory product | Big upfront spec turns out wrong; teams spend more time defending the plan than adapting to what's learned |
| Scrum applied to a support/maintenance team's ticket flow | Artificial sprint boundaries around inherently unpredictable, continuously-arriving work; Kanban would fit better |
| Kanban applied to a team that needs forecasted, stakeholder-facing delivery dates | Continuous flow alone doesn't produce the commitment cadence stakeholders are asking for; needs a cadence overlay |

## A worked example

An organization runs three very different initiatives under one blanket
mandate — "everything is Scrum." Team A builds a new customer-facing
product with heavy uncertainty (good agile fit). Team B maintains a stable
payroll system, fielding an unpredictable stream of small tickets (better
suited to Kanban). Team C is executing a fixed-scope regulatory filing with
a hard external deadline and well-understood requirements (better suited to
a lightweight predictive plan with agile-style daily transparency, not full
Scrum).

Applying this module's framework: Team A keeps Scrum — its uncertainty and
feedback opportunities justify the ceremony overhead. Team B moves to
Kanban with WIP limits and class-of-service lanes, matching its continuous,
unpredictable ticket flow. Team C keeps a fixed, verified plan with clear
milestones, but adopts daily standups and a visible task board for
transparency — borrowing agile's communication practices without forcing
sprint boundaries onto genuinely fixed-scope, well-understood work.

## Exercise

Your portfolio includes: (1) a brand-new mobile app with unclear
requirements and eager users willing to give feedback, (2) an IT helpdesk
team fielding a continuous, unpredictable stream of tickets, and (3) a
one-time data-migration project with a hard compliance deadline and fully
specified requirements. For each, use the decision framework to name the
methodology you'd choose and the specific characteristic (from the first
table) that drove the choice.
