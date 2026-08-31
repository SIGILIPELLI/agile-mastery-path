# 05 · Definition of Done & Definition of Ready

Two short checklists — one gating entry into a sprint, one gating exit —
prevent most of the mid-sprint surprises teams blame on "bad requirements"
or "bad estimation." This module treats them as a single system rather than
two independent artifacts.

## Two gates, two purposes

| | Definition of Ready (DoR) | Definition of Done (DoD) |
|---|---|---|
| Gates | Entry into a sprint | Exit from a sprint (or a story) |
| Owned by | Product Owner, validated by team | Whole team |
| Answers | "Can we confidently start this?" | "Is this actually finished?" |
| Scope | Per story | Usually team- or increment-wide, plus per-story acceptance criteria |
| Changes how often | Rarely — it's a quality bar for backlog items | Rarely, but should grow as engineering maturity grows |

A team with a strong DoD but no DoR still pulls in vague stories and
discovers mid-sprint they don't know what "done" for *that story*
specifically means. A team with a strong DoR but weak DoD ships
inconsistent quality — "done" means something different depending on who
finished the ticket.

## A representative Definition of Done

| Level | Example criteria |
|---|---|
| Code | Peer-reviewed, merged, follows style guide |
| Tests | Unit tests written and passing, coverage doesn't drop |
| Quality | No new critical/high static-analysis findings |
| Integration | Merged to main, CI green |
| Documentation | User-facing docs or changelog updated if behavior changed |
| Acceptance | Product Owner has verified against the story's acceptance criteria |

DoD is layered: some criteria apply to every single story (code review,
tests); others apply once per sprint or release (regression suite,
performance check). Conflating the two makes the DoD too heavy to check per
story.

## A representative Definition of Ready

See Module 03 for the full INVEST-based checklist (Independent, Negotiable,
Valuable, Estimable, Small, Testable). The DoR is intentionally the
*minimum* bar — a story doesn't need every detail resolved, just enough for
the team to commit to it confidently.

## A worked example

A team's velocity is volatile: some sprints finish everything early, others
carry 40% of stories over. Diagnosis:

1. Inspecting the DoD reveals it only says "code merged" — no test or
   review requirement. Some stories ship with zero tests, inflating
   apparent velocity while accumulating defects that resurface later as
   unplanned work.
2. Inspecting the DoR reveals it doesn't exist — the PO writes one-line
   stories and the team estimates them on the spot in Planning.
3. Fix: the team writes an explicit DoD (code review + tests + PO
   acceptance) and a DoR checklist, and applies the DoR as a literal
   checklist item on the Planning board — no story enters Planning without
   a check next to each DoR item.

Three sprints later, carryover drops to under 10% and defect reports
trace-backed to "missing tests" fall to zero, because incomplete work no
longer counts as done.

## Exercise

Write a Definition of Done (5–7 criteria) and a Definition of Ready (5–6
criteria) for a team building a mobile app feature. Then take one vague
story ("add push notifications") and (1) show what's missing against your
DoR, (2) rewrite it so it passes, and (3) list which of your DoD criteria
would have caught a bug that shipped without tests.
