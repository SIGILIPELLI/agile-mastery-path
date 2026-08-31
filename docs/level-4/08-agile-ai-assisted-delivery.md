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

## Exercise

Your team has adopted an AI coding assistant and story throughput has
doubled, but two production incidents in the last month traced back to
AI-generated code that passed review too quickly. Using this module's
framework: (1) name one Definition-of-Done addition that would have caught
this class of bug, (2) decide whether WIP limits should move up or down and
justify it, (3) propose how you'd re-baseline estimates without simply
inflating apparent velocity, and (4) name one ceremony where AI assistance
is appropriate and one where you'd deliberately keep it out.
