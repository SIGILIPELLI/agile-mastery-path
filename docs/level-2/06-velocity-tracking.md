# 06 · Velocity Tracking

Velocity is the most commonly misused Agile metric — treated as a
productivity score, a cross-team comparison tool, or a management target,
none of which it was designed for. This module covers what velocity
actually is and the failure modes of using it wrong.

## What velocity is

Velocity is simply: **story points completed per sprint**, averaged over
several recent sprints. It exists for exactly one purpose — forecasting how
much a *specific team* can likely complete in a *future sprint*, based on
its own recent history.

| Correct use | Incorrect use |
|---|---|
| Forecasting this team's own capacity next sprint | Comparing Team A's velocity to Team B's |
| Sanity-checking Sprint Planning ("we're pulling 40 points, we usually do 28") | Setting velocity as a target to hit or exceed |
| Release forecasting: remaining points ÷ average velocity = sprints remaining | Using velocity in performance reviews |
| Spotting a real capacity change (illness, holidays, new hire ramp-up) | Comparing velocity across different estimation scales or teams |

Because story points are relative and team-specific (a "5" on one team
means nothing on another), any cross-team comparison is comparing
different units and produces meaningless conclusions — usually pressure to
inflate estimates, which is the well-known cause of "velocity inflation."

## Velocity inflation: cause and symptom

| Cause | Symptom | Fix |
|---|---|---|
| Velocity used as a target | Story points creep up for the same work | Stop using velocity as a KPI; use it only for forecasting |
| Cross-team comparison | Teams game their own scale to look "faster" | Compare throughput/cycle time trends instead, if comparison is needed at all |
| Partial-credit counting | Points counted for stories not fully done | Only count points for stories meeting the full Definition of Done |

## Using velocity for release forecasting

A simple, honest forecast uses a *range*, not a single number, because
velocity varies sprint to sprint:

| Input | Example |
|---|---|
| Remaining backlog | 140 points |
| Last 6 sprints' velocity | 18, 22, 15, 24, 19, 21 |
| Average velocity | ≈ 19.8 |
| Range (min–max) | 15–24 |
| Forecast | 140 ÷ 19.8 ≈ 7 sprints (best case ~6, worst case ~9) |

Presenting the range rather than the average alone sets more honest
stakeholder expectations and avoids the "you said 7 sprints" trap when
reality lands at 8.

## A worked example

A manager starts publishing a leaderboard ranking five teams by velocity.
Within two sprints, every team's average velocity rises 20–30% with no
corresponding increase in delivered features — teams have recalibrated
their own point scales upward to avoid looking slow. The Scrum Masters
diagnose this as velocity-as-target inflation and take it to the manager
with the release-forecasting table above: velocity is only meaningful
within one team's own consistent scale, and the leaderboard is comparing
units that were never equivalent. The fix is removing the leaderboard and
replacing it with each team's own release forecast range, reviewed
privately with each team.

## How It Actually Works

Velocity inflation isn't a discipline problem — it's a predictable
consequence of Goodhart's Law ("when a measure becomes a target, it ceases
to be a good measure") acting on a number that was only ever accurate
*because* nobody was optimizing it directly.

**Why the leaderboard breaks the measurement in exactly two sprints.** Story
points have no external anchor — a "5" means whatever the team's own past
"5"s meant, calibrated only by comparison within that team's own history
(Module 08, Level 1). The moment velocity becomes a visible, ranked
scoreboard, every team gains a direct incentive to move the one thing they
fully control — their own internal calibration — rather than the thing
leadership actually wants (more delivered value). Recalibrating "this is now
an 8, not a 5" costs nothing and immediately improves the ranking, so it's
the path of least resistance; actually delivering 20-30% more real work in
two sprints is not achievable at all, which is exactly how you can tell the
rise is inflation and not genuine improvement — the two are mechanically
distinguishable by whether shipped features increased to match.

**Why forecasting must use a range, and why a single number is actively
misleading.** Velocity is a noisy sample from sprint to sprint (illness,
an unexpectedly gnarly bug, a holiday week) — averaging 6 sprints gives a
central estimate, but the variance around it (15 to 24 in the example) is
real, recurring variation, not a mistake to average away. A stakeholder told
"7 sprints" hears a promise; told "6 to 9 sprints" hears a forecast — the
difference matters mechanically because reality landing at sprint 8 falsifies
the first framing and confirms the second, even though both came from
identical underlying data. This is the same statistical move as Module 09's
point-in-time capacity math: report the distribution, not just its center,
whenever the thing being forecast has meaningful variance.

**Why partial-credit counting corrupts the *next* forecast, not just the
current one.** If a team counts points for a story that's 90% done but not
fully meeting the DoD, this sprint's velocity number looks better, but next
sprint inherits the unfinished 10% as either invisible carryover or a
disguised new story — either way, the historical velocity series now
contains a number that doesn't represent what the team actually completed,
which means every future forecast built on that series (including the
6-sprint average above) is quietly built on a corrupted data point,
propagating the error forward indefinitely until enough clean sprints dilute
it.

## Exercise

Given a team's last 8 sprint velocities (invent plausible numbers with some
variance) and a backlog of 200 remaining points: (1) compute the average
and a min–max range, (2) produce a sprint-count forecast as a range, not a
single number, (3) identify one thing that would make you distrust this
forecast (e.g., a big backlog item with no split yet), and (4) explain in
one paragraph why comparing this team's velocity to another team's would be
invalid.
