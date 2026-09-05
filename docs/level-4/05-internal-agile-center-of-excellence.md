# 05 · Building an Internal Agile Center of Excellence

Once an organization has more than a handful of agile teams, ad hoc coaching
(one senior person helping whoever asks) stops scaling. A Center of
Excellence (CoE) formalizes how practices, coaching, and standards spread
without becoming a bureaucratic layer that slows teams down.

## What a CoE should and shouldn't do

| Should | Shouldn't |
|---|---|
| Curate and share practices that worked, with evidence | Mandate a single framework/process for every team regardless of context |
| Provide coaching capacity teams can pull from | Insert itself as a required approval gate on team decisions |
| Run a community of practice connecting practitioners across teams | Become the only place agile knowledge lives, creating a bottleneck |
| Track org-wide health metrics to guide where coaching capacity goes | Use those metrics to rank or punish teams |

## A CoE operating model

| Component | Purpose |
|---|---|
| Charter | Explicit scope: what the CoE owns (coaching capacity, practice library, community of practice) vs. what stays with teams (day-to-day process choices) |
| Coaching pool | A small number of experienced coaches, allocated to teams based on need, not permanently embedded everywhere |
| Practice library | A living, curated set of practices with context on when each applies — not a mandated playbook |
| Community of practice | Regular, opt-in cross-team sessions where practitioners share real problems and solutions |
| Health metrics | Org-wide signals (e.g., team-reported psychological safety, cycle time trends) used to prioritize coaching investment |

## Funding and sizing

| Organization size | Typical CoE shape |
|---|---|
| Under ~100 engineers | 1-2 part-time coaches, informal community of practice |
| 100-500 engineers | Small dedicated team (3-5), practice library, quarterly cross-team retro-of-retros |
| 500+ engineers | Federated model — a small central CoE plus embedded coaches per business unit, connected by a shared community of practice |

A CoE that grows headcount faster than the organization it serves is a
warning sign it's drifting toward a control function rather than an
enabling one.

## A worked example

A 300-engineer organization stands up a CoE by hiring five coaches and
having them each embed permanently into five teams, effectively becoming a
required approval step for any process change ("check with your coach
first"). Within a year, teams report the coaches as a bottleneck, and
several teams quietly stop engaging with the CoE altogether, reverting to
ad hoc practices with no visibility for anyone.

Diagnosis against the "should/shouldn't" table: the CoE became a mandatory
gate instead of a pulled resource, and it never established a community of
practice so knowledge stayed siloed within each coach's five teams. The
reset: coaches rotate through a shared pool that teams request time from
(pull, not permanent assignment); a monthly community-of-practice session is
established where any team can bring a real problem; and the practice
library is opened for any team to contribute to, not just the coaches —
shifting the CoE from a gate to a shared resource.

## How It Actually Works

The permanent-embed CoE's collapse in the worked example follows the same
authority-versus-service structural failure that shows up throughout this
level (Module 02's directing-vs-coaching, Module 03's gate-vs-automated-
check) — a support function that becomes a mandatory checkpoint stops being
judged on whether it helps and starts being judged on whether it can be
avoided.

**Why "check with your coach first" inevitably becomes a bottleneck,
regardless of coach quality.** The moment a coach's approval is required
before a team can act, the coach's time becomes a hard constraint on every
one of their five teams' throughput — this is a direct application of the
Theory of Constraints from Module 05, Level 1: whatever process step
everything must pass through caps the system's total speed at that step's
capacity, no matter how fast the rest of the pipeline moves. Five embedded
coaches gating five teams' worth of decisions is structurally identical to
a single reviewer gating a Kanban "In Review" column (Module 04, Level 2) —
the fix there (rotate the bottleneck, cap WIP) is the same fix applied here
(rotate coaches through a shared, pulled pool instead of a fixed
one-to-one gate).

**Why permanent embedding also starves the community-of-practice
mechanism.** A coach permanently assigned to five teams accumulates deep,
valuable context — but that context stays trapped inside those five teams'
boundaries unless something forces cross-pollination. This is the same
silo problem Module 02, Level 3 diagnoses for distributed multi-team
dependencies: knowledge that only exists in one place is knowledge that
can't help anyone outside that place, and a CoE without a deliberate
sharing mechanism (the monthly cross-team session) recreates exactly the
information-isolation problem it exists to solve, just relocated from
teams to coaches.

**Why health metrics have to be explicitly protected from becoming a
ranking tool, not just informally discouraged.** The moment a metric like
"team-reported psychological safety" is visible in a format that ranks
teams against each other, it triggers the identical Goodhart's Law dynamic
as Module 06, Level 2's velocity leaderboard: teams start optimizing their
self-reported score rather than their actual psychological safety, because
the visible ranking creates a reputational incentive stronger than the
metric's original diagnostic purpose. Using the metric only to *route
coaching investment* (not to publish comparisons) keeps it functioning as
the honest signal it was designed to be, for exactly the same reason
velocity stays honest only when nobody's rewarded for inflating it.

## Exercise

Your 150-engineer organization has no formal agile support function today;
coaching happens informally when a manager personally knows someone
knowledgeable. Design a CoE for this scale: (1) how many coaches, and pooled
or embedded, (2) one thing the CoE will explicitly NOT have authority over,
(3) one org-wide health metric you'd track and how you'd avoid it becoming a
team-ranking tool, and (4) the first community-of-practice topic you'd
schedule, based on a real problem this organization is likely facing at
this stage of maturity.
