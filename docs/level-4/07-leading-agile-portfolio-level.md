# 07 · Leading Agile at Portfolio Level

At the portfolio level, the unit of work isn't a story or a sprint — it's an
investment decision across many products and teams, competing for finite
capacity. Agile principles still apply, but the tools change: backlogs
become investment themes, and "sprint planning" becomes capital allocation.

## Portfolio-level agile concepts

| Team-level concept | Portfolio-level equivalent |
|---|---|
| Product backlog | Portfolio backlog of epics/investment themes |
| Sprint planning | Quarterly (or PI-based) capacity allocation across themes |
| Definition of Done | Portfolio-level exit criteria (an initiative is "done" when it hits a measurable business outcome, not just ships) |
| Retrospective | Portfolio-level inspect-and-adapt: which bets paid off, which didn't, and why |

## Prioritizing at portfolio scale: WSJF

Weighted Shortest Job First (from SAFe) prioritizes by economic value
divided by effort, favoring high-value, low-effort work and explicitly
penalizing large, slow-to-deliver bets that tie up capacity for a long time.

| Component | Question it answers |
|---|---|
| User/business value | How much value does this unlock? |
| Time criticality | Does the value decay if delayed (e.g., a market window)? |
| Risk reduction / opportunity enablement | Does this reduce risk or unlock other future work? |
| Job size (denominator) | How much capacity does this consume? |

WSJF score = (value + time criticality + risk reduction) ÷ job size. Rank
by score, not by whoever has the most political capital to push their
initiative up the list.

## Governing without micromanaging teams

| Portfolio-level lever | What it controls | What it must NOT control |
|---|---|---|
| Which initiatives get funded/staffed | Investment allocation | How the funded team runs its sprints internally |
| Exit criteria for an initiative | What "success" means at the business level | The team's technical implementation choices |
| Quarterly re-prioritization | Whether an initiative keeps its funding into the next period | Fixing scope irrevocably for a whole year |

## A worked example

A portfolio committee is choosing among four proposed initiatives with a
fixed capacity of 40 team-quarters for the next year: a large platform
rewrite (high estimated value, very high effort, no time pressure), a
compliance-driven feature (moderate value, moderate effort, hard external
deadline), a customer-requested integration (high value, low effort, no
deadline pressure), and an internal tooling improvement (low direct
business value, low effort, reduces risk of a known recurring incident).

Scoring each with WSJF surfaces that the customer-requested integration
(high value, low effort) and the compliance feature (moderate value, hard
deadline, so effectively high time-criticality) score highest, while the
platform rewrite — despite being the initiative most executives are excited
about — scores lowest, since a large denominator (job size) dominates.
Rather than funding the rewrite first because of its visibility, the
committee funds the two highest-WSJF items fully, allocates a smaller
protected slice to the tooling improvement (justified by risk reduction
rather than raw value), and defers the platform rewrite to next quarter's
re-prioritization once the higher-scoring bets have delivered.

## How It Actually Works

WSJF's real function is forcing a hidden variable — the *opportunity cost of
time* — into a decision that would otherwise be made on visibility and
political capital, and the platform-rewrite scoring last is the direct
mechanical consequence of what the formula deliberately penalizes.

**Why job size sits in the denominator, not as a separate factor to
"consider."** Two initiatives with identical total value produce very
different economic outcomes if one takes one quarter and the other takes
eight — the fast one returns its value (and frees capacity for the next
bet) seven quarters sooner, which compounds across everything that capacity
could have been used for in the meantime. Placing job size in the
denominator makes this compounding effect explicit and comparable across
very differently-shaped initiatives, rather than leaving "but it'll take
years" as a vague, easily-overridden caveat attached to an otherwise
impressive value story — which is exactly the caveat that gets waved away
when the initiative also happens to be the one executives are most excited
about.

**Why time criticality has to be scored separately from raw value, not
folded into it.** Two initiatives can unlock identical dollar value, but if
one's value decays with delay (a market window, a regulatory deadline) and
the other's doesn't, treating them as equally urgent misallocates capacity —
the decaying-value initiative loses real value for every quarter it waits,
while the stable one loses nothing by waiting. This is precisely why the
compliance feature outranks the platform rewrite despite lower raw value:
its effective urgency (hard external deadline) is a cost of delay the
rewrite simply doesn't carry, and WSJF's separate time-criticality term is
what makes that difference visible in the ranking instead of buried in
qualitative discussion.

**Why "exit criteria, not implementation" is the correct governance
boundary, and violating it recreates enterprise micromanagement.** A
portfolio committee dictating a team's internal technical choices is making
a decision with far less context than the team actually has about its own
codebase and constraints — this is the identical authority-mismatch failure
as Module 03, Level 4's stage-gated CAB reviewing every release regardless
of risk, or Module 05, Level 4's coach becoming a mandatory approval step:
a higher layer inserting itself into decisions the lower layer is better
positioned to make. Setting the exit criterion (a measurable business
outcome) and then stepping back is what lets the portfolio layer govern
*what* gets funded without recreating the very micromanagement agile
principles were adopted to remove at the team level.

## Exercise

Score these three initiatives with WSJF (use a 1-10 scale for each
component, effort 1-10 for job size) and justify your numbers: (1) a new
market-entry feature with high value but a 6-month delivery window and no
external deadline, (2) a security patch required by a regulator in 60 days,
moderate effort, (3) a UX polish item, low effort, no deadline, modest
value. State which you'd fund first under limited capacity and why, and
name one thing the portfolio committee should NOT dictate to the team once
an initiative is funded.
