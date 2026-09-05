# 08 · Agile & AI-Assisted Delivery

AI coding assistants and agents change the economics of individual tasks —
often making implementation faster than estimation, review, or
integration. Agile practices built around human-only delivery speeds need
deliberate adjustment, or the bottleneck just moves without anyone noticing.

## What actually changes with AI-assisted delivery

| Old assumption | New reality |
|---|---|
| Writing code is usually the slowest step in a story | Writing code is often now faster than review, testing, and integration |
| Story point estimates reflect roughly human-only implementation effort | Estimates need to account for AI-accelerated implementation plus unchanged review/verification effort |
| One engineer, one story, sequential | An engineer can run several AI-assisted threads in parallel, raising WIP-limit questions |
| Code review checks for correctness and style | Code review also needs to check for AI-specific failure modes: plausible-looking but subtly wrong logic, hallucinated APIs, license/provenance issues |

## Adjusting the flow

| Practice | Adjustment for AI-assisted work |
|---|---|
| WIP limits | May need lowering, not raising — faster implementation can pile more unreviewed work into the review column than the team can actually verify |
| Definition of Done | Add explicit AI-specific checks: no hallucinated dependencies, no unreviewed generated tests asserting trivial/tautological conditions |
| Estimation | Re-baseline story points periodically; a task that was a 5 six months ago may genuinely be a 2 now, and pretending otherwise inflates apparent velocity for no reason |
| Pairing/review | Human review effort becomes the real constraint — invest coaching there, not in prompting technique alone |

## Where AI helps agile practice itself

| Ceremony/artifact | AI-assisted use | Caution |
|---|---|---|
| Backlog refinement | Drafting acceptance criteria, surfacing edge cases from a rough story description | Still needs human judgment on business priority and actual user need |
| Retrospective | Summarizing patterns across many past retro notes | Don't let it replace the team's own reflection — summaries can flatten real disagreement |
| Release notes / documentation | Drafting from commit/PR history | Needs a human accuracy pass before anything customer-facing ships |

## A worked example

A team adopts an AI coding assistant and initially celebrates a 3x increase
in story throughput. Within two sprints, the review queue backs up
severely, a subtle bug from AI-generated code (correct-looking but wrong
edge-case handling in a discount calculation) reaches production, and two
engineers report they're now spending more time reviewing generated code
than they used to spend writing it themselves — the team's real cycle time
hasn't actually improved.

The team responds by lowering its review-column WIP limit (rather than
raising the "in progress" limit as they'd initially planned), adding an
explicit Definition-of-Done item requiring a human-written test for any
business-logic branch introduced by generated code, and re-baselining
story points for a sample of recent stories to reflect that implementation
time dropped but review time didn't. The next retrospective tracks cycle
time specifically (not just story throughput), revealing the real
bottleneck moved to code review — prompting the team to invest coaching
time in review practices rather than further prompting technique.

## How It Actually Works

The team celebrating a "3x throughput increase" and then discovering
unchanged real cycle time is the Theory of Constraints (already seen in
Module 05, Level 1's Kanban mechanics) playing out with a twist: AI
assistance sped up a *non-bottleneck* stage, which by definition cannot
improve total system throughput at all.

**Why speeding up implementation alone cannot improve cycle time if review
was already the constraint.** In a pipeline of sequential stages
(implement → review → integrate), total throughput is capped by the slowest
stage — this is the same principle behind Module 04, Level 2's cycle-time
diagnosis. If review was already running at capacity before AI assistance
arrived, making implementation faster just means more finished work arrives
at the review queue's door per unit time, without review's own capacity
changing at all — the queue backs up, WIP balloons, and by Little's Law
(cycle time = WIP ÷ throughput), cycle time for any individual item actually
*worsens* even though "story throughput" (a misleading metric here, since
completion is gated by review, not implementation) looked like it tripled.

**Why lowering the WIP limit, not raising it, is the mechanically correct
response.** The intuitive move — more capacity upstream, so raise the "in
progress" ceiling to match — ignores that the actual constraint didn't move.
Raising a non-bottleneck stage's limit while the bottleneck stays fixed only
grows the queue in front of the bottleneck faster, which is exactly the
"lots of items in progress, few finished" symptom from Module 04, Level 2's
Kanban table. Lowering the review-column limit instead forces the same pull
discipline that fixes any bottleneck: work stops entering the pipeline
faster than the actual constraint (human review) can absorb it, which is
uncomfortable (developers producing code faster than it can be reviewed)
but is precisely the friction that reveals review as the true limiting
factor, rather than letting unreviewed AI output silently pile up
unverified.

**Why re-baselining estimates has to separate implementation time from
review time, not just adjust the total.** If a story's point value simply
drops because implementation got faster, without accounting for review
effort staying constant, the team's forecasting math (Module 06, Level 2)
silently breaks — the same point total no longer maps to the same real
elapsed time, because the ratio of implementation-to-review effort inside
that point has shifted. This is a subtler version of velocity inflation:
not gaming the number for appearance, but letting an unexamined change in
the underlying work composition corrupt the historical series anyway,
unless the team deliberately re-measures what a point represents now.

## Exercise

Your team has adopted an AI coding assistant and story throughput has
doubled, but two production incidents in the last month traced back to
AI-generated code that passed review too quickly. Using this module's
framework: (1) name one Definition-of-Done addition that would have caught
this class of bug, (2) decide whether WIP limits should move up or down and
justify it, (3) propose how you'd re-baseline estimates without simply
inflating apparent velocity, and (4) name one ceremony where AI assistance
is appropriate and one where you'd deliberately keep it out.
