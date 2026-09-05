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

## How It Actually Works

The reason "money for nothing, change for free" fixes what a fixed-scope
appendix breaks is that it changes the vendor's *incentive gradient*, not
just the paperwork — and incentive gradients, not good intentions, are what
actually determine vendor behavior under a contract.

**Why a fixed feature-list appendix makes the vendor's rational move the
wrong move for the client.** Once a vendor is paid a fixed price for a
fixed list of 40 features, their profit is maximized by delivering exactly
that list with minimum rework — any client request to reorder or swap
scope is, from the vendor's economic position, pure downside (more work, no
more money) unless a change order captures the difference. This isn't
vendor bad faith; it's the contract's own structure making "defend the
original scope" the financially rational strategy. The two-week
change-order cycle in the worked example isn't bureaucratic friction that
appeared by accident — it's the vendor's only mechanism for being paid for
the extra work a scope change implies, so slowing it down (or making it
costly) is aligned with the vendor's incentives, not opposed to them.

**Why swapping (not just adding) is the specific mechanism that keeps price
fixed while scope stays flexible.** A pure change-order model treats new
requests as *additions* requiring new payment — which is exactly what makes
reprioritization expensive. "Change for free" instead treats a new priority
as a *substitution* for equal-sized not-yet-started scope: the total
committed work-volume never changes, only its composition does, which means
the vendor's revenue is unaffected by the swap and there's no financial
reason to resist it. This is the contract-law equivalent of Module 09,
Level 2's mid-sprint trade-off rule (something equal-sized must leave for
something new to enter) — the same conservation principle, just enforced at
contract scope instead of sprint scope.

**Why the kill-fee clause is what actually aligns vendor sequencing with
client value, not the sprint reviews alone.** Sprint reviews make quality
and progress visible, but visibility alone doesn't change what the vendor
is paid to build first — a vendor could demo diligently every sprint while
still working through the appendix in its own preferred order. The
possibility of early termination is what makes sequencing matter: if the
client can walk away after any sprint and only pay for what's delivered,
the vendor's revenue now depends on delivering the *highest-value* work
early, because that's the scope most likely to actually get paid for before
a potential stop. The kill fee converts "please prioritize value" from a
request into a financial incentive the vendor cannot ignore.

## Exercise

Your organization is about to sign a 6-month, fixed-price contract with an
external vendor for a new internal tool, and stakeholders admit priorities
will likely shift after the first two months. Draft: (1) which contract
model from the table you'd propose and why, (2) two contract clauses that
keep the backlog reorderable without renegotiating price, (3) one governance
mechanism to keep quality visible sprint-by-sprint instead of only at final
acceptance, and (4) the specific condition under which the client could end
the engagement early and what they'd owe.
