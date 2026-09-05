# 02 · The Waterfall Model

Waterfall is the SDLC run **once, straight through, in strict sequence**,
with a formal sign-off gate between each phase. The name comes from the
diagram: work flows downhill from Requirements to Maintenance, and — in its
purest form — never flows back upstream. It is the oldest documented software
process model (formalized by Winston Royce in 1970, ironically as a
description of a *risky* approach he was warning against) and it is still the
right choice for a specific, identifiable class of project.

## The phase gates

| Gate | What must be true to pass through it | Who signs off |
|---|---|---|
| Requirements → Design | Requirements are complete, unambiguous, and approved | Business sponsor / client |
| Design → Implementation | Architecture and detailed design reviewed | Technical lead / architect |
| Implementation → Testing | Code complete, matches design | Development lead |
| Testing → Deployment | All defined test cases pass, no open critical defects | QA lead / client acceptance |
| Deployment → Maintenance | System live, handover complete | Operations |

The defining trait is **each gate is expensive to reopen**. Discovering in
the Testing phase that a Requirements-phase assumption was wrong means
reopening a closed, signed-off phase — which in a strict Waterfall project
means a formal change request, re-approval, and rework of every downstream
artifact built on the wrong assumption.

## Why it exists, and where it genuinely wins

Waterfall isn't a mistake project managers made before Agile was invented —
it's the correct model when the cost structure of the project rewards
up-front certainty:

| Condition | Why Waterfall fits |
|---|---|
| Requirements are genuinely stable (e.g., a regulatory reporting format, a physical hardware spec) | There is nothing to discover mid-project that changes the plan |
| Fixed-price / fixed-scope contract | The buyer needs a firm, defensible cost and date before signing |
| Physical or safety-critical systems (avionics firmware, medical devices) | Changing course after fabrication/certification is enormously expensive or dangerous |
| Heavy compliance/audit requirements | Regulators expect a linear, fully-documented paper trail per phase |
| Distributed teams that can't easily sync daily | A written, complete specification substitutes for constant back-and-forth |

## A worked example: a govt. tax-filing portal migration

A government agency needs to replace a 15-year-old tax-filing system.
Requirements are set by law (specific forms, specific validation rules,
specific submission deadlines that cannot move), the contract is fixed-price
with a mandated go-live date tied to the next tax year, and an external
auditor requires a signed requirements-traceability matrix. This is a
textbook Waterfall fit:

1. **Requirements** (10 weeks): every tax form's fields and validation
   rules are documented and signed off by the tax authority's legal team.
2. **Design** (8 weeks): system architecture, database schema, and every
   screen wireframe reviewed and approved before a line of code is written.
3. **Implementation** (20 weeks): the vendor builds against the approved
   design, with no scope changes accepted without a formal change order.
4. **Testing** (8 weeks): a dedicated QA phase runs the full suite of
   validation rules against every form, cross-checked against the legal
   requirements document line by line.
5. **Deployment** (2 weeks): a scheduled cutover date, with a rollback plan
   back to the legacy system if go-live fails.
6. **Maintenance**: ongoing support contract for bug fixes and the next tax
   year's rule changes, treated as a new, smaller Waterfall cycle.

Running this as an Agile project instead would be a mismatch: a tax
authority's legal team is not going to "refine the backlog every sprint" on
a legally mandated form, and a fixed-price government contract usually
cannot legally absorb the kind of scope flexibility Agile assumes.

## Where Waterfall genuinely fails

| Failure mode | Why it happens |
|---|---|
| The "big bang" integration problem | Components built in isolation across months often don't fit together cleanly the first time they're actually combined, late in Implementation |
| Late discovery of misunderstood requirements | The customer doesn't see working software until Testing/Deployment — by which point a misunderstanding from Requirements is baked into everything |
| No room for market/user feedback | If user needs shift during the 6–12 months of a Waterfall project, there's no checkpoint to react to it |
| Sunk-cost pressure to ship anyway | Because so much is invested by the time defects surface, teams are pressured to ship known-flawed software rather than reopen a gate |

## How It Actually Works

The mechanism that makes Waterfall expensive to correct isn't bureaucracy for
its own sake — it's that each phase gate converts a *decision* into *sunk
work downstream*, and the cost of reopening a gate scales with how much has
been built on top of it.

**Why "big bang integration" happens mechanically, not accidentally.** When
Design produces a set of interface contracts (an API shape, a data schema,
a message format) and different teams then build against those contracts in
isolation for months, each team is implicitly making small interpretive
choices the contract didn't fully pin down — how a null field behaves, what
units a number is in, what happens on a timeout. Those choices are invisible
and consistent *within* one team's code, because they only get exercised
against that team's own assumptions. Integration is the first moment two
teams' interpretations actually collide, which is precisely why it surfaces
late (nothing before it exercised the seam) and expensively (weeks of
parallel work now have to be reconciled instead of one design conversation).

**Why the change-request process exists, and what it's actually doing.** A
formal change request isn't red tape — it's the mechanism that prices in the
cascading cost of a late change *before* anyone approves it. Changing a
requirement after Design is signed off means re-touching the design
artifacts derived from it, then the code derived from that design, then the
tests derived from that code, then possibly redoing sign-offs that already
happened. The change-request form is forcing someone to trace that
dependency chain and put a number on it, which is exactly the audit trail a
regulator or fixed-price client needs — and exactly the overhead that makes
Waterfall a bad fit once requirements are expected to move.

**Why sunk-cost pressure to ship is structural, not a personality flaw.**
Because Waterfall front-loads nearly all its spend into Requirements through
Implementation and only tests near the very end, the moment a critical
defect surfaces is also the moment the project has the least budget and
schedule left to absorb a phase reopening — the two things happen together
by construction, not coincidence. That's why "ship it, patch it later" is the
default outcome of a late Waterfall defect: reopening Testing → Design →
Implementation at 90% of budget spent is a bigger ask than accepting known
risk, even when the team knows better.

## Exercise

Take a real or hypothetical software project (choose something with either a
regulatory constraint, a fixed hardware dependency, or a fixed-price
contract — do not choose a typical consumer web/mobile app). Write out a
6-phase Waterfall plan for it: name a realistic duration for each phase, name
who signs off at each gate, and identify one *specific* requirement that, if
wrong, would be expensive to fix once you reach the Testing phase. Then write
two sentences arguing why this specific project is a genuinely better fit
for Waterfall than for Agile — referencing the "where it genuinely wins"
table above, not just "Waterfall is more organized."
