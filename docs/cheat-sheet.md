---
title: "Agile & Software Delivery Cheat Sheet: Quick Reference, Beginner to Advanced"
description: "A free Agile & Software Delivery cheat sheet: 40 quick-reference tables from every level of the Agile & Software Delivery Mastery Path, each linked to its full lesson."
---

# Agile & Software Delivery Cheat Sheet

Quick-reference tables from **40 lessons** of the free Agile & Software Delivery Mastery Path, in course order from beginner to advanced. Each section links to the full lesson with explanations and runnable examples.

## Level 1 · Entry

### [01 · What Is the SDLC?](level-1/01-what-is-sdlc.md)

*The six phases, and what each one actually produces*

| Phase | Core question it answers | Typical output |
|---|---|---|
| 1. Requirements | What does the business/user actually need? | Requirements document, user stories, acceptance criteria |
| 2. Design | How will the system be structured to meet that need? | Architecture diagram, data model, UI wireframes, API contracts |
| 3. Implementation | Build the thing | Working code, unit tests |
| 4. Testing | Does it actually do what was specified, correctly? | Test results, defect log, sign-off |
| 5. Deployment | Get it into the hands of real users | Release, deployment runbook, rollback plan |
| 6. Maintenance | Keep it working and improve it over time | Bug fixes, patches, feature updates, monitoring |

### [02 · The Waterfall Model](level-1/02-waterfall-model.md)

*The phase gates*

| Gate | What must be true to pass through it | Who signs off |
|---|---|---|
| Requirements → Design | Requirements are complete, unambiguous, and approved | Business sponsor / client |
| Design → Implementation | Architecture and detailed design reviewed | Technical lead / architect |
| Implementation → Testing | Code complete, matches design | Development lead |
| Testing → Deployment | All defined test cases pass, no open critical defects | QA lead / client acceptance |
| Deployment → Maintenance | System live, handover complete | Operations |

### [03 · The Agile Manifesto &amp; Principles](level-1/03-agile-manifesto-principles.md)

*The four values, read correctly*

| We value... | ...over | The common misreading |
|---|---|---|
| Individuals and interactions | processes and tools | "Agile means no process" — wrong; it means process serves people, not the other way around |
| Working software | comprehensive documentation | "Agile means no documentation" — wrong; it means documentation must earn its keep, not become the deliverable itself |
| Customer collaboration | contract negotiation | "Agile means no contracts" — wrong; it means the relationship should stay collaborative even where a contract exists |
| Responding to change | following a plan | "Agile means no planning" — wrong; it means the plan is expected to update as you learn, not treated as fixed truth |

### [04 · Scrum Roles, Events &amp; Artifacts](level-1/04-scrum-roles-events-artifacts.md)

*The three roles*

| Role | Accountable for | Not accountable for |
|---|---|---|
| Product Owner | Maximizing product value; ordering the Product Backlog; single voice on what "done" is worth building next | *How* the work gets built, or estimating technical effort |
| Scrum Master | The team's effective use of Scrum; removing impediments; coaching the organization | Directing the team's day-to-day technical work or assigning tasks |
| Developers | Building a usable Increment each Sprint; managing their own work within the Sprint | Deciding *what* to build — that's the Product Owner's call |

### [05 · Kanban Basics (WIP Limits &amp; Pull System)](level-1/05-kanban-basics.md)

*The board, and the pull system*

| Backlog | Analysis (WIP 3) | Development (WIP 4) | Review (WIP 2) | Done |
|---|---|---|---|---|
| 30 items waiting | 2 / 3 | 4 / 4 (**full**) | 1 / 2 | — |

### [06 · Agile vs. Waterfall](level-1/06-agile-vs-waterfall.md)

*Head-to-head comparison*

| Dimension | Waterfall | Agile |
|---|---|---|
| Requirements | Fixed up front, formally signed off | Expected to evolve; captured as a living backlog |
| Delivery | One release at the end of the project | Incremental releases every sprint/iteration |
| Customer involvement | Concentrated at the start (requirements) and end (acceptance) | Continuous — every sprint review |
| Change mid-project | Formal change-request process, expensive | Expected and routine — the backlog absorbs it |
| Documentation | Comprehensive, produced per phase, often contractually required | "Just enough" — working software is the primary evidence of progress |
| Risk discovery | Late (often in Testing, near the end) | Early and often (every sprint surfaces new information) |
| Budget/schedule certainty | High, if requirements really are stable | Lower per-feature certainty, but total spend rate is knowable |
| Team structure fit | Works with a chain of specialist hand-offs across teams | Needs a small, cross-functional, co-located-or-well-synced team |
| Best contract type | Fixed-price, fixed-scope | Time-and-materials, or scope-flexible fixed-budget |

