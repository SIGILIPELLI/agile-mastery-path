# 01 · Agile Transformation & Change Management

Rolling out agile across an organization is a change-management problem
first and a process problem second. Teams that get the mechanics right
(Scrum events, boards, tools) but ignore how people experience change end up
with "agile theater" — the ceremonies exist, the mindset doesn't.

## Why transformations stall

| Failure mode | What it looks like | Root cause |
|---|---|---|
| Mandated from the top, no buy-in | Teams run standups because they're told to, not because it helps them | Change imposed, not co-designed |
| Framework-first, outcome-second | Success measured by "are we doing Scrum right" | No connection drawn to the business problem agile was meant to solve |
| Middle-management left out | Team level adopts agile; managers still run project plans and status reports the old way | The layer that controls incentives and resourcing wasn't part of the change |
| No slack for the learning curve | Teams expected to hit full velocity from sprint one | Ignores that new ways of working are genuinely slower before they're faster |

## A change-management model for agile rollout

Kotter's 8-step model maps directly onto agile transformation:

| Step | Applied to an agile rollout |
|---|---|
| Create urgency | Name the specific business pain (missed deadlines, quality escapes, slow time-to-market) driving the change |
| Build a coalition | Recruit respected engineers and managers as early adopters/champions, not just executives |
| Form a vision | One sentence describing what "good" looks like in 12 months, in outcome terms, not process terms |
| Communicate the vision | Repeatedly, through multiple channels, connected back to the named pain |
| Empower action | Remove structural blockers (rigid budgeting cycles, siloed approvals) that make agile behavior impossible even for willing teams |
| Generate short-term wins | Pick 1-2 pilot teams likely to succeed; publicize their results early |
| Consolidate gains | Use pilot success to expand, adjusting the approach based on what was learned, not copy-pasting it verbatim |
| Anchor in culture | Update hiring, promotion, and performance-review criteria to reward the new behaviors, not just the old ones |

## Choosing a rollout pattern

| Pattern | How it works | Best for |
|---|---|---|
| Big bang | All teams switch at once | Rare cases with strong top-down mandate and small org size |
| Pilot-then-scale | 1-2 teams first, lessons applied before wider rollout | Most organizations — lower risk, real proof points |
| Grassroots | Individual teams opt in organically, coaching follows demand | Cultures resistant to mandates; slower but more durable |

## A worked example

A 200-engineer organization mandates "everyone does Scrum" starting next
quarter, with all teams trained in a single two-day session and expected to
run full ceremonies immediately. Six months later, most teams are running
standups as status meetings, sprint commitments are treated as immovable
deadlines by management (defeating the purpose of iterative replanning),
and velocity is used to compare and rank teams — driving estimate inflation.

Diagnosis using the model above: no coalition was built (training was
one-directional, not co-designed with team input), no short-term win was
established before scaling to 200 people at once, and the change wasn't
anchored — performance reviews still reward individual output over team
outcomes. The reset: the organization pauses the org-wide mandate, selects
two willing pilot teams with engaged managers, runs an 8-week pilot with a
dedicated coach, and only expands further once those two teams can show a
concrete before/after result the rest of the org recognizes as real.

## How It Actually Works

The 200-engineer rollout failed at a specific, identifiable point — not
"lack of enthusiasm" but a broken feedback loop between the visible layer
(ceremonies) and the invisible layer (incentives) that actually drives
behavior, and every symptom in the worked example traces back to that one
gap.

**Why performance-review criteria override any ceremony, mechanically.**
People optimize for what they're actually measured and rewarded on, not for
what a training session told them to value — this isn't cynicism, it's
rational behavior under the org's real incentive structure. If reviews still
score individual output, a developer correctly perceives that helping a
teammate finish their story (the self-organizing behavior Scrum depends on,
Module 04, Level 1) costs them personally while looking busy on their own
tickets pays off at review time. Running standups doesn't change this
calculation at all — the ceremony sits on top of an unchanged incentive
layer, which is exactly why "anchor in culture" is Kotter's *last* step, not
an optional add-on: skip it and every earlier step's gains erode back toward
whatever the real incentives reward.

**Why treating sprint commitments as immovable deadlines defeats the exact
mechanism Scrum relies on.** A Sprint Backlog is supposed to be a forecast
the team re-plans against as reality unfolds (Module 09, Level 1) — but if
management treats the committed point total as a fixed deadline the way a
Waterfall milestone would be treated, the team's rational response is to
protect against being wrong by inflating estimates (the exact velocity-
inflation mechanism from Module 06, Level 2, now driven by management
pressure instead of a leaderboard). The ceremony (Sprint Planning) survived
the rollout; the underlying trust relationship that makes its numbers
honest did not, because nothing in a two-day training session changed how
management actually reacts to a missed sprint.

**Why "big bang, no pilot" removes the one thing that makes later steps
possible.** Kotter's "generate short-term wins" step exists because belief
that the new way of working *actually helps* has to be built from evidence,
not instruction — a 200-person simultaneous rollout has no early, visible
proof point anyone can point to when skepticism arises in week 3, because
every team is equally unproven at the same time. A pilot generates exactly
the evidence a skeptical middle manager needs to justify changing their own
behavior (the "empower action" step) — without it, the change has no social
proof to draw on, and reverts to whatever behavior the *actual* incentive
structure (still unreformed) rewards.

## Exercise

Your organization wants to move 6 teams from ad hoc project management to
Scrum within two quarters. Using Kotter's model: (1) write the one-sentence
urgency statement naming a real business pain, (2) name three roles/people
types you'd recruit for the change coalition and why, (3) choose a rollout
pattern from the table and justify it against this org's size, and (4)
name one structural blocker (budgeting, approvals, reporting) that would
need to change for teams to actually behave differently, not just perform
differently.
