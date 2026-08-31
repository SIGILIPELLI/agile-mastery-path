# 03 · Hybrid Agile-Waterfall Models

Most real organizations aren't purely Agile or purely Waterfall — a fixed
contractual milestone, a hardware dependency, or a regulatory gate often
forces some Waterfall-style sequencing around an Agile core. This module
covers doing that deliberately instead of by accident.

## Why pure models rarely survive contact with reality

| Constraint | Why it resists pure Agile | Why it resists pure Waterfall |
|---|---|---|
| Fixed hardware manufacturing lead time | Can't iteratively "release" a physical board mid-sprint | Waterfall alone ignores that the software running on it benefits from iteration |
| Government/regulatory approval gate | The gate itself is a hard, sequential milestone | Everything *except* the gate benefits from iterative delivery |
| Fixed-price client contract with a spec | Client wants a locked scope and price upfront | Delivery execution still benefits from sprints and continuous feedback |

## The "Water-Scrum-Fall" pattern

The most common hybrid shape: Waterfall-style phases at the edges (upfront
requirements/contracting, and final release/deployment/compliance
sign-off), with Agile iteration in the middle where uncertainty is highest
and feedback is most valuable.

| Phase | Style | Why |
|---|---|---|
| Requirements & contracting | Waterfall-like | Client/legal need a defined scope and price before committing budget |
| Build & design | Agile (sprints) | Highest uncertainty; iteration and feedback reduce risk fastest here |
| Release, compliance sign-off | Waterfall-like | Regulatory or deployment gates are inherently sequential and non-negotiable |

## Designing a hybrid deliberately

1. Identify which constraints are genuinely fixed and sequential (a
   regulatory gate, a hardware ship date) versus which are just *assumed*
   to be fixed out of habit.
2. Keep the sequential parts as small as possible — a locked scope
   document doesn't have to mean a locked *solution design*, just a locked
   *outcome and price*.
3. Run everything else — design, build, internal testing — as normal
   sprints with real Sprint Reviews, even inside a fixed-price contract.
4. Use the Definition of Done and release checklist (Module 03/05, Level 2)
   as the bridge artifact between the Agile middle and the Waterfall-style
   release gate.

## Where hybrids go wrong

| Failure | Symptom | Fix |
|---|---|---|
| "Agile" in name only | Sprints exist, but scope and design are fully locked upfront, so sprints just execute a plan with no real feedback loop | Ensure the contract locks *outcomes*, not implementation details, leaving room for the team to adapt *how* |
| Waterfall creeping into the middle | Every sprint needs sign-off from a change-control board before starting | Reserve heavyweight change control for genuinely fixed constraints, not internal iteration |
| No true iteration ever demoed to the client | Client only sees the work at the final Waterfall-style gate | Insist on Sprint Reviews with the client, even under a fixed-price contract — cheaper to catch misalignment early |

## A worked example

A vendor signs a fixed-price contract to build a hospital records feature,
which requires final regulatory sign-off (a hard, sequential gate). The
initial plan treats the entire project as Waterfall to satisfy the
contract's need for a locked price. Nine months in, the client discovers
the delivered UI doesn't match evolving clinical workflow needs — because
there was no feedback loop until the very end.

The team restructures for the next phase: the contract locks the *outcome*
(patient record access meeting a named regulatory standard) and price, but
the build itself runs as 2-week sprints with a client-facing Sprint Review
every sprint. The regulatory sign-off remains a genuine Waterfall-style gate
at the end — that part can't be iterative — but everything before it now
gets caught early instead of at a single final review.

## Exercise

For a project with a fixed government compliance deadline 6 months out and
a fixed-price contract: (1) identify which parts of the project are
genuinely sequential/fixed versus which are just assumed to be, (2) design
a Water-Scrum-Fall shape naming what happens in each phase, (3) propose one
way to keep the fixed-price contract while still allowing real client
feedback loops mid-project, and (4) name one specific failure mode from the
table above you'd watch for.
