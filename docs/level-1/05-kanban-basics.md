# 05 · Kanban Basics (WIP Limits & Pull System)

Kanban is a **flow-based** method for managing work, in contrast to Scrum's
**iteration-based** approach. There are no sprints, no fixed-length
timeboxes, and no dedicated Product Owner role in the original Kanban
Method — instead, work items flow continuously across a visual board, and
the entire system is regulated by one core mechanism: a limit on how much
work is allowed to be "in progress" at once.

## The board, and the pull system

A Kanban board is a set of columns representing stages of work, each
optionally carrying a **Work-In-Progress (WIP) limit** — a hard cap on how
many items may sit in that column at once.

| Backlog | Analysis (WIP 3) | Development (WIP 4) | Review (WIP 2) | Done |
|---|---|---|---|---|
| 30 items waiting | 2 / 3 | 4 / 4 (**full**) | 1 / 2 | — |

The critical rule: **Development is full. Nobody may pull a new item into
Development, even if they finish their current task early**, until an item
leaves Development for Review. This is what "pull" means — work is pulled
into a stage only when there's open capacity downstream, never pushed in
because someone happens to be free. A developer who finishes early doesn't
start something new from the backlog; they go help unblock whatever's stuck
in Review, because clearing the bottleneck grows the team's total throughput
more than starting a seventh item ever would.

## Why WIP limits are the whole point

Without a WIP limit, the instinct on every team is to **start** as much work
as possible — it feels productive. Kanban's core insight is that starting
work is not the same as finishing it, and a team measured on what's
*finished* (not what's started) needs a mechanism that fights the instinct to
start. A full WIP limit forces a decision: help finish something already in
flight, or do nothing — and "do nothing" is deliberately built in as more
acceptable than starting a new item, because a growing pile of half-finished
work is a worse outcome than an idle person for an hour.

| Symptom | What it reveals | Kanban's answer |
|---|---|---|
| Lots of items "in progress," few finished each week | Too much WIP relative to team capacity | Lower the WIP limits until flow visibly improves |
| One column is perpetually full | That stage is the bottleneck | Add capacity there, or pull people from earlier stages to help clear it |
| Items sit untouched for days between stages | Handoff friction, not effort — the work is "in progress" but nobody is actively on it | Track and reduce this "wait time" specifically, separate from active work time |

## Kanban's six core practices (brief)

1. **Visualize the workflow** — every stage of work becomes a column,
   nothing is invisible or "in someone's head."
2. **Limit WIP** — as above; this is the mechanism, not a suggestion.
3. **Manage flow** — actively watch how items move and fix what's slow.
4. **Make policies explicit** — write down what "ready to pull" and "done"
   mean for each column, so pulling decisions aren't ad hoc.
5. **Implement feedback loops** — regular reviews of the board and metrics
   (cadence, not a fixed sprint — could be weekly).
6. **Improve collaboratively, evolve experimentally** — change one policy
   at a time and observe the effect, rather than redesigning the whole
   board at once.

## A worked example: a 3-person support team adopts Kanban

A three-person customer-support engineering team fields incoming bug
reports at unpredictable rates — Scrum's fixed sprint doesn't fit because
work arrives continuously and priorities shift daily (a production
outage can't wait for the next sprint planning). They set up:

`Backlog → Triage (WIP 3) → In Progress (WIP 2) → Verify (WIP 2) → Done`

In week one, they notice **Verify** is constantly full — QA capacity is the
bottleneck, not development. Two developers respond by pulling zero new
items into In Progress for half a day and instead pairing to clear the
Verify backlog. By week three, average time from Triage to Done drops from
6 days to 3.5 days — not because anyone worked harder, but because the WIP
limit forced attention onto the actual constraint instead of letting
everyone stay "individually busy" while total throughput stagnated.

## How It Actually Works

WIP limits work because of a real, provable relationship in queueing theory —
**Little's Law** — not because "focus is a nice idea." It states:

`Average Time in System = Average Work In Progress / Average Throughput`

Rearranged, this says: for a fixed throughput rate, more WIP mechanically
*means* longer time-in-system, not just correlates with it. This is why the
support team's cycle time dropped from 6 days to 3.5 days without anyone
working harder — they didn't increase throughput, they decreased WIP, and the
formula forced the average time-per-item down as a direct consequence, not a
side effect of morale or effort.

**Why an idle developer is the correct outcome, mechanically.** When
Development is full and a developer finishes early, starting a new item
increases WIP without increasing the rate at which items complete — by
Little's Law, that action can only make cycle time *worse* for every item
already in flight, because now there are more things sharing the same finite
throughput. Going to help clear the Review bottleneck instead doesn't just
"feel like teamwork" — it's the only action available that increases
effective throughput at the actual constraint, which is the one lever that
improves the formula's outcome. This is a direct application of the Theory
of Constraints: a system's total throughput is capped by its slowest stage,
so effort spent anywhere else is invisible in the final number.

**Why "wait time" and "work time" have to be tracked separately.** An item
that sits untouched between two columns for three days isn't costing anyone
active effort, but it is fully counted in the numerator of Little's Law — it
inflates time-in-system exactly as much as three days of someone actively
working it would. Teams that only track "hours worked per item" miss this
entirely, because the biggest lever on cycle time in most real workflows
turns out to be handoff delay (something waiting for a reviewer, an
approval, an environment) rather than the work itself — which is why
practice #5 (explicit feedback loops reviewing the board) exists: it's the
mechanism for actually noticing where time is being lost.

## Exercise

Design a Kanban board for a real or invented workflow (support tickets,
content publishing, a personal task list — anything with distinct stages).
Define at least 4 columns with a WIP limit for each middle column (not
Backlog or Done), and write the explicit "pull policy" for one column (what
must be true about an item before it can move in). Then write a short
scenario, in the style of the support-team example, where a column hits its
WIP limit and describe exactly what the team should do in response —
specifically justify why they should *not* just raise the WIP limit to make
the friction go away.
