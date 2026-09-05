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

## How It Actually Works

The financial-debt metaphor isn't decorative — technical debt behaves like
real debt in a specific, measurable way: it charges *interest* every time
someone has to work around it, and the interest rate scales with how often
that code path gets touched, which is exactly why the prioritization signal
in this module is change-frequency, not discomfort.

**Why the hardcoded payment-gateway assumption's cost compounds instead of
staying fixed.** Each new feature that touches the checkout module has to
work *around* the hardcoded provider assumption rather than through a clean
interface — meaning every one of the four features built between the launch
crunch and the discovery paid a small "interest" cost (extra time
navigating the coupling) without anyone tracking it as debt. By the time a
second provider is genuinely needed, the interest already paid across four
features plus the principal cost of the eventual refactor is far larger than
the cost would have been to build it cleanly the first time — this is
identical, mechanically, to compound interest: the debt itself didn't grow,
but the number of transactions charged against it did, and each one paid a
little more because the coupling had spread further (five files, not one).

**Why "deliberate and untracked" is specifically the most dangerous
quadrant, not just an inconvenient one.** Deliberate-and-tracked debt at
least gives someone downstream the chance to notice the tag and decide it's
worth paying down before it compounds. Deliberate-and-untracked debt is
invisible to everyone except the person who made the trade-off in the
moment — which means the decision to accept a shortcut effectively becomes
permanent by default (nobody manages what they can't see), even though the
original author might have happily flagged it for cleanup if asked. This is
why "log every shortcut before the sprint closes" is the single highest-
leverage fix in the worked example: it costs one sentence at decision time
and converts a permanent, invisible liability into a visible, manageable
one.

**Why dedicated capacity has to be protected like a real sprint commitment,
not treated as slack.** A percentage reserved for debt paydown that gets
silently reabsorbed into feature work under deadline pressure (the same
mid-sprint erosion pattern as Module 09, Level 2) never actually pays down
anything — it just becomes a line item that exists on paper while the debt
log grows unchecked sprint after sprint. Protecting it the same way a Sprint
Goal is protected (Module 09, Level 2's framework: something else has to
give if this capacity is claimed for something else) is what keeps the
paydown real instead of aspirational — which is precisely why the fix in
the worked example commits a *fixed* 15%, not a "we'll get to it when we
can" intention.

## Exercise

Your team just shipped a feature under deadline pressure by copy-pasting a
validation function instead of refactoring a shared one, and no one logged
it. Using this module's framework: (1) classify the debt type, (2) write
the backlog item that should have been logged, including its "interest"
description in stakeholder terms, (3) decide whether it belongs in the
current sprint's Boy Scout cleanup or the dedicated debt-capacity backlog
and justify the choice using the interest-frequency signal, and (4) propose
one process change that would make deliberate debt trackable going forward.
