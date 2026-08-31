# 10 · Project — Release Plan with Sprint Roadmap

This project combines every Level 2 module into one deliverable: a release
plan spanning several sprints, built the way a real Scrum Master or PO
would build one for a stakeholder-facing deadline.

## The scenario

You're the Scrum Master for a 5-person team building a **team task-tracking
tool** (think: a lightweight internal Jira). Leadership wants a first
public release in **10 weeks**. The team has three sprints of history.

## Step 1: Historical velocity (Module 06)

| Sprint | Points completed |
|---|---|
| -3 | 21 |
| -2 | 17 |
| -1 | 23 |

Average velocity ≈ 20.3; range 17–23.

## Step 2: Definition of Ready gate on the backlog (Modules 03, 05)

The raw backlog has 9 items; refinement (Module 03) splits the two largest
into 5 smaller stories each, and every item is checked against the team's
Definition of Ready (INVEST) before entering the release plan. Two items
fail "Testable" (no acceptance criteria) and are sent back to the PO before
being included below.

| # | Story | Points | Tier |
|---|---|---|---|
| 1 | Create/assign/close tasks | 5 | Must-have |
| 2 | Task board with drag-and-drop status | 8 | Must-have |
| 3 | Basic user accounts & login | 5 | Must-have |
| 4 | Comment on a task | 3 | Must-have |
| 5 | Email notification on assignment | 5 | Must-have |
| 6 | Search tasks by keyword | 3 | Nice-to-have |
| 7 | Task labels/tags | 2 | Nice-to-have |
| 8 | Dark mode | 3 | Nice-to-have |

Must-have total: 26 points. Nice-to-have total: 8 points.

## Step 3: Sprint roadmap (5 two-week sprints = the 10-week window)

Using average velocity (20.3) and the range (17–23), the must-have tier (26
points) forecasts to roughly **1.3 sprints** — but the release also needs a
Definition-of-Done pass, deployment work, and buffer, none of which is in
the story points. The team adds a release-hardening allowance instead of
inflating story estimates.

| Sprint | Planned content | Points | Notes |
|---|---|---|---|
| 1 | Stories 1–3 | 18 | Core CRUD + auth foundation |
| 2 | Stories 4–5, refinement for nice-to-haves | 8 | Must-have tier complete |
| 3 | Stories 6–8 (nice-to-have) | 8 | Buffer available if sprint 1–2 slip |
| 4 | Hardening: DoD-wide regression, security review, load test | — | No new stories; fixed cost of shipping |
| 5 | Buffer / bug-fix sprint + release | — | Held in reserve, not pre-committed |

## Step 4: Risk register (Module 04's flow-health lens applied to the plan)

| Risk | Likelihood | Mitigation |
|---|---|---|
| Login/auth story underestimated (new to this team) | Medium | Time-boxed spike in sprint 1, week 1, to surface unknowns early |
| Nice-to-have scope creep into "must-have" | Medium | PO reconfirms tier boundary at every sprint review |
| Sprint 4 hardening surfaces major defects | Low-medium | Sprint 5 held explicitly as buffer, not pre-filled with new features |

## Step 5: Working agreement addition for the release (Module 08)

The team adds one release-specific norm: "No new stories enter Sprint 4 —
it's regression and hardening only," preventing scope creep from quietly
eating the buffer sprint the same way Module 09's framework prevents
mid-sprint scope creep.

## Step 6: Stakeholder-facing summary

> **Release Plan**: Must-have task-tracking (create/assign/close, board,
> accounts, comments, notifications) ships by end of sprint 2 (week 4).
> Nice-to-have polish (search, labels, dark mode) ships by end of sprint 3
> (week 6) if velocity holds. Sprints 4–5 (weeks 7–10) are reserved for
> hardening and buffer before the public release date. **Confidence: high
> for must-have scope; medium for nice-to-have scope**, contingent on the
> auth spike in sprint 1 not surfacing major unknowns.

## Project deliverable — what to produce

For a product of your own choosing, produce:

1. A 3-sprint velocity history (or invented plausible numbers) with average
   and range.
2. A refined, DoR-checked backlog split into must-have and nice-to-have
   tiers with points.
3. A sprint-by-sprint roadmap covering a fixed release window, including at
   least one dedicated hardening/buffer sprint.
4. A 3-item risk register with likelihood and a concrete mitigation each.
5. One release-specific working agreement that protects your buffer sprint
   from scope creep.
6. A one-paragraph stakeholder-facing summary stating confidence level and
   naming the specific condition that confidence depends on.