### [07 · User Stories &amp; Backlogs](level-1/07-user-stories-backlogs.md)

*The standard format, and why each part exists*

| Part | Purpose | What goes wrong if it's missing |
|---|---|---|
| Role | Identifies *whose* need this is | Stories become generic feature requests disconnected from a real user's actual problem |
| Capability | The concrete thing being asked for | Without it, there's nothing to build — this is the only part people usually remember |
| Benefit ("so that") | The *reason* the capability matters | Without it, a developer can't make good judgment calls on edge cases — they don't know what the feature is actually for |

### [08 · Estimation Basics (Story Points &amp; Planning Poker)](level-1/08-estimation-basics.md)

*Why relative sizing beats absolute time estimates*

| Approach | What it asks | Why it fails / succeeds |
|---|---|---|
| Hours/days estimate | "How many hours will this take?" | Ignores that different developers work at different speeds, and anchors the team to false precision on something inherently uncertain |
| Story points | "Is this bigger, smaller, or the same size as this other thing we already built?" | Comparison is a skill people are actually accurate at; the team's own historical velocity (Module covered later) converts points into a real-world forecast without needing individual time estimates at all |

### [09 · A Simple Sprint-Planning Exercise](level-1/09-sprint-planning-exercise.md)

*What Sprint Planning actually has to produce*

| Input to the session | Output of the session |
|---|---|
| Ordered Product Backlog | A Sprint Goal, in one sentence |
| Team's known capacity (people, days available, focus factor) | A Sprint Backlog: the specific stories pulled in |
| Historical velocity (if any sprints have run before) | A sanity check that total points pulled ≈ historical velocity |

### [10 · Capstone — Run a Mock 1-Week Sprint Plan](level-1/10-capstone-mock-sprint-plan.md)

*Step 1: Write the Product Goal and a starting backlog*

| # | Story | Acceptance criteria (abridged) |
|---|---|---|
| 1 | As a user, I want to log an expense with amount, category, and date, so I can build a spending history. | Amount must be > 0; category is chosen from a fixed list; date defaults to today but is editable. |
| 2 | As a user, I want to set a monthly budget per category, so I know my spending limits. | Budget is a positive number per category; can be edited any time; applies starting the current month. |
| 3 | As a user, I want to see my remaining budget per category, so I know what I can still spend. | Remaining = budget − sum of expenses this month, per category; updates immediately after logging an expense. |
| 4 | As a user, I want a warning when I'm within 10% of a category's budget, so I can adjust spending before overshooting. | Warning shown on the category view; not a blocking action; recalculated on every expense entry. |
| 5 | As a user, I want to see a simple bar chart of spending by category for the current month, so I can spot patterns at a glance. | One bar per category; updates when an expense is added; empty categories still shown at zero. |

## Level 2 · Intermediate

### [01 · Scrum Ceremonies in Depth](level-2/01-scrum-ceremonies-in-depth.md)

*The four inspect-and-adapt loops*

| Loop | Event(s) | Inspects | Frequency |
|---|---|---|---|
| Product direction | Sprint Review | The Increment, against real stakeholder needs | Every sprint |
| Sprint execution | Daily Scrum | Progress toward the Sprint Goal | Every day |
| Process health | Sprint Retrospective | How the team works together | Every sprint |
| Plan formation | Sprint Planning | What's achievable and valuable next | Every sprint |

### [02 · Sprint Retrospectives](level-2/02-sprint-retrospectives.md)

*The five-stage retrospective*

| Stage | Purpose | Typical technique |
|---|---|---|
| Set the stage | Get everyone present and safe to speak | Check-in question, restate the Prime Directive |
| Gather data | Surface facts and events from the sprint, not opinions yet | Timeline, mood chart, sprint metrics |
| Generate insights | Ask *why* patterns occurred | 5 Whys, fishbone diagram, grouping/affinity mapping |
| Decide what to do | Convert insight into 1–3 concrete actions | Dot-voting, effort/impact grid |
| Close | Confirm ownership and appreciate the team | Restate owners + due sprint, retro-on-the-retro |

### [03 · Backlog Refinement](level-2/03-backlog-refinement.md)

*What refinement actually produces*

