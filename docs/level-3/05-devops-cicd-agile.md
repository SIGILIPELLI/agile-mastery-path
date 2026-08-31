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

## Exercise

For a team whose Definition of Done currently stops at "merged to main,
tests passing": (1) map each DoD criterion to its CI/CD automation
equivalent using the table above, (2) name one deployment strategy from the
table you'd add and why it fits this team's risk profile, (3) identify one
non-technical organizational handoff (like the Ops example) that would
still block fast delivery even with a perfect pipeline, and (4) propose one
concrete change to remove it.
