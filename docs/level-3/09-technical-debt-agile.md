# 09 · Technical Debt in an Agile Delivery Model

Agile's short cycles and pressure to ship every sprint make it easy to
accumulate technical debt without anyone explicitly deciding to. This module
covers naming debt honestly, tracking it, and paying it down without
stopping feature delivery.

## Types of technical debt

| Type | Example | How it's usually incurred |
|---|---|---|
| Deliberate, tracked | "We'll hardcode this config to hit the demo deadline" | A conscious trade-off, logged for later |
| Deliberate, untracked | Same trade-off, never written down anywhere | The most dangerous kind — invisible until it bites |
| Accidental, discovered | A design that seemed fine turns out not to scale | Found through use, not foreseeable at the time |
| Bit rot | Code that was fine when written, now stale relative to newer patterns/libraries | Normal decay as the codebase and ecosystem evolve |

The dangerous quadrant is deliberate-and-untracked: it's a choice, but
nobody outside the moment it was made knows it exists.

## Making debt visible

| Technique | How it works |
|---|---|
| Debt log / backlog tag | Every known shortcut logged as a backlog item, tagged `tech-debt`, with the trade-off it made explicit |
| Debt-interest framing | Describe cost in terms stakeholders understand: "this slows every future story touching this module by ~20%" |
| Boy Scout rule | Small, opportunistic cleanup bundled into stories that touch the affected code, instead of always deferring |
| Dedicated capacity | A fixed percentage of each sprint (commonly 10-20%) reserved for debt paydown, protected like any other commitment |

## Deciding what to pay down first

| Signal | Priority |
|---|---|
| Debt in a module changed almost every sprint | High — interest compounds fastest here |
| Debt in code touched once a year | Low — the interest rarely comes due |
| Debt actively causing production incidents | Highest — it's no longer just slow, it's breaking |
| Debt only the original author understands (bus factor) | High — risk compounds independently of change frequency |

The rule of thumb: prioritize by *how often the debt is paid in interest*,
not by how uncomfortable it is to look at.

## A worked example

A team's checkout module accumulated debt over six months: a payment-gateway
integration was hardcoded for one provider "temporarily" during a launch
crunch, with no ticket ever filed. Nine months later, the business wants a
second payment provider, and every estimate for that work balloons because
the hardcoded assumption is threaded through five files with no clean
seam.

The team runs a retrospective focused specifically on this incident and
introduces two changes: every deliberate shortcut now requires a backlog
item tagged `tech-debt` before the sprint closes (making the deliberate
kind trackable), and the team commits a fixed 15% of each sprint's capacity
to debt paydown, prioritized using the interest-frequency signal rather than
gut feel. Six months later, the debt log shows the payment-gateway coupling
as the single highest-interest item (touched by four of the last six
features), and it gets scheduled and fixed before it blocks the next
required integration.

## Exercise

Your team just shipped a feature under deadline pressure by copy-pasting a
validation function instead of refactoring a shared one, and no one logged
it. Using this module's framework: (1) classify the debt type, (2) write
the backlog item that should have been logged, including its "interest"
description in stakeholder terms, (3) decide whether it belongs in the
current sprint's Boy Scout cleanup or the dedicated debt-capacity backlog
and justify the choice using the interest-frequency signal, and (4) propose
one process change that would make deliberate debt trackable going forward.