| Refinement activity | Output | Who drives it |
|---|---|---|
| Splitting large items | Stories small enough to fit in one sprint | PO + team together |
| Adding acceptance criteria | Testable "done" conditions per story | PO, validated by team |
| Estimating | Story points or sizing for prioritization | Whole team |
| Ordering | Backlog sequence reflecting value and dependency | Product Owner |
| Removing stale items | A backlog that reflects current reality | Product Owner |

### [04 · Kanban Metrics (Cycle Time, Lead Time, CFD)](level-2/04-kanban-metrics.md)

*The core measurements*

| Metric | Definition | Answers |
|---|---|---|
| Lead time | Time from request created to delivered | "How long does a customer wait?" |
| Cycle time | Time from work started to delivered | "How long does work take once we commit to it?" |
| Throughput | Items completed per unit time | "How much do we ship?" |
| WIP | Items currently in progress | "How much is in flight right now?" |

### [05 · Definition of Done &amp; Definition of Ready](level-2/05-definition-of-done-ready.md)

*Two gates, two purposes*

| | Definition of Ready (DoR) | Definition of Done (DoD) |
|---|---|---|
| Gates | Entry into a sprint | Exit from a sprint (or a story) |
| Owned by | Product Owner, validated by team | Whole team |
| Answers | "Can we confidently start this?" | "Is this actually finished?" |
| Scope | Per story | Usually team- or increment-wide, plus per-story acceptance criteria |
| Changes how often | Rarely — it's a quality bar for backlog items | Rarely, but should grow as engineering maturity grows |

### [06 · Velocity Tracking](level-2/06-velocity-tracking.md)

*What velocity is*

| Correct use | Incorrect use |
|---|---|
| Forecasting this team's own capacity next sprint | Comparing Team A's velocity to Team B's |
| Sanity-checking Sprint Planning ("we're pulling 40 points, we usually do 28") | Setting velocity as a target to hit or exceed |
| Release forecasting: remaining points ÷ average velocity = sprints remaining | Using velocity in performance reviews |
| Spotting a real capacity change (illness, holidays, new hire ramp-up) | Comparing velocity across different estimation scales or teams |

### [07 · Release Planning](level-2/07-release-planning.md)

*Release planning inputs*

| Input | Source | Role in the plan |
|---|---|---|
| Prioritized backlog | Product Owner | Defines *what*, in order of value |
| Velocity range | Module 06 | Defines *how much* per sprint, realistically |
| Fixed constraints | Business (date, budget, compliance deadline) | Defines the boundary the plan must fit |
| Dependencies | Architecture, other teams | Defines sequencing constraints |
| Risk register | Team + stakeholders | Defines what could blow up the plan |

### [08 · Working Agreements &amp; Team Norms](level-2/08-working-agreements-team-norms.md)

*What belongs in a working agreement*

| Category | Example agreements |
|---|---|
| Communication | Core hours everyone is reachable; response-time expectation for Slack/chat |
| Meetings | Cameras on/off norm; no meetings before 10am; Daily Scrum starts on time regardless of who's missing |
| Code/work quality | PR review turnaround within 1 business day; no merging your own PR |
| Conflict | Disagreements raised directly first, escalated to the team only if unresolved after one attempt |
| Focus | No pinging people during marked "deep work" blocks; interruptions reserved for true blockers |
| Decision-making | Reversible decisions made by whoever's doing the work; irreversible ones brought to the team |

### [09 · Handling Scope Change Mid-Sprint](level-2/09-handling-scope-change.md)

*Sprint Goal as the filter, not "no changes ever"*

| Request type | Sprint Goal impact | Typical response |
|---|---|---|
| Critical production bug | Threatens the goal if unfixed (outage, data loss) | Accept; renegotiate scope to compensate |
| "Nice to have while you're in there" | No bearing on the goal | Defer to backlog, refine for next sprint |
| Stakeholder changed their mind on a planned story | May or may not affect the goal | Discuss with PO; only mid-sprint change if goal is truly at risk otherwise |
| Executive escalation, unrelated to goal | Doesn't affect the goal by definition | Push back explicitly; log for next Planning |

### [10 · Project — Release Plan with Sprint Roadmap](level-2/10-project-release-plan.md)

*Step 1: Historical velocity (Module 06)*

| Sprint | Points completed |
|---|---|
| -3 | 21 |
| -2 | 17 |
| -1 | 23 |

## Level 3 · Advanced

### [01 · Scaling Frameworks Overview (SAFe, LeSS, Nexus)](level-3/01-scaling-frameworks-overview.md)

