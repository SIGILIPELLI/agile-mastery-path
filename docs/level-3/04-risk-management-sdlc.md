# 04 · Risk Management Across SDLC Phases

Waterfall front-loads risk analysis into one upfront phase; Agile spreads
risk management across every sprint, but that only works if someone
actually does it deliberately rather than assuming short cycles
automatically dissolve risk. This module gives a phase-aware risk practice.

## Risk categories and where they concentrate

| Risk category | Concentrates in | Example |
|---|---|---|
| Requirements risk | Early (discovery, backlog formation) | Misunderstood user need |
| Technical/architecture risk | Early-to-mid (design, first builds) | Chosen approach doesn't scale |
| Schedule/scope risk | Ongoing, spikes near release | Underestimated stories, scope creep |
| Integration risk | Mid-to-late | Two teams' components don't compose as assumed |
| Operational risk | Late (release, post-release) | Deployment failure, unhandled load |
| Compliance/legal risk | Can appear at any phase | A late-discovered regulatory requirement |

## A lightweight risk register

| Field | Purpose |
|---|---|
| Risk description | One sentence, specific, not vague ("integration may be hard") |
| Likelihood (L/M/H) | Rough, not false-precision |
| Impact (L/M/H) | What breaks if it happens |
| Trigger/signal | The specific observable that means it's happening |
| Mitigation | What reduces likelihood or impact, and by when |
| Owner | A person, not a team |

Likelihood × Impact gives a rough priority (High/High first), but the
**trigger/signal** column is what actually makes a risk register useful day
to day — it converts "watch out for X" into a specific, checkable
condition someone can notice during normal work.

## Where Agile helps risk management, and where it doesn't automatically

| Agile mechanism | Risk benefit | What it doesn't cover |
|---|---|---|
| Short sprints | Surfaces requirements/technical risk within weeks, not months | Doesn't surface risks nobody thought to name in the register |
| Sprint Review | Validates against real stakeholder feedback early | Doesn't substitute for a deliberate architecture risk-spike |
| Retrospective | Surfaces process/team risk | Rarely surfaces external risk (vendor delay, compliance change) |
| Backlog reprioritization | Can de-risk by resequencing risky work earlier | Only works if risky items are *tagged* as such in refinement |

The key discipline: tag genuinely risky backlog items during refinement
(Module 03, Level 2) and deliberately schedule them **earlier**, even if
they're not the highest business value, specifically to buy down risk while
there's still time to react — this is often called a "risk-based spike" or
"walking skeleton" approach.

## A worked example

A team building a payments integration doesn't register the third-party
payment gateway's undocumented rate limits as a risk — it isn't visible
until week 9 of a 12-week project, when load testing suddenly fails.

Retrospective analysis: the risk register, if it had existed, should have
had "third-party gateway may have undocumented limits under load" logged
in week 1 with trigger "load test throughput below X" and mitigation
"run a small-scale load test against the gateway in sprint 1, not sprint
9." For the next project of similar shape, the team adds a standing rule:
any story involving an unfamiliar third-party dependency gets a
risk-register entry and an early, small-scale spike in the first sprint
that touches it — regardless of that story's business priority ranking.

## Exercise

For a project integrating with an unfamiliar external API under a fixed
deadline: (1) list three risks across at least two categories from the
table, (2) write a full risk-register row (all six fields) for the highest
Likelihood×Impact one, (3) propose a risk-based spike you'd schedule in
sprint 1 rather than by business priority alone, and (4) name the specific
trigger/signal that would tell you the mitigation isn't working and the
risk is materializing anyway.
