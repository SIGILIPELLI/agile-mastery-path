# 10 · Capstone — Full Organizational Agile Transformation Roadmap

This capstone combines every module from Levels 1-4 into one deliverable: a
full transformation roadmap for an organization, the way a Director of
Agile or Head of Transformation would actually present one to executive
leadership.

## The scenario

A 400-engineer software company, organized into 12 product teams plus a
shared platform group, currently runs ad hoc project management: fixed
annual budgets, quarterly project plans, no consistent ceremonies across
teams, and a reputation internally for slow, unpredictable delivery.
Leadership has approved an 18-month transformation with an executive
sponsor, but no dedicated budget increase — the roadmap must work within
existing headcount.

## Step 1: Foundational team practices (Level 1)

Every team pilot starts with the fundamentals: Scrum roles clarified,
backlog and estimation practices established, and a working Definition of
Done — the base every later layer depends on.

## Step 2: Deepened team maturity (Level 2)

Pilot teams add real retrospectives (not status meetings), velocity
tracking used for forecasting rather than performance comparison, and
working agreements that protect the team from silent scope creep.

## Step 3: Change-management approach (Level 4, Module 01)

Rather than a big-bang mandate across 400 engineers, the roadmap uses a
pilot-then-scale pattern: 2 teams in month 1-3, expanding to the full
organization by month 12, anchored by a change coalition including
respected senior engineers and at least two skeptical managers deliberately
recruited rather than avoided.

## Step 4: Scaling and dependency management (Level 3)

As teams beyond the pilot come online, a lightweight Scrum-of-Scrums
handles cross-team dependencies, with the shared platform group's backlog
gaining a class-of-service lane for requests blocking other teams (Level 3,
Modules 01, 07).

## Step 5: Coaching model (Level 4, Module 02, 05)

A CoE of 3 pooled coaches (drawn from internal Scrum Masters, not new
hires, respecting the no-budget-increase constraint) supports pilot and
scaling teams, backed by a monthly community of practice open to all 400
engineers.

## Step 6: Governance fit (Level 4, Module 03)

The existing quarterly Change Advisory Board is redefined to review only
high-risk changes (identified by an automated risk classifier); standard
changes deploy continuously with an auto-generated audit trail, satisfying
the same compliance requirement without gating daily delivery.

## Step 7: Portfolio-level prioritization (Level 4, Module 07)

The annual fixed-budget project model is replaced with quarterly WSJF-based
re-prioritization across the 12 product teams, funding teams as persistent
units rather than one-off fixed-scope projects.

## Step 8: Measurement plan (Level 4, Module 06)

| Dimension | Metric | Baseline source |
|---|---|---|
| Speed | Lead time for changes | Pulled retroactively from existing ticket timestamps |
| Stability | Change failure rate | Newly instrumented from the deploy pipeline starting month 1 |
| People | Quarterly engagement/psychological-safety survey | New survey, first run in month 1 as the baseline |
| Business | Time-to-market on the next 3 major initiatives | Compared against the last 3 completed initiatives under the old model |

## Step 9: 18-month timeline

| Phase | Months | Milestone |
|---|---|---|
| Pilot | 1-3 | 2 teams running full Level 1-2 practices; baseline metrics captured |
| Early scale | 4-8 | 6 teams onboarded; CoE and Scrum-of-Scrums operating; CAB redefinition live |
| Full scale | 9-14 | All 12 teams plus platform group; portfolio WSJF prioritization live |
| Consolidate | 15-18 | Metrics reviewed against baseline; hiring/promotion criteria updated to anchor gains (Kotter step 8) |

## How It Actually Works

This roadmap's nine steps aren't independently good ideas stacked together —
each later step depends on an earlier step already being real, and the
sequencing itself is the actual design, not just a scheduling convenience.

**Why Step 1-2's team-level fundamentals have to exist before Step 4's
scaling layer means anything.** A Scrum-of-Scrums or class-of-service lane
coordinates *between* teams that already have a functioning internal
process — Module 07, Level 3's dependency-visibility mechanisms assume each
team already has honest velocity, a real Definition of Done, and a backlog
that isn't fiction. Scaling coordination onto teams whose own Sprint
Backlogs are guesses (no real DoR/DoD, per Module 05, Level 2) just
coordinates noise faster — this is why the timeline gates "early scale"
(months 4-8) behind the pilot teams demonstrably running real Level 1-2
practices first, not just on a calendar schedule.

**Why the deliberately-recruited skeptical managers matter more than the
respected senior engineers.** Module 01, Level 4 diagnosed the failed
200-engineer rollout as missing exactly this: middle management, the layer
that controls incentives and resourcing, wasn't part of the coalition. A
coalition of only enthusiastic senior engineers builds technical credibility
but does nothing to address the review-cycle and budget-reporting decisions
that live with managers — recruiting skeptics specifically (not avoiding
them) means the objections that would otherwise surface as passive
resistance in month 9 get raised and answered in month 1, when the roadmap
can still adapt.

**Why the CAB redefinition (Step 6) and the portfolio funding shift (Step 7)
have to land roughly together, not sequentially at either extreme.**
Quarterly WSJF re-prioritization (Module 07, Level 4) assumes teams can
actually ship against changing priorities without waiting on a governance
bottleneck — funding flexibility without release flexibility just produces
teams that are told to reprioritize but can't deploy the result any faster
than before (the exact CAB-batching failure from Module 03, Level 4). This
is why both appear in the same "full scale" phase: one changes what gets
funded, the other changes how fast funded work reaches production, and
neither alone closes the gap between "leadership wants faster delivery" and
delivery actually being faster.

**Why baselining starts in month 1, not after the transformation is
declared complete.** Module 06, Level 4's central lesson — that
"improvement" is unfalsifiable without a captured "before" — is why Step 8's
baseline collection is scheduled at the very start of Step 9's timeline,
concurrent with the pilot, rather than retrofitted at month 18 when
leadership asks for a results readout. A transformation that only starts
measuring once someone wants to know if it worked cannot actually answer
that question, regardless of how well the rollout itself went.

## Capstone deliverable — what to produce

For an organization of your own choosing (or this scenario), produce:

1. A rollout pattern decision (big bang / pilot-then-scale / grassroots)
   with justification tied to organization size and risk tolerance.
2. A named change coalition (roles, not just titles) including at least one
   deliberately-recruited skeptic.
3. A governance redesign for at least one real compliance/approval
   bottleneck, specifying the automated mechanism that replaces manual
   gating.
4. A portfolio-level prioritization mechanism (e.g., WSJF) replacing fixed
   annual project budgets.
5. A 4-dimension measurement plan (speed, stability, people, business) with
   a stated baseline source for each metric.
6. An 18-month phased timeline with concrete milestones per phase.
7. One sentence stating how gains will be anchored (Kotter's step 8) so the
   transformation survives sponsor turnover or leadership change.
