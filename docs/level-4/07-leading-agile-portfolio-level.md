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

## Exercise

Score these three initiatives with WSJF (use a 1-10 scale for each
component, effort 1-10 for job size) and justify your numbers: (1) a new
market-entry feature with high value but a 6-month delivery window and no
external deadline, (2) a security patch required by a regulator in 60 days,
moderate effort, (3) a UX polish item, low effort, no deadline, modest
value. State which you'd fund first under limited capacity and why, and
name one thing the portfolio committee should NOT dictate to the team once
an initiative is funded.
