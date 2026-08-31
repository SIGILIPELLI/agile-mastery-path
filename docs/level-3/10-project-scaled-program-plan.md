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
