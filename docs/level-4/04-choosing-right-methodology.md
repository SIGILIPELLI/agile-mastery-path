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

## How It Actually Works

Every mismatch in this module's table reduces to the same underlying
diagnostic: a methodology's overhead only pays for itself when the
*specific mechanism* it provides addresses uncertainty or variability that
actually exists in the work. Applying it where that mechanism has nothing
to act on produces ceremony with no function — costly theater, not a
process error you can tune your way out of.

**Why "ceremonies feel like theater" is the correct diagnostic signal, not
just a complaint.** Sprint Review exists to let stakeholder feedback change
what happens next (Module 04, Level 1) — but Team C's regulatory filing has
requirements fixed by law, so there is nothing a Sprint Review's feedback
loop *can* change; the review happens, produces no course correction, and
everyone present correctly senses that the exercise accomplished nothing.
This isn't a facilitation failure to fix with better retro techniques — it's
the mechanism itself having no uncertainty to resolve in this specific
context, which is why the fix is removing the mechanism (sprint boundaries)
rather than running it better.

**Why Team B's unpredictable ticket flow breaks specifically on the sprint
boundary, not on Scrum's other parts.** A Sprint Backlog commits to a fixed
set of items for a fixed window — but a support team's incoming tickets
arrive at an unpredictable rate with unpredictable urgency (a production
incident doesn't wait for the next Sprint Planning). Forcing that flow into
sprint boundaries means either the sprint commitment gets broken routinely
(destroying its value as a forecast, Module 09, Level 1) or urgent tickets
get artificially delayed until the next planning session (defeating the
point of a support function). Kanban's pull-based, continuous-flow model
(Module 05, Level 1) has no boundary to violate — WIP limits regulate flow
without requiring the arrival rate to be predictable, which is exactly the
property this kind of work needs and Scrum's timeboxed commitment doesn't
provide.

**Why Team C still benefits from daily standups despite not needing
sprints.** A standup's value — surfacing blockers fast, in the room with
people who can act on them (Module 01, Level 2) — has nothing to do with
requirements uncertainty; it's a communication-bandwidth mechanism (Module
03, Level 1) that helps *any* team coordinate daily work, regardless of
whether the overall plan is fixed or adaptive. This is why the right answer
for Team C isn't "no agile practices at all" — it's isolating which specific
mechanism (iterative re-planning vs. daily communication) each agile
practice provides, and keeping only the ones whose underlying uncertainty
actually exists in this project.

## Exercise

Your portfolio includes: (1) a brand-new mobile app with unclear
requirements and eager users willing to give feedback, (2) an IT helpdesk
team fielding a continuous, unpredictable stream of tickets, and (3) a
one-time data-migration project with a hard compliance deadline and fully
specified requirements. For each, use the decision framework to name the
methodology you'd choose and the specific characteristic (from the first
table) that drove the choice.