*The core problem scaling frameworks solve*

| Problem at scale | Single-team Scrum answer | Why it breaks with N teams |
|---|---|---|
| One backlog, one PO | Product Owner refines and orders it | One person can't hold context for 10 teams' worth of detail |
| Shared Sprint cadence | Sprint Planning aligns the team | Teams drift out of sync without a shared calendar |
| Cross-team dependencies | Doesn't exist within one team | Team A blocked on Team B becomes routine |
| Architectural coherence | Whatever the team agrees | No mechanism to keep 10 teams' technical decisions compatible |

### [02 · Agile in Distributed Teams](level-3/02-agile-distributed-teams.md)

*What breaks first, and why*

| Ceremony/practice | Co-located assumption | What breaks remotely |
|---|---|---|
| Daily Scrum | Quick, informal, easy to read the room | Becomes a scheduling puzzle across time zones; harder to sense disengagement |
| Sprint Planning | Whiteboard, sticky notes, spontaneous side-conversations | Needs a shared digital board and explicit facilitation to avoid silent non-participation |
| Retrospective | Psychological safety builds from informal hallway trust | Requires deliberate anonymous-input tools to surface honest feedback |
| Pairing/collaboration | Walk over and look at someone's screen | Requires explicit screen-share norms; async by default unless scheduled |

### [03 · Hybrid Agile-Waterfall Models](level-3/03-hybrid-agile-waterfall.md)

*Why pure models rarely survive contact with reality*

| Constraint | Why it resists pure Agile | Why it resists pure Waterfall |
|---|---|---|
| Fixed hardware manufacturing lead time | Can't iteratively "release" a physical board mid-sprint | Waterfall alone ignores that the software running on it benefits from iteration |
| Government/regulatory approval gate | The gate itself is a hard, sequential milestone | Everything *except* the gate benefits from iterative delivery |
| Fixed-price client contract with a spec | Client wants a locked scope and price upfront | Delivery execution still benefits from sprints and continuous feedback |

### [04 · Risk Management Across SDLC Phases](level-3/04-risk-management-sdlc.md)

*Risk categories and where they concentrate*

| Risk category | Concentrates in | Example |
|---|---|---|
| Requirements risk | Early (discovery, backlog formation) | Misunderstood user need |
| Technical/architecture risk | Early-to-mid (design, first builds) | Chosen approach doesn't scale |
| Schedule/scope risk | Ongoing, spikes near release | Underestimated stories, scope creep |
| Integration risk | Mid-to-late | Two teams' components don't compose as assumed |
| Operational risk | Late (release, post-release) | Deployment failure, unhandled load |
| Compliance/legal risk | Can appear at any phase | A late-discovered regulatory requirement |

### [05 · DevOps &amp; CI/CD Integration with Agile](level-3/05-devops-cicd-agile.md)

*Two feedback loops, not one*

| Loop | Shortened by | Answers |
|---|---|---|
| Planning/product loop | Scrum events, sprints | "Are we building the right thing?" |
| Technical delivery loop | CI/CD pipeline, automated testing, deployment automation | "Can we actually ship what we built, safely, right now?" |

### [06 · Metrics &amp; Reporting for Stakeholders](level-3/06-metrics-reporting-stakeholders.md)

*Internal metrics vs. stakeholder questions*

| Stakeholder question | Wrong metric to lead with | Right translation |
|---|---|---|
| "Are we on track?" | Raw velocity number | Forecast range against the release plan (Level 2, Module 07) |
| "Is quality okay?" | Story point count | Defect trend, escaped-bug rate, DoD compliance |
| "Why did this slip?" | "Velocity dropped" | Named cause: scope change, dependency block, risk materializing (Module 04) |
| "What are we getting for our investment?" | Points delivered | Business outcomes tied to delivered features (adoption, revenue, retention) |

### [07 · Multi-Team Dependency Management](level-3/07-multi-team-dependency-management.md)

*Types of dependencies*

| Type | Example | Typical fix |
|---|---|---|
| Technical | Team A's feature needs an API Team B hasn't built yet | Sequence work; build a stub/mock in the meantime |
| Resource | Both teams need the one engineer who knows the legacy billing system | Cross-train, or explicitly schedule that person's time across teams |
| Knowledge | Team A doesn't know a constraint only Team B's domain expert knows | Early cross-team refinement session, not discovered mid-sprint |
| Sequencing | Feature B can't ship before feature A per business/legal reasons | Backlog ordering reflects the constraint, visible to both teams |

