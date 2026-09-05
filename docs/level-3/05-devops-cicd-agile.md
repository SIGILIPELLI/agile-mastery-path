# 05 · DevOps & CI/CD Integration with Agile

Agile shortens the *planning* feedback loop to weeks; DevOps and CI/CD are
what shorten the *technical* feedback loop to minutes. Without them, a team
can run perfect two-week sprints and still only actually ship to production
once a quarter — this module covers why both loops need to be short
together.

## Two feedback loops, not one

| Loop | Shortened by | Answers |
|---|---|---|
| Planning/product loop | Scrum events, sprints | "Are we building the right thing?" |
| Technical delivery loop | CI/CD pipeline, automated testing, deployment automation | "Can we actually ship what we built, safely, right now?" |

A team can have excellent Sprint Reviews demoing "done" work that then sits
in a release-candidate branch for two months waiting on manual QA and a
change-advisory-board meeting — Agile ceremonies alone don't guarantee fast
technical delivery.

## The CI/CD pipeline as an extension of the Definition of Done

| DoD criterion (Level 2, Module 05) | CI/CD equivalent |
|---|---|
| Code peer-reviewed | Pull request gate, required approvals |
| Tests passing | Automated test suite runs on every commit |
| No new critical findings | Automated static analysis / security scan in the pipeline |
| Merged to main, CI green | Continuous Integration step |
| Deployable | Continuous Delivery: automated build + deploy to a staging/production-like environment |

Framed this way, CI/CD isn't a separate initiative from Agile process — it's
the *automation* of the Definition of Done, removing the manual toil that
otherwise makes "done" mean "done, pending a two-week manual release
process."

## Deployment strategies that keep releases low-risk

| Strategy | How it works | Fits well with |
|---|---|---|
| Feature flags | Ship code dark, turn on for users independently of deploy | Decoupling "deploy" from "release," letting Sprint Review demo features safely before general rollout |
| Trunk-based development | Small, frequent merges to main instead of long-lived branches | Short sprints, avoiding integration risk (Module 04) piling up |
| Canary/blue-green deploys | Roll out to a small slice of traffic first | Catching operational risk before it hits everyone |

## DevOps culture, not just tooling

Pipelines alone don't produce DevOps outcomes if the org still has separate
Dev and Ops teams with a ticket-based handoff between them — that's the
same handoff latency Agile eliminated between Product and Dev, just moved
one step later. The cultural shift mirrors Scrum's own: "you build it, you
run it" collapses the same silo CI/CD collapses technically.

## A worked example

A team ships "done" stories every sprint per its Definition of Done, but a
separate Ops team still manually deploys once a month after a change
request form. Sprint Reviews demo working software that stakeholders can't
actually use for weeks. Diagnosis: the team's DoD stops at "merged to
main," but delivery to real users is gated by a process outside the team's
control.

Fix, over two quarters: (1) the team adds an automated staging deploy on
every merge, closing the gap between "merged" and "deployed to a
production-like environment"; (2) feature flags are introduced so new work
can be merged and deployed dark, then turned on progressively; (3) the
manual change-request gate is renegotiated to apply only to flag flips, not
every code deploy, since deploys themselves are now low-risk and reversible.
Time from "done" to "usable by real users" drops from a month to same-day.

## How It Actually Works

The worked example's core failure — "done" stories sitting unusable for a
month — happens because two feedback loops that look identical on a Scrum
board (both produce a green checkmark) are actually measuring different
things, and closing one does nothing to close the other.

**Why feature flags solve a *sequencing* problem that sprints alone
cannot.** A Sprint Review's demo and a real user's access to a feature are,
by default, the same event — the code has to be live in production for
either to happen. That coupling forces a false choice: either delay
deployment until a feature is fully polished (defeating the point of
incremental delivery) or expose half-finished work to every real user the
moment it merges. Feature flags break the coupling by separating "the code
is deployed" from "the code is switched on for users" into two independent
decisions — the team can deploy continuously (closing the technical loop)
while the product decision of *when* to expose a feature stays entirely
separate and reversible, which is exactly why Sprint Review can safely demo
dark-shipped work: nothing about demoing it commits the team to exposing it
broadly yet.

**Why CI/CD is correctly framed as DoD automation, not a parallel
initiative.** The manual version of "code peer-reviewed, tests passing, no
critical findings" requires a human to remember and execute each check every
time — which means its actual enforcement rate depends on human diligence
under sprint-end time pressure, exactly the condition where checklist steps
get silently skipped (Module 05, Level 2's DoD-erosion mechanism, again). A
pipeline enforces the identical checklist as a mechanical gate that cannot
be skipped under pressure, because it isn't a person choosing whether to run
it — it runs on every commit regardless of how rushed anyone feels. This is
why "CI/CD is automating the DoD" isn't a metaphor: it's structurally
removing the exact human failure point that causes DoD erosion in teams
without it.

**Why fixing the pipeline without fixing the Dev/Ops handoff changes
nothing end-to-end.** Little's Law (Module 04, Level 2) applies just as
much to an org-level value stream as to a Kanban column: total time from
"done" to "usable" is the sum of every stage's wait time, and a
lightning-fast CI pipeline followed by a month-long manual Ops queue still
produces a month-long total, because the bottleneck — the slowest stage —
dominates the sum regardless of how fast the other stages run. This is why
the worked example's real fix isn't step 1 (automated staging deploy) alone
— it's step 3, renegotiating the change-request gate itself, because that
manual approval queue was always the actual bottleneck, and speeding up
everything upstream of a bottleneck has almost no effect on total
throughput.

## Exercise

For a team whose Definition of Done currently stops at "merged to main,
tests passing": (1) map each DoD criterion to its CI/CD automation
equivalent using the table above, (2) name one deployment strategy from the
table you'd add and why it fits this team's risk profile, (3) identify one
non-technical organizational handoff (like the Ops example) that would
still block fast delivery even with a perfect pipeline, and (4) propose one
concrete change to remove it.
