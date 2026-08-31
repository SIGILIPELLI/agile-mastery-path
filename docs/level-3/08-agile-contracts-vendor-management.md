# 08 · Agile Contracts & Vendor Management

Agile assumes changing requirements; most commercial contracts assume fixed
scope. When a vendor or client relationship is governed by a contract, that
tension has to be resolved explicitly, or the contract quietly overrides the
agile process the moment money is on the line.

## Contract models and how they fit agile

| Model | How it works | Agile fit |
|---|---|---|
| Fixed price / fixed scope | Set price for a defined scope, agreed up front | Poor — any backlog reordering becomes a change-order negotiation |
| Time & materials (T&M) | Client pays for actual hours/effort | Good — supports iterative discovery, but gives the client little cost ceiling |
| T&M with a cap | T&M up to a not-to-exceed ceiling | Better — caps risk while keeping room to reprioritize |
| Money for nothing, change for free | Client can swap unstarted scope of equal size for new scope at no extra cost; can stop early and pay only for a partial "kill fee" | Best fit — explicitly designed for agile backlogs |
| Outcome/value-based | Payment tied to a measured business outcome, not hours or features | Strong fit in principle, hard to structure and verify in practice |

## Structuring an agile-friendly fixed-price deal

Fixed price doesn't have to mean fixed scope if the contract fixes the
*budget and cadence* instead of the feature list:

| Contract element | What it fixes | What stays flexible |
|---|---|---|
| Total budget / duration | Number of sprints and the rate | — |
| Definition of Done | Quality bar every increment must meet | — |
| Sprint review as a checkpoint | Cadence of demonstrated, inspectable progress | — |
| Backlog | — | Content and order, reprioritized every sprint by the client's PO |
| "Money for nothing" clause | — | Client can end early, paying only for delivered scope plus a small fee |

This shifts the vendor's incentive from "defend the original scope" to
"deliver the highest-value backlog items first," because the client can
stop paying once satisfied.

## Vendor governance without micromanagement

| Mechanism | Purpose |
|---|---|
| Vendor attends sprint review, not just final acceptance | Continuous, low-drama inspection instead of one high-stakes handoff |
| Shared Definition of Done, agreed before the contract starts | Removes "done" as a point of dispute at invoicing time |
| Independent QA/acceptance sampling each sprint | Catches quality drift early, before it compounds across many sprints |
| Escalation path defined in the contract (not improvised later) | Disagreements over scope/quality have a pre-agreed resolution route |

## A worked example

A company hires an external vendor to build a customer portal under a
fixed-price, fixed-scope contract with 40 features listed in an appendix. By
sprint 4, the client's priorities have shifted — 10 of the 40 features are
now low value, and 6 new features matter more. Under the original contract,
any change requires a formal change order, a two-week approval cycle, and a
price renegotiation; the vendor has no incentive to raise it since they're
already paid for the original list.

The fix, applied to the next contract renewal: total budget and sprint cadence
stay fixed, but the appendix is replaced with "money for nothing, change for
free" language — the client's PO can swap any not-yet-started feature for a
new one of equal or smaller size at every sprint boundary, and can end the
engagement early paying only a 20% kill fee on remaining budget. Sprint
reviews become the acceptance mechanism instead of a single end-of-project
sign-off. The vendor now has a direct incentive to sequence the
highest-value features first, since early termination is now a real
possibility.

## Exercise

Your organization is about to sign a 6-month, fixed-price contract with an
external vendor for a new internal tool, and stakeholders admit priorities
will likely shift after the first two months. Draft: (1) which contract
model from the table you'd propose and why, (2) two contract clauses that
keep the backlog reorderable without renegotiating price, (3) one governance
mechanism to keep quality visible sprint-by-sprint instead of only at final
acceptance, and (4) the specific condition under which the client could end
the engagement early and what they'd owe.