### [08 · Agile Contracts &amp; Vendor Management](level-3/08-agile-contracts-vendor-management.md)

*Contract models and how they fit agile*

| Model | How it works | Agile fit |
|---|---|---|
| Fixed price / fixed scope | Set price for a defined scope, agreed up front | Poor — any backlog reordering becomes a change-order negotiation |
| Time & materials (T&M) | Client pays for actual hours/effort | Good — supports iterative discovery, but gives the client little cost ceiling |
| T&M with a cap | T&M up to a not-to-exceed ceiling | Better — caps risk while keeping room to reprioritize |
| Money for nothing, change for free | Client can swap unstarted scope of equal size for new scope at no extra cost; can stop early and pay only for a partial "kill fee" | Best fit — explicitly designed for agile backlogs |
| Outcome/value-based | Payment tied to a measured business outcome, not hours or features | Strong fit in principle, hard to structure and verify in practice |

### [09 · Technical Debt in an Agile Delivery Model](level-3/09-technical-debt-agile.md)

*Types of technical debt*

| Type | Example | How it's usually incurred |
|---|---|---|
| Deliberate, tracked | "We'll hardcode this config to hit the demo deadline" | A conscious trade-off, logged for later |
| Deliberate, untracked | Same trade-off, never written down anywhere | The most dangerous kind — invisible until it bites |
| Accidental, discovered | A design that seemed fine turns out not to scale | Found through use, not foreseeable at the time |
| Bit rot | Code that was fine when written, now stale relative to newer patterns/libraries | Normal decay as the codebase and ecosystem evolve |

### [10 · Project — Scaled Program Delivery Plan](level-3/10-project-scaled-program-plan.md)

*Step 2: Distributed-team working agreement (Module 02)*

| Practice | Decision |
|---|---|
| Overlap window | 2 hours of daily overlap, used for the shared Scrum of Scrums plus any live pairing |
| Async default | Refinement and design docs written async first; sync time reserved for decisions, not information transfer |
| Documentation | Every cross-team API decision recorded in a shared doc within the overlap window, not left to chat history |

## Level 4 · Master

### [01 · Agile Transformation &amp; Change Management](level-4/01-agile-transformation-change-management.md)

*Why transformations stall*

| Failure mode | What it looks like | Root cause |
|---|---|---|
| Mandated from the top, no buy-in | Teams run standups because they're told to, not because it helps them | Change imposed, not co-designed |
| Framework-first, outcome-second | Success measured by "are we doing Scrum right" | No connection drawn to the business problem agile was meant to solve |
| Middle-management left out | Team level adopts agile; managers still run project plans and status reports the old way | The layer that controls incentives and resourcing wasn't part of the change |
| No slack for the learning curve | Teams expected to hit full velocity from sprint one | Ignores that new ways of working are genuinely slower before they're faster |

### [02 · Coaching Teams](level-4/02-coaching-teams.md)

*Coaching vs. facilitating vs. managing*

| Mode | What it does | When to use it |
|---|---|---|
| Facilitating | Guides a process to a group's own outcome, contributes no content | Running a retro, a planning session |
| Coaching | Helps someone find their own answer through questions, doesn't supply the answer | Team is capable but stuck, avoiding a hard conversation, or repeating a pattern |
| Managing/directing | Makes the call and tells people what to do | Genuine emergencies, or when the team lacks the information/authority to decide |

### [03 · Enterprise SDLC Governance](level-4/03-enterprise-sdlc-governance.md)

*Where governance and agile collide*

| Governance need | Traditional mechanism | Agile-compatible alternative |
|---|---|---|
| Change approval / audit trail | Change Advisory Board sign-off before each release | Automated, logged approvals baked into the CI/CD pipeline (who approved, what changed, when) |
| Security review | A dedicated security-gate phase before release | Security-as-code checks (SAST/DAST) run on every build; a human reviews only flagged exceptions |
| Financial controls (capitalization, budget) | Fixed project budgets tied to a fixed scope | Budgets tied to a team/product for a period (quarter), not to a project's fixed deliverable list |
| Regulatory documentation | A large document produced at the end of a phase | Documentation generated incrementally, alongside the work, from artifacts already produced (tickets, PRs, test results) |

### [04 · Choosing the Right Methodology per Project Type](level-4/04-choosing-right-methodology.md)

*The core question: how well is the work understood?*

