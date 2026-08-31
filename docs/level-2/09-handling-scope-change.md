# 09 · Handling Scope Change Mid-Sprint

"Can you just squeeze this in?" is one of the most common pressures a Scrum
team faces, and how a team answers it determines whether Sprint commitments
mean anything. This module gives a decision framework instead of an
absolute rule.

## Sprint Goal as the filter, not "no changes ever"

Scrum doesn't forbid change — it protects the *Sprint Goal*, not the exact
list of tickets. The right question when a change request lands mid-sprint
is never "can the team fit it," it's "does accepting this still let us meet
the Sprint Goal."

| Request type | Sprint Goal impact | Typical response |
|---|---|---|
| Critical production bug | Threatens the goal if unfixed (outage, data loss) | Accept; renegotiate scope to compensate |
| "Nice to have while you're in there" | No bearing on the goal | Defer to backlog, refine for next sprint |
| Stakeholder changed their mind on a planned story | May or may not affect the goal | Discuss with PO; only mid-sprint change if goal is truly at risk otherwise |
| Executive escalation, unrelated to goal | Doesn't affect the goal by definition | Push back explicitly; log for next Planning |

## The trade-off rule

If new work genuinely must enter the sprint, something of *equal size* must
leave, decided by the Product Owner — not silently absorbed by the team
working overtime. This keeps the Sprint Goal achievable and keeps
stakeholders honest about the cost of "urgent" requests.

| Step | Who does it |
|---|---|
| 1. Assess Sprint Goal impact | Scrum Master + team |
| 2. If goal is at risk without the change, accept it | Team |
| 3. Identify equal-sized item(s) to remove | Product Owner, in front of the team |
| 4. Update the Sprint Backlog visibly | Whoever facilitates |
| 5. Note the change for the retro | Scrum Master |

## Why absorbing scope silently is worse than saying no

A team that always "finds a way" to squeeze in extra work without dropping
anything teaches stakeholders that the Sprint commitment is soft and
renegotiable at will — the next urgent request arrives just as casually.
Making the trade-off visible (something drops) is what keeps "urgent"
requests rare instead of routine.

## A worked example

Mid-sprint, a stakeholder asks the team to add a small compliance fix
"since it's quick." The Scrum Master runs it through the framework:

1. Sprint Goal check: the current goal is "ship the redesigned checkout
   flow." The compliance fix is unrelated.
2. Per the table, this is a "nice to have while you're in there" — no goal
   impact.
3. The Scrum Master declines the mid-sprint insertion, logs the item in the
   backlog, and confirms with the PO it will be prioritized for the next
   refinement session.
4. Two days later, a genuine production incident does threaten the
   checkout goal (a payment gateway bug). This time the team accepts the
   fix, and the PO removes an equivalent-sized lower-priority checkout
   story from the sprint in full view of the team.

The team said no once and yes once, using the same framework both times —
consistency, not a blanket rule, is what stakeholders learn to trust.

## Exercise

Invent three mid-sprint change requests of varying urgency (one clearly
Sprint-Goal-threatening, one clearly not, one ambiguous). For each: (1)
classify it using the table, (2) state the response, (3) for the one you
accept, name what equal-sized item you'd remove and who decides, and (4)
write one sentence you'd say to the stakeholder explaining the trade-off
out loud.
