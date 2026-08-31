# 06 · Measuring Transformation Success

"Are we agile yet?" is the wrong question — it invites checklist theater
(are we doing the ceremonies) instead of measuring whether the
transformation delivered the business outcome it was meant to. This module
covers picking measures that reflect outcomes, not compliance.

## Outcome metrics vs. compliance metrics

| Compliance metric (avoid as a success measure) | Outcome metric (prefer) |
|---|---|
| % of teams "doing Scrum" (running the ceremonies) | Lead time from idea to production |
| Story points completed per sprint | Deployment frequency and change failure rate |
| Number of teams trained | Employee-reported engagement/psychological safety |
| Certification counts | Customer-reported satisfaction / NPS trend |

Compliance metrics are easy to game (run the meeting, skip the substance)
and easy to measure. Outcome metrics are harder to measure but much harder
to fake, because they reflect what actually reached customers or
employees.

## A balanced measurement set (DORA-adjacent, broadened)

| Dimension | Metric | What it reveals |
|---|---|---|
| Speed | Lead time for changes | How fast value reaches customers |
| Stability | Change failure rate, MTTR | Whether speed is coming at the cost of quality |
| People | Engagement/psychological-safety survey trend | Whether the transformation is sustainable, not just fast |
| Business | Time-to-market for new initiatives, customer satisfaction trend | Whether any of the above actually mattered to the business |

Track a small set across all four dimensions — optimizing only "speed"
metrics reliably produces stability regressions, and optimizing only
"people" metrics without tying to business outcomes makes the transformation
hard to defend at budget time.

## Baselining and cadence

| Step | Approach |
|---|---|
| Baseline before the change | Capture pre-transformation values for every chosen metric; without this, "improvement" is unfalsifiable |
| Set a realistic time horizon | Meaningful movement in lead time/stability usually takes 2-3 quarters, not weeks |
| Review quarterly, not weekly | Weekly noise in these metrics is normal; quarterly trend is the signal |
| Pair every metric with a story | A number without the human context behind it ("why did MTTR spike in Q2") won't survive stakeholder scrutiny |

## A worked example

A company's leadership declares its 18-month agile transformation a success
because 100% of teams now run Scrum ceremonies and average two
certifications per engineer. Six months later, customer complaints about
release quality have increased, and time-to-market for new features hasn't
measurably changed — the metrics leadership tracked were all compliance
metrics, and none of them detected the actual problem.

A retrospective on the measurement approach itself introduces a balanced
set: lead time (baselined against pre-transformation data pulled from old
ticket timestamps), change failure rate (newly instrumented from the
deploy pipeline), a quarterly engagement survey, and time-to-market on the
next three initiatives. Within two quarters, the new metrics show lead time
essentially unchanged despite the ceremony rollout — surfacing that the
real bottleneck was a manual, weekly-batch QA sign-off process the
transformation never touched, invisible to compliance metrics but obvious
in the outcome ones.

## Exercise

Your organization is six months into an agile transformation and leadership
wants a one-page success report. Using this module's framework: (1) name
one compliance metric currently being reported that should be dropped or
demoted, (2) choose one metric from each of the four dimensions (speed,
stability, people, business) to include instead, (3) state what
pre-transformation baseline you'd need for each and how you'd source it if
it was never captured, and (4) name the realistic time horizon you'd set
expectations against before claiming success or failure.
