# 06 · Metrics & Reporting for Stakeholders

The metrics a team needs to run itself (cycle time, velocity range) are
rarely the metrics a stakeholder needs to make a decision. This module
covers translating internal delivery metrics into reporting that answers
the questions executives and clients actually ask.

## Internal metrics vs. stakeholder questions

| Stakeholder question | Wrong metric to lead with | Right translation |
|---|---|---|
| "Are we on track?" | Raw velocity number | Forecast range against the release plan (Level 2, Module 07) |
| "Is quality okay?" | Story point count | Defect trend, escaped-bug rate, DoD compliance |
| "Why did this slip?" | "Velocity dropped" | Named cause: scope change, dependency block, risk materializing (Module 04) |
| "What are we getting for our investment?" | Points delivered | Business outcomes tied to delivered features (adoption, revenue, retention) |

Reporting raw team-internal metrics to stakeholders (especially velocity —
see Level 2 Module 06) invites exactly the misuse that metric was designed
to avoid: comparison, target-setting, and blame, none of which the metric
supports.

## A stakeholder reporting structure

| Section | Content | Cadence |
|---|---|---|
| Status | On track / at risk / off track, one line | Every sprint or release checkpoint |
| Delivered this period | Business-language feature list, not ticket IDs | Every sprint |
| Forecast | Range, not a single date (Level 2, Module 07) | Every sprint, updated |
| Risks | Top 2–3 from the risk register (Module 04), plain language | Every sprint |
| Ask | What's needed from the stakeholder (decision, budget, feedback) | As needed |

The "Ask" row is the most frequently omitted and most valuable — a report
that only informs, without ever asking the stakeholder to decide something,
trains them to skim it rather than act on it.

## Choosing what NOT to show

| Internal artifact | Show to stakeholders? | Why |
|---|---|---|
| Burndown chart | Rarely as-is | Reads as behind schedule to someone unfamiliar with normal sprint variance |
| CFD (Level 2, Module 04) | Only to technically literate stakeholders | Requires explanation to avoid misreading |
| Release forecast range | Yes | Directly answers "when," honestly |
| Business-outcome dashboard (adoption, NPS, revenue) | Yes | Answers "was it worth it," which velocity never answers |

## A worked example

A program manager has been sending executives a weekly slide with each
team's velocity trend line. One team's velocity dips for two sprints (a
planned migration absorbed capacity) and an executive escalates, assuming
the team is underperforming. The Scrum Master reframes the next report
using the structure above: status is "on track — release forecast
unchanged," the dip is explained in the risks section as a planned,
time-boxed migration already factored into the forecast range, and the
"delivered this period" section lists the actual completed migration work
in business terms. The escalation resolves in one conversation, because the
report now answers "are we on track" directly instead of leaving the
executive to infer it from a graph never designed for that audience.

## How It Actually Works

The velocity-dip escalation in the worked example is a textbook case of a
correct internal signal being read by the wrong audience as a different,
incorrect signal — and the fix works because it addresses *why* the
misread happens, not just because it uses nicer words.

**Why a raw metric always gets interpreted through the reader's own mental
model, not the metric's actual definition.** Velocity was defined (Level 2,
Module 06) as a noisy, team-relative forecasting input with an expected
range of variation — dips are normal, not alarming, to someone who
understands the underlying distribution. An executive with no exposure to
that context has no such model; the only interpretation available to them
is the intuitive one everyone brings to a downward-trending line on a
slide — "this is getting worse." The chart isn't lying, but it's answering
a question ("what's the trend") the executive wasn't actually asking
("are we on track for the thing I approved budget for") — and a metric
answering the wrong question reliably produces a wrong conclusion even when
every number on it is accurate.

**Why "status: on track" plus a named cause resolves the escalation in one
pass, while the graph alone never could.** A release forecast range (Level
2, Module 07) already has the planned migration's capacity cost baked into
it — the report isn't hiding the dip, it's showing that the dip was already
priced into the number that actually answers the executive's real question.
Naming the specific, time-boxed cause converts an ambiguous downward trend
into a bounded, already-accounted-for event, which is the difference
between "something might be going wrong, indefinitely" and "something
specific happened, on schedule, for a known reason, and doesn't change the
forecast" — only the second version is actually reassuring, because only it
answers the causal question a worried reader is implicitly asking.

**Why omitting the "Ask" trains stakeholders to stop reading carefully.** A
report that only informs gives the reader no reason to engage with it beyond
skimming for bad news — there's nothing to *do* with the information, so
attention naturally drops over successive reports (this is the same
attention-allocation dynamic as Module 02, Level 2's action-item-graveyard:
things with no clear next action get deprioritized by the reader's own
brain). A report that regularly asks for a specific decision trains the
opposite habit — the stakeholder learns the report is a place where their
input actually changes something, so they read it as an active document
rather than a status broadcast to file away.

## Exercise

Given a sprint where the team completed 14 of 18 planned points because a
dependency on another team blocked one story: (1) write the one-line status
using the structure above, (2) write a "delivered this period" section in
business, not ticket, language, (3) write the risk-register-derived risk
entry in plain language, and (4) write a specific, answerable "ask" for the
stakeholder — not a vague "please be aware."