| Work characteristic | Implication for methodology |
|---|---|
| Requirements well understood, low uncertainty, regulatory/fixed deadline | Predictive (waterfall-like) approaches can work fine — the cost of upfront planning is low relative to the risk of change |
| Requirements emerge through use, high uncertainty, fast feedback available | Iterative/agile approaches earn their overhead by cutting the cost of being wrong |
| Continuous flow of similarly-sized work, no discrete "projects" | Kanban fits better than sprint-based Scrum |
| Deep technical unknowns need investigation before any plan is credible | A time-boxed spike or discovery phase precedes methodology selection |

### [05 · Building an Internal Agile Center of Excellence](level-4/05-internal-agile-center-of-excellence.md)

*What a CoE should and shouldn't do*

| Should | Shouldn't |
|---|---|
| Curate and share practices that worked, with evidence | Mandate a single framework/process for every team regardless of context |
| Provide coaching capacity teams can pull from | Insert itself as a required approval gate on team decisions |
| Run a community of practice connecting practitioners across teams | Become the only place agile knowledge lives, creating a bottleneck |
| Track org-wide health metrics to guide where coaching capacity goes | Use those metrics to rank or punish teams |

### [06 · Measuring Transformation Success](level-4/06-measuring-transformation-success.md)

*Outcome metrics vs. compliance metrics*

| Compliance metric (avoid as a success measure) | Outcome metric (prefer) |
|---|---|
| % of teams "doing Scrum" (running the ceremonies) | Lead time from idea to production |
| Story points completed per sprint | Deployment frequency and change failure rate |
| Number of teams trained | Employee-reported engagement/psychological safety |
| Certification counts | Customer-reported satisfaction / NPS trend |

### [07 · Leading Agile at Portfolio Level](level-4/07-leading-agile-portfolio-level.md)

*Portfolio-level agile concepts*

| Team-level concept | Portfolio-level equivalent |
|---|---|
| Product backlog | Portfolio backlog of epics/investment themes |
| Sprint planning | Quarterly (or PI-based) capacity allocation across themes |
| Definition of Done | Portfolio-level exit criteria (an initiative is "done" when it hits a measurable business outcome, not just ships) |
| Retrospective | Portfolio-level inspect-and-adapt: which bets paid off, which didn't, and why |

### [08 · Agile &amp; AI-Assisted Delivery](level-4/08-agile-ai-assisted-delivery.md)

*What actually changes with AI-assisted delivery*

| Old assumption | New reality |
|---|---|
| Writing code is usually the slowest step in a story | Writing code is often now faster than review, testing, and integration |
| Story point estimates reflect roughly human-only implementation effort | Estimates need to account for AI-accelerated implementation plus unchanged review/verification effort |
| One engineer, one story, sequential | An engineer can run several AI-assisted threads in parallel, raising WIP-limit questions |
| Code review checks for correctness and style | Code review also needs to check for AI-specific failure modes: plausible-looking but subtly wrong logic, hallucinated APIs, license/provenance issues |

### [09 · Career Growth: Scrum Master to Agile Coach/Director](level-4/09-career-growth-scrum-master-to-coach.md)

*The career ladder and what changes at each level*

| Level | Unit of impact | Core skill that matters most |
|---|---|---|
| Scrum Master | One team's process health | Facilitation, servant leadership, removing team-level impediments |
| Senior Scrum Master / multi-team | Two to three teams, cross-team dependencies | Coordination, Scrum-of-Scrums facilitation, stakeholder communication |
| Agile Coach | A program or business unit | Coaching (not directing), organizational-change literacy, influence without authority |
| Director of Agile / Head of Transformation | The whole organization's operating model | Strategic change management, portfolio-level thinking, executive stakeholder management |

### [10 · Capstone — Full Organizational Agile Transformation Roadmap](level-4/10-capstone-organizational-transformation-roadmap.md)

*Step 8: Measurement plan (Level 4, Module 06)*

| Dimension | Metric | Baseline source |
|---|---|---|
| Speed | Lead time for changes | Pulled retroactively from existing ticket timestamps |
| Stability | Change failure rate | Newly instrumented from the deploy pipeline starting month 1 |
| People | Quarterly engagement/psychological-safety survey | New survey, first run in month 1 as the baseline |
| Business | Time-to-market on the next 3 major initiatives | Compared against the last 3 completed initiatives under the old model |

---

Go deeper with the full [Agile & Software Delivery Mastery Path](index.md) curriculum or test yourself with the [interview questions](interview-questions.md).
