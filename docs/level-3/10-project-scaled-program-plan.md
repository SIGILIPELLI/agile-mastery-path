# 10 · Project — Scaled Program Delivery Plan

This project combines every Level 3 module into one deliverable: a delivery
plan for a program spanning multiple teams, the way a Release Train
Engineer, program manager, or senior Scrum Master would build one.

## The scenario

Three teams (Checkout, Catalog, and Platform — 5 people each) are jointly
delivering a **new marketplace feature** launching in **12 weeks**. Checkout
and Catalog depend on a shared API that Platform owns. The client is
overseas and works 6 timezone hours ahead. The organization already runs
CI/CD and wants the launch delivered without a code freeze.

## Step 1: Scaling framework choice (Module 01)

A lightweight Scrum-of-Scrums model is chosen over full SAFe: three teams is
below the threshold where SAFe's overhead pays for itself, but informal
coordination alone won't catch cross-team dependencies at this scope.

## Step 2: Distributed-team working agreement (Module 02)

| Practice | Decision |
|---|---|
| Overlap window | 2 hours of daily overlap, used for the shared Scrum of Scrums plus any live pairing |
| Async default | Refinement and design docs written async first; sync time reserved for decisions, not information transfer |
| Documentation | Every cross-team API decision recorded in a shared doc within the overlap window, not left to chat history |

## Step 3: Delivery model (Module 03)

Feature work stays fully Scrum inside each team; the shared Platform API is
delivered Kanban-style with a class-of-service lane for "blocking another
team," which jumps the Platform backlog ahead of Platform's own internal
priorities.

## Step 4: Cross-SDLC risk register (Module 04)

| Risk | Phase | Mitigation |
|---|---|---|
| Shared API contract changes after Checkout/Catalog build against it | Design | API contract frozen and versioned before either dependent team starts integration |
| No code freeze, but a launch date is fixed | Release | Feature-flag every launch item; toggle off anything not ready by launch day |
| Overseas client feedback loop too slow for weekly iteration | Requirements | Client reviews a recorded walkthrough async, plus one live session per overlap window weekly |

## Step 5: CI/CD integration (Module 05)

Each team ships to a shared staging environment behind feature flags on
every merge; a nightly integration test suite runs across all three teams'
services so cross-team breakage surfaces the next morning, not at
launch-week integration.

## Step 6: Stakeholder metrics (Module 06)

| Metric | Audience | Cadence |
|---|---|---|
| Cross-team dependency burn-down | Program stakeholders | Weekly |
| Feature-flag readiness (% of launch scope toggle-ready) | Client + leadership | Bi-weekly |
| Cycle time on the Platform "blocking" lane | Program stakeholders | Weekly |

## Step 7: Dependency management (Module 07)

A shared dependency board tags every Checkout/Catalog story that needs the
Platform API, reviewed at a twice-weekly, 15-minute Scrum of Scrums capped
to cross-team blockers only.

## Step 8: Contract structure (Module 08)

The overseas client relationship runs on a T&M-with-cap model with a
"money for nothing" clause, so the fixed 12-week program budget can absorb
the client reprioritizing which non-launch-critical features ship in the
final two weeks.

## Step 9: Technical debt guardrail (Module 09)

Given the no-freeze, feature-flagged approach, the program reserves 10% of
each team's sprint capacity for debt incurred by flag scaffolding, with an
explicit backlog item to remove dead flags within two sprints of launch.

## How It Actually Works

This plan's nine decisions aren't independent choices bolted together — each
one is compensating for a specific failure mode that a different one of this
plan's own decisions would otherwise create, and seeing those cross-links is
what separates a coherent program plan from a checklist of separately-good
ideas.

**Why the class-of-service lane for Platform is what actually makes the
Scrum-of-Scrums choice viable.** Choosing lightweight coordination over SAFe
(Step 1) only works if the shared Platform dependency doesn't become an
unmanaged bottleneck — three teams below SAFe's overhead threshold (Module
01) still concentrate all cross-team risk onto one team's backlog the moment
two other teams depend on it. The "blocking another team" class-of-service
lane is the specific mechanism that prevents Platform's own internal
priorities from silently starving Checkout and Catalog — without it, the
lightweight coordination choice from Step 1 would be undermined by exactly
the kind of invisible dependency Module 07 describes.

**Why freezing the API contract before feature flags exist is a strict
prerequisite, not a parallel workstream.** Feature-flagging launch items
(Step 4's release risk) only de-risks the *release* date — it does nothing
about the *design*-phase risk that Checkout and Catalog are building against
a contract that might still change. If the API froze *after* both teams
started integrating, every subsequent change would ripple through both
teams' already-built code (the big-bang-integration mechanism from Module
02, Level 1), regardless of how good the feature-flag and no-freeze release
strategy is. This is why the plan sequences it as an early Design-phase gate
before either dependent team starts — the two risk mitigations target
different SDLC phases (Module 04) and neither substitutes for the other.

**Why the nightly cross-team integration suite has to exist alongside
feature flags, not instead of them.** Feature flags decouple *deployment*
from *user exposure* (Module 05) but say nothing about whether three teams'
services actually compose correctly when merged — that's a technical
integration question, not a release-sequencing one. Running the suite
nightly rather than only at launch-week is applying the same short-feedback-
loop principle from Module 01, Level 1 one level up: a compatibility break
found the morning after it's introduced costs one day's rework; the same
break found during launch week, after weeks of further work built on the
broken assumption, costs the entire program's remaining schedule.

**Why the debt-scaffolding guardrail is aimed specifically at flags, not
debt in general.** A no-freeze, feature-flagged approach necessarily
accumulates a *specific, predictable* kind of debt — dead flags and their
branching logic — that ordinary Boy-Scout cleanup (Module 09) won't
naturally catch, because a dormant flag doesn't get touched by future
feature work the way the checkout-module example's hardcoded coupling did.
Reserving capacity with an explicit removal deadline compensates for the
one place this program's chosen delivery style creates debt that its own
normal maintenance cycle wouldn't otherwise surface.

## Program deliverable — what to produce

For a multi-team program of your own choosing, produce:

1. A scaling-framework decision (lightweight Scrum-of-Scrums, SAFe, or
   another) with one sentence justifying the choice against team count and
   dependency density.
2. A distributed-team working agreement covering overlap hours and the
   async/sync split.
3. A 3-item cross-SDLC risk register spanning at least two different SDLC
   phases.
4. A CI/CD integration plan describing how cross-team breakage is caught
   before launch, not during it.
5. A 3-metric stakeholder reporting cadence.
6. A dependency-visibility mechanism plus its meeting cadence.
7. A contract-model decision for any external party, using the Module 08
   framework.
8. One technical-debt guardrail specific to the delivery approach chosen.
