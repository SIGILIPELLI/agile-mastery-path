# 08 · Estimation Basics (Story Points & Planning Poker)

Agile teams need to answer "how much can we commit to this sprint?" without
the luxury of a fully specified Waterfall plan to estimate against. The
standard tool is **story points** — a *relative*, unitless measure of size —
estimated collaboratively through a technique called **Planning Poker**.
Understanding why relative estimation works (and where it breaks) is more
valuable than memorizing the Fibonacci numbers themselves.

## Why relative sizing beats absolute time estimates

Humans are reliably bad at estimating absolute duration ("this will take 6
hours") but reliably good at relative comparison ("this is about twice as
big as that other thing we did"). Story points exploit the second skill and
avoid the first:

| Approach | What it asks | Why it fails / succeeds |
|---|---|---|
| Hours/days estimate | "How many hours will this take?" | Ignores that different developers work at different speeds, and anchors the team to false precision on something inherently uncertain |
| Story points | "Is this bigger, smaller, or the same size as this other thing we already built?" | Comparison is a skill people are actually accurate at; the team's own historical velocity (Module covered later) converts points into a real-world forecast without needing individual time estimates at all |

A story point encodes three things at once — complexity, effort, and
uncertainty/risk — not just "how long." A small task with high uncertainty
(e.g., "integrate with a vendor API we've never used") can rightly get more
points than a larger task the team has done many times before.

## The modified Fibonacci scale

| Points | 1 | 2 | 3 | 5 | 8 | 13 | 20 | 40 | 100 |
|---|---|---|---|---|---|---|---|---|---|
| Meaning | Trivial, well understood | Small | Small-medium | Medium | Large | Very large | Needs breaking down | Needs breaking down | Epic — not sprint-ready |

The widening gaps between numbers are deliberate: it's easy to tell a 3 from
a 5, but forcing a team to decide between "14 or 15 points" for something
genuinely large is false precision — Agile estimation gives up precision on
big items on purpose, because that precision was never real to begin with.
Anything estimated at 20+ should generally be split into smaller stories
before it enters a sprint (see the INVEST "Small" criterion from Module 7).

## Planning Poker: the procedure

1. The Product Owner reads a story and its acceptance criteria aloud.
2. Each team member privately selects a card (physical or in a Planning
   Poker app) showing their point estimate — privately, to avoid anchoring
   on whoever speaks first.
3. All cards are revealed simultaneously.
4. If everyone agrees, that's the estimate. If estimates diverge widely
   (e.g., a 3 and a 13), the highest and lowest estimators each explain
   their reasoning — often the low estimator missed a hidden complexity, or
   the high estimator misunderstood the scope.
5. Re-vote after discussion. Repeat until convergence, generally within 2–3
   rounds.

The simultaneous reveal is the entire point — a spoken-aloud go-around lets
the first, most confident voice anchor everyone else's number, which
defeats the purpose of independent relative judgment.

## A worked example: a Planning Poker session

The team is estimating "As a user, I want to reset my forgotten password via
email" (from Module 1's SDLC example).

| Round 1 votes | Dev A: 3 | Dev B: 3 | Dev C: 8 | QA: 5 |
|---|---|---|---|---|

Dev C's 8 stands out. Asked why, Dev C explains the team has never
integrated with the transactional email provider before, and there's
unknown setup work (DNS records, sender reputation) that isn't visible in
the story itself. That's new information for the rest of the team.

| Round 2 votes | Dev A: 5 | Dev B: 5 | Dev C: 5 | QA: 5 |
|---|---|---|---|---|

Consensus at **5**. The convergence came from surfacing a hidden
dependency, not from social pressure to agree — which is exactly what
Planning Poker's structured disagreement step is designed to produce.

## Common estimation pitfalls

| Pitfall | Why it happens | Fix |
|---|---|---|
| Points inflate over time | Team feels judged on velocity, so the same-sized work quietly gets called an 8 instead of a 5 | Never use velocity as a performance metric (Level 2 covers this) |
| Comparing one team's points to another's | Points are a *team-relative* unit, not a standard unit like hours | Never compare velocity or point scales across teams |
| Skipping the disagreement discussion when short on time | The convergence step is where hidden risk actually surfaces | Protect the 2–3 minutes it takes; it's cheaper than discovering the risk mid-sprint |
| Re-estimating stories after they're already in progress | Story points estimate *before* the work starts; once started, track remaining work in hours/tasks instead | Don't re-point a story mid-sprint — that corrupts the historical velocity data |

## How It Actually Works

Story points work as a forecasting tool for a specific statistical reason:
they convert an unreliable *absolute* judgment into a reliable *relative*
one, and then let the team's own historical throughput do the unit
conversion.

**Why comparison is more reliable than absolute duration, cognitively.**
Estimating "6 hours" requires modeling every step of an unfamiliar task in
your head and summing imagined durations — a process with compounding error
at each step, and no anchor against reality. Estimating "about twice as big
as the story we finished last week" only requires recognizing structural
similarity to something already experienced, which is a much shorter
inferential chain and degrades far less with unfamiliarity. This is the same
reason humans are bad at guessing a building's height in feet but good at
guessing "about three times as tall as that other building" — relative
judgment routes around the part of the estimate people are actually bad at.

**Why the conversion to real time has to happen later, in aggregate.** A
story point never claims to equal a fixed number of hours for any individual
story — a "5" might take one developer 4 hours and another 9, and the same
developer 3 hours on a good day and 7 on a day full of interruptions. What's
statistically stable is not any single estimate but the *team's average
points completed per sprint* (velocity, covered later) — averaging washes out
the individual noise the same way flipping a coin 100 times gives a much more
reliable estimate of its bias than flipping it once. This is precisely why
comparing velocity across teams is meaningless: each team's points-to-hours
ratio is a private constant baked into their own history, not a shared unit.

**Why simultaneous reveal is the mechanism that prevents information
collapse.** A sequential go-around turns four independent estimates into
one estimate plus three social confirmations — once Dev A says "3" out loud,
Dev B's "8" now carries social cost to state, so the group's four data points
degrade into effectively one. Simultaneous reveal preserves four independent
samples of the team's judgment, and it's specifically the *outlier* (Dev C's
8) that carries new information — the discussion step exists because an
outlier is usually outlier because they know something (a hidden dependency)
the rest of the room doesn't, not because they're wrong.

## Exercise

Write five stories of varying real or plausible complexity for a project of
your choice. Assign each a story point value from the Fibonacci scale, and
for each, write one sentence justifying the number by *comparing it to
another story in your list* (e.g., "this is a 5 because it's about twice as
complex as the 3-point story, since it touches an external API we haven't
integrated before"). Then simulate a two-round Planning Poker disagreement:
invent two team members who initially estimate one story very differently
(like the 3-vs-8 example), state the extra piece of information that
surfaces, and show the converged final estimate.
