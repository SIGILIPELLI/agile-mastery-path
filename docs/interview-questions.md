---
title: "Agile & Software Delivery Interview Questions and Answers (180 Questions)"
description: "180 Agile & Software Delivery interview questions with answers and explanations, from beginner to advanced, organised by level. Free, from the Agile & Software Delivery Mastery Path."
---

# Agile & Software Delivery Interview Questions and Answers

**180 questions** with the correct answer and a short explanation, organised from beginner (Level 1) to advanced (Level 4). Every question comes from a lesson in the free Agile & Software Delivery Mastery Path, so you can open the lesson to go deeper.

!!! tip "Practise, don't just read"
    Each lesson also ends with an interactive quiz, and the [final quiz](quiz.md) tests all four levels. Try to answer each question below before reading the answer.

## Level 1 · Entry

### [01 · What Is the SDLC?](level-1/01-what-is-sdlc.md)

**Q1.** What are the six SDLC phases?

**Answer:** Requirements, design, implementation, testing, deployment, maintenance

Every methodology arranges and repeats the same phases.

**Q2.** How do Waterfall and Agile differ regarding the phases?

**Answer:** Not which phases exist, but how often you cycle through them and in what order

Waterfall runs them once; Agile runs a compressed version repeatedly per sprint.

**Q3.** What is the typical output of the Requirements phase?

**Answer:** Requirements document, user stories, acceptance criteria

Design produces architecture diagrams and data models.

**Q4.** What does the Maintenance phase involve?

**Answer:** Bug fixes, patches, feature updates and monitoring

It continues after deployment.

### [02 · The Waterfall Model](level-1/02-waterfall-model.md)

**Q5.** What is Waterfall?

**Answer:** The SDLC run once, in strict sequence, with a formal sign-off gate between phases

Winston Royce described it in 1970 as a risky approach to warn against.

**Q6.** Why is it costly when Testing reveals a wrong requirement?

**Answer:** Each gate is expensive to reopen: a formal change request, re-approval and rework of downstream artifacts

That's the defining trait of Waterfall.

**Q7.** When does Waterfall genuinely fit?

**Answer:** Stable requirements, fixed-price contracts, safety-critical or heavily audited work

Up-front certainty is rewarded.

**Q8.** Who typically signs off Testing → Deployment?

**Answer:** QA lead / client acceptance

All defined test cases pass with no open critical defects.

### [03 · The Agile Manifesto &amp; Principles](level-1/03-agile-manifesto-principles.md)

**Q9.** Where and when was the Agile Manifesto written?

**Answer:** February 2001, Snowbird, Utah, by seventeen practitioners

They were frustrated with heavyweight documentation-driven processes.

**Q10.** What is the key caveat in the Manifesto?

**Answer:** While there is value in the items on the right, we value the items on the left more

Agile doesn't mean no process, no documentation, no contracts or no planning.

**Q11.** What does 'working software over comprehensive documentation' mean?

**Answer:** Documentation is still valued, but working software outranks it

It's a common misreading to say Agile means no documentation.

**Q12.** How many principles back the four values?

**Answer:** Twelve

For example deliver working software frequently, in weeks rather than months.

### [04 · Scrum Roles, Events &amp; Artifacts](level-1/04-scrum-roles-events-artifacts.md)

**Q13.** What are Scrum's parts?

**Answer:** Three accountabilities, five events and three artifacts

Product Owner, Scrum Master, Developers.

**Q14.** Is the Daily Scrum a status report to the Scrum Master?

**Answer:** No: it's Developers inspecting progress toward the Sprint Goal and re-planning the next 24 hours (15 minutes)

Running it as a status meeting is a role failure.

**Q15.** What is the real output of the Sprint Review?

**Answer:** An updated Product Backlog, from stakeholder feedback on the Increment

It's not a demo for its own sake.

**Q16.** What is a common Product Owner failure?

**Answer:** Acting as a project manager in disguise, assigning tasks and dictating how work happens

That collapses self-organisation and turns Scrum into Waterfall with a two-week clock.

### [05 · Kanban Basics (WIP Limits &amp; Pull System)](level-1/05-kanban-basics.md)

**Q17.** Kanban is flow-based. What does that mean versus Scrum?

**Answer:** No sprints or timeboxes; work flows continuously across a visual board regulated by WIP limits

The original method has no dedicated Product Owner.

**Q18.** Development is full (4/4). A developer finishes early. What should they do?

**Answer:** Help unblock items stuck downstream (e.g. Review), not pull a new item

Pull means work enters a stage only when there is capacity downstream.

**Q19.** Why are WIP limits the whole point?

**Answer:** They fight the instinct to start work, since a pile of half-finished work is worse than an idle hour

Teams should be measured on what's finished, not started.

**Q20.** One column is perpetually full. What does it reveal?

**Answer:** That stage is the bottleneck; add capacity there

Lots of items in progress but few finished means too much WIP.

### [06 · Agile vs. Waterfall](level-1/06-agile-vs-waterfall.md)

**Q21.** What is the decision test between Agile and Waterfall?

**Answer:** Which of scope, schedule or cost is truly fixed; the other two must flex

Fixed scope fits Waterfall; fixed schedule or cost fits Agile.

**Q22.** A trade-show launch date is fixed. What flexes?

**Answer:** Scope: ship the highest-value subset

That fits Agile.

**Q23.** When is risk discovered in each model?

**Answer:** Waterfall: late (often in Testing); Agile: early and often, every sprint

Agile surfaces new information each sprint.

**Q24.** What contract type best fits each?

**Answer:** Waterfall: fixed-price, fixed-scope; Agile: time-and-materials or scope-flexible fixed-budget

A request to 'be more agile' that fixes all three variables is incoherent.

### [07 · User Stories &amp; Backlogs](level-1/07-user-stories-backlogs.md)

**Q25.** What is the standard user story format?

**Answer:** As a [role], I want [capability], so that [benefit]

The 'so that' clause anchors developer judgment calls.

**Q26.** What are acceptance criteria?

**Answer:** Specific, testable conditions that must hold for the story to be complete

For example a customer with no saved address sees an empty form.

**Q27.** What goes wrong without the 'so that' benefit?

**Answer:** A developer can't make good judgment calls about edge cases

For example whether to let users edit a prefilled address.

**Q28.** What is a backlog?

**Answer:** The ordered collection of stories and work items a team might build

Vague or oversized stories are where most sprint failures start.

### [08 · Estimation Basics (Story Points &amp; Planning Poker)](level-1/08-estimation-basics.md)

**Q29.** Why are story points relative?

**Answer:** Humans are bad at absolute durations but good at comparing sizes

Compare to something already built.

**Q30.** What does a story point encode?

**Answer:** Complexity, effort and uncertainty/risk

A small high-uncertainty task can get more points than a bigger familiar one.

**Q31.** Why does the Fibonacci scale widen its gaps?

**Answer:** Precision on big items is false; choosing between 14 and 15 is meaningless

Anything 20+ should usually be split.

**Q32.** What technique estimates collaboratively?

**Answer:** Planning Poker

Everyone reveals estimates together.

### [09 · A Simple Sprint-Planning Exercise](level-1/09-sprint-planning-exercise.md)

**Q33.** What does Sprint Planning produce?

**Answer:** A Sprint Goal (one sentence) and a Sprint Backlog sized to capacity

Inputs: ordered Product Backlog, capacity and historical velocity.

**Q34.** In the example, Dev B has 8 days and focus factor 0.8. What is the effective capacity?

**Answer:** 6.4 days

8 × 0.8 = 6.4; the team total was 29.4 person-days.

**Q35.** Last three sprints delivered 21, 25 and 23 points. What is the planning guidance?

**Answer:** Plan about 23 points (average velocity), not more just because the backlog has more

Velocity is a sanity check against over-commitment.

**Q36.** From which end of the backlog are stories pulled?

**Answer:** The top, since it's ordered by priority

Running totals stop when the planned points are reached.

### [10 · Capstone — Run a Mock 1-Week Sprint Plan](level-1/10-capstone-mock-sprint-plan.md)

**Q37.** Why does the capstone use a 1-week sprint?

**Answer:** To keep it finishable in one sitting while exercising every step

The common length is two weeks.

**Q38.** What must exist before any sprint?

**Answer:** A Product Goal and an ordered Product Backlog

Their goal: track spending against a monthly budget without a spreadsheet.

**Q39.** The team's first sprint has no velocity. What do they plan against?

**Answer:** Capacity

Velocity builds after sprints run.

**Q40.** How are stories estimated?

**Answer:** Planning Poker on the Fibonacci scale, with discussion to a final value

Differences between estimators are discussed.

## Level 2 · Intermediate

### [01 · Scrum Ceremonies in Depth](level-2/01-scrum-ceremonies-in-depth.md)

**Q41.** Which event checks whether you built the right thing?

**Answer:** Sprint Review (outer loop)

The Daily Scrum checks you're on track for the plan.

**Q42.** What risk arises from running tight standups but skipping a genuine Review?

**Answer:** Being efficient at building the wrong thing

Review feeds the backlog with stakeholder feedback.

**Q43.** What is the highest-leverage Daily Scrum fix?

**Answer:** Reframe from 'what did I do' to 'what's in the way of the Sprint Goal'

Only the team can act on blockers, so it becomes self-organising.

**Q44.** What is a healthy retrospective outcome?

**Answer:** Concrete, owned action items (cap at 1–3)

Venting without follow-through is the failure mode.

### [02 · Sprint Retrospectives](level-2/02-sprint-retrospectives.md)

**Q45.** What are the five retrospective stages?

**Answer:** Set the stage, gather data, generate insights, decide what to do, close

Skipping straight to deciding produces actions aimed at symptoms.

**Q46.** What is the Prime Directive?

**Answer:** Everyone did the best job they could, given what they knew, their skills, resources and the situation (Norm Kerth)

It reframes retros from blame to system improvement.

**Q47.** Which techniques generate insights?

**Answer:** 5 Whys, fishbone diagram and affinity mapping

Dot-voting and effort/impact grids help decide.

**Q48.** How many actions should a retro leave?

**Answer:** 1–3 concrete actions with owners and a due sprint

Fewer actions get done.

### [03 · Backlog Refinement](level-2/03-backlog-refinement.md)

**Q49.** What is refinement?

**Answer:** The ongoing habit of taking items from idea to ready-to-pull, ideally no more than 10% of team capacity

It was formerly called grooming.

**Q50.** What does INVEST stand for?

**Answer:** Independent, Negotiable, Valuable, Estimable, Small, Testable

Used as a readiness gate for stories.

**Q51.** Which are story-splitting axes?

**Answer:** Workflow steps, business rules, data boundaries, CRUD operations, happy path versus edge cases

For example Checkout into browse cart, coupon, pay, confirm.

**Q52.** Who orders the backlog?

**Answer:** The Product Owner

Estimating involves the whole team.

### [04 · Kanban Metrics (Cycle Time, Lead Time, CFD)](level-2/04-kanban-metrics.md)

**Q53.** What is the difference between lead time and cycle time?

**Answer:** Lead time: request created to delivered; cycle time: work started to delivered

Lead time is the customer's wait.

**Q54.** What does Little's Law say?

**Answer:** Average cycle time = average WIP ÷ average throughput, so lowering WIP lowers cycle time

That's the maths behind WIP limits.

**Q55.** A CFD's 'In Progress' band widens steadily. What does it mean?

**Answer:** Growing WIP: a bottleneck forming, work starting faster than finishing

Parallel bands mean stable flow.

**Q56.** Why use percentiles instead of the average cycle time?

**Answer:** Cycle time has a long right tail; 85th percentile is a reasonable forecast and 95th suits external commitments

The average hides outliers.

### [05 · Definition of Done &amp; Definition of Ready](level-2/05-definition-of-done-ready.md)

**Q57.** What do DoR and DoD gate?

**Answer:** DoR gates entry into a sprint; DoD gates the exit (when something is finished)

DoR is per story; DoD is usually team-wide.

**Q58.** What happens with a strong DoD but no DoR?

**Answer:** The team pulls in vague stories and discovers mid-sprint what 'done' means for each

The reverse gives inconsistent quality.

**Q59.** Why is DoD layered?

**Answer:** Some criteria apply to every story (review, tests), others once per sprint or release (regression suite); mixing makes it too heavy

Keep per-story checks light.

**Q60.** In the volatile-velocity example, what was wrong?

**Answer:** The DoD only said 'code merged', so stories shipped without tests, inflating velocity while accumulating defects

Strengthening the DoD stabilises velocity.

### [06 · Velocity Tracking](level-2/06-velocity-tracking.md)

**Q61.** What is velocity for?

**Answer:** Forecasting how much a specific team can complete in a future sprint, from its own recent history

Story points completed per sprint, averaged over recent sprints.

**Q62.** Why is cross-team velocity comparison meaningless?

**Answer:** Story points are relative and team-specific, so they're different units; comparisons push teams to inflate estimates

That causes velocity inflation.

**Q63.** Backlog 140 points, average velocity 19.8. About how many sprints?

**Answer:** About 7 (best ~6, worst ~9 using the range)

Present a range, not a single number.

**Q64.** What counts toward velocity?

**Answer:** Only points for stories fully meeting the Definition of Done

Partial-credit counting inflates velocity.

### [07 · Release Planning](level-2/07-release-planning.md)

**Q65.** Date-driven versus scope-driven release plans?

**Answer:** Date-driven fixes the date and varies scope; scope-driven fixes the feature set (MVP) and varies the date

Most real releases are a hybrid.

**Q66.** What if the forecast doesn't clear the fixed date?

**Answer:** Cut scope, never compress the Definition of Done

Quality is not the lever.

**Q67.** How often should a release plan be re-forecast?

**Answer:** Every sprint, with updated velocity and remaining backlog

It's a living forecast, not a one-time Gantt chart.

**Q68.** 95 must-have points, velocity 19 (range 15–24), 5 sprints available. What's the verdict?

**Answer:** Tight, not safe: the average fits but the worst case reads closer to 7 sprints

Raise it in release planning and consider cutting scope.

### [08 · Working Agreements &amp; Team Norms](level-2/08-working-agreements-team-norms.md)

**Q69.** Who should write a working agreement?

**Answer:** The team itself, as a short team-owned document

A rule imposed is compliance; a rule the team wrote is a commitment.

**Q70.** Where should norms be drafted?

**Answer:** In a retrospective, where they emerge from fresh friction

Keep it short (5–10 items) and visible.

**Q71.** How should violations be treated?

**Answer:** As a retro topic, since the norm itself may be wrong

Handle peer-to-peer.

**Q72.** When should agreements be reviewed?

**Answer:** Every few sprints and when a new member joins

A new hire should read it on day one.

### [09 · Handling Scope Change Mid-Sprint](level-2/09-handling-scope-change.md)

**Q73.** What does Scrum protect when change arrives mid-sprint?

**Answer:** The Sprint Goal, not the exact ticket list

The question is whether accepting it still lets us meet the goal.

**Q74.** A critical production bug (outage) lands mid-sprint. Response?

**Answer:** Accept it and renegotiate scope to protect the goal

It threatens the goal if unfixed.

**Q75.** A 'nice to have while you're in there' request?

**Answer:** Defer to the backlog and refine for the next sprint

No bearing on the Sprint Goal.

**Q76.** Is the right question 'can the team fit it'?

**Answer:** No: ask whether accepting it still lets the team meet the Sprint Goal

That's the decision framework.

### [10 · Project — Release Plan with Sprint Roadmap](level-2/10-project-release-plan.md)

**Q77.** Last three sprints: 21, 17, 23 points. What are the average and range?

**Answer:** About 20.3; range 17–23

(21+17+23)/3 ≈ 20.3.

**Q78.** Two items failed 'Testable'. What happened?

**Answer:** They were sent back to the PO for acceptance criteria before entering the plan

The DoR gate protects the plan.

**Q79.** Must-have is 26 points, forecasting about 1.3 sprints. Why a 10-week window?

**Answer:** The release also needs DoD hardening, deployment and buffer, which story points don't cover

A hardening allowance is added instead of inflating estimates.

**Q80.** What do sprints 4 and 5 hold?

**Answer:** Hardening (regression, security, load) with no new stories, and a reserved buffer/bug-fix sprint

Buffer is held in reserve, not pre-committed.

## Level 3 · Advanced

### [01 · Scaling Frameworks Overview (SAFe, LeSS, Nexus)](level-3/01-scaling-frameworks-overview.md)

**Q81.** Why do scaling frameworks exist?

**Answer:** One Scrum team tops out around 5–9 people; many teams need coordinated backlogs, dependencies and releases

One PO can't hold context for 10 teams.

**Q82.** How do SAFe, LeSS and Nexus compare?

**Answer:** SAFe: prescriptive, highest overhead; LeSS: minimal, more Scrum not Scrum-plus; Nexus: lightweight with an integration team

Nexus is Scrum.org's extension.

**Q83.** What trade-off underlies every scaling framework?

**Answer:** Team autonomy versus organisation-level coordination

LeSS demands more discipline and technical maturity.

**Q84.** What problem arises that single-team Scrum doesn't have?

**Answer:** Cross-team dependencies, where Team A is blocked on Team B

Also architectural coherence and shared cadence.

### [02 · Agile in Distributed Teams](level-3/02-agile-distributed-teams.md)

**Q85.** What's the scarcest resource on a distributed team?

**Answer:** Synchronous time: reserve it for what truly needs real-time discussion

Push status and FYI updates to async.

**Q86.** Name the three time-zone strategies.

**Answer:** Follow-the-sun, overlap window, async-first

Each has trade-offs, e.g. follow-the-sun needs excellent handoff documentation.

**Q87.** How can a Daily Scrum be async-friendly?

**Answer:** Post 'what's blocking the Sprint Goal' in a channel; hold a short rotating live window only for items needing discussion; Scrum Master follows up

It avoids forcing someone to attend at 6am or 10pm.

**Q88.** What does a remote retro need?

**Answer:** Deliberate mechanisms like anonymous input, since hallway trust is missing

Psychological safety must be built deliberately.

### [03 · Hybrid Agile-Waterfall Models](level-3/03-hybrid-agile-waterfall.md)

**Q89.** What is the Water-Scrum-Fall pattern?

**Answer:** Waterfall at the edges (requirements/contracting, release/compliance) with Agile sprints in the middle

The middle holds the most uncertainty and feedback value.

**Q90.** Why do pure models rarely survive?

**Answer:** Fixed hardware lead times, regulatory gates and fixed-price contracts force some sequencing

Design hybrids deliberately, not by accident.

**Q91.** Why is requirements and contracting Waterfall-like?

**Answer:** Client and legal need a defined scope and price before committing

Build and design stay Agile.

**Q92.** A regulatory approval gate is...

**Answer:** A hard sequential milestone that sits around the Agile core

Release and compliance sign-off are inherently sequential.

### [04 · Risk Management Across SDLC Phases](level-3/04-risk-management-sdlc.md)

**Q93.** Which column makes a risk register useful day to day?

**Answer:** Trigger/signal: a specific observable that means the risk is happening

It converts 'watch out for X' into a checkable condition.

**Q94.** Who should own a risk?

**Answer:** A person, not a team

Fields: description, likelihood, impact, trigger, mitigation, owner.

**Q95.** Where do requirements risk and operational risk concentrate?

**Answer:** Requirements early (discovery); operational late (release and post-release)

Compliance risk can appear at any phase.

**Q96.** What do short sprints not do automatically?

**Answer:** Surface risks nobody has thought about; risk work still needs to be deliberate

Tag risky backlog items during refinement and resequence them earlier.

### [05 · DevOps &amp; CI/CD Integration with Agile](level-3/05-devops-cicd-agile.md)

**Q97.** What are the two feedback loops?

**Answer:** Planning/product loop (Scrum, weeks) and technical delivery loop (CI/CD, minutes)

Perfect sprints can still ship only quarterly without CI/CD.

**Q98.** How is CI/CD related to the Definition of Done?

**Answer:** It automates it: review gates, automated tests, scans, CI-green merges and deployable builds

It removes the manual toil that makes 'done' mean 'pending a manual release'.

**Q99.** What do feature flags enable?

**Answer:** Shipping code dark and turning it on independently of deploy, decoupling deploy from release

Trunk-based development and canary/blue-green deploys also keep releases low-risk.

**Q100.** Why isn't a pipeline alone DevOps?

**Answer:** Separate Dev and Ops teams with ticket-based handoffs recreate the old silo; culture matters

DevOps is culture, not just tooling.

### [06 · Metrics &amp; Reporting for Stakeholders](level-3/06-metrics-reporting-stakeholders.md)

**Q101.** A stakeholder asks 'Are we on track?'. What should you lead with?

**Answer:** A forecast range against the release plan, not raw velocity

Raw velocity invites comparison and blame.

**Q102.** Which row of the stakeholder report is most often omitted but most valuable?

**Answer:** The Ask: a decision, budget or feedback needed

A report that never asks trains stakeholders to skim.

**Q103.** For 'Is quality okay?' which metrics?

**Answer:** Defect trend, escaped-bug rate and DoD compliance

Points don't measure quality.

**Q104.** Which artifacts should you show stakeholders?

**Answer:** Release forecast range and business-outcome dashboards; burndown rarely as-is; CFD only to technical stakeholders

Choose what answers their questions.

### [07 · Multi-Team Dependency Management](level-3/07-multi-team-dependency-management.md)

**Q105.** What are the four dependency types?

**Answer:** Technical, resource, knowledge and sequencing

Each has a typical fix.

**Q106.** Why make dependencies visible at refinement/planning time?

**Answer:** A dependency discovered in the sprint it blocks has already cost the sprint

Use tags, shared roadmaps, or joint planning.

**Q107.** What is a Scrum of Scrums?

**Answer:** A short regular sync among representatives of dependent teams, focused on dependencies, not status

It's not a status meeting.

**Q108.** How can a technical dependency be eased?

**Answer:** Sequence work and build a stub or mock of the other team's API

Resource dependencies are fixed by cross-training.

### [08 · Agile Contracts &amp; Vendor Management](level-3/08-agile-contracts-vendor-management.md)

**Q109.** Which contract model fits agile poorly?

**Answer:** Fixed price / fixed scope, since any backlog reordering becomes a change request

T&amp;M supports iterative discovery; a cap bounds the risk.

**Q110.** How can a fixed-price deal be agile-friendly?

**Answer:** Fix budget, cadence and Definition of Done, but keep the backlog content and order flexible

The vendor then delivers the highest-value items first.

**Q111.** What does 'money for nothing' let the client do?

**Answer:** End early, paying only for delivered scope plus a small fee

The incentive shifts from defending scope to delivering value.

**Q112.** Why agree the Definition of Done before the contract starts?

**Answer:** It removes 'done' as a dispute at invoice time

Also have the vendor attend sprint reviews and sample QA each sprint.

### [09 · Technical Debt in an Agile Delivery Model](level-3/09-technical-debt-agile.md)

**Q113.** Which debt type is the most dangerous?

**Answer:** Deliberate and untracked: a conscious choice nobody else knows about

It's invisible to everyone after the moment it was made.

**Q114.** How should you prioritise paydown?

**Answer:** By how often the interest is paid (code changed often, causing incidents, bus-factor risk), not by how ugly it is

Debt in code touched once a year is low priority.

**Q115.** What is dedicated capacity for debt?

**Answer:** A protected fixed share of each sprint, commonly 10–20%

It keeps paying down without stopping feature work.

**Q116.** What is the Boy Scout rule?

**Answer:** Small opportunistic cleanup bundled into stories touching the affected code

Combine with a tech-debt tag and interest framing for stakeholders.

### [10 · Project — Scaled Program Delivery Plan](level-3/10-project-scaled-program-plan.md)

**Q117.** Why choose a Scrum-of-Scrums over full SAFe for three teams?

**Answer:** Three teams are below the threshold where SAFe's overhead pays off, yet informal coordination wouldn't catch dependencies

It's a deliberate framework choice.

**Q118.** How is the shared Platform API delivered?

**Answer:** Kanban-style with a class-of-service lane for 'blocking another team'

It jumps Platform's own priorities.

**Q119.** How does the plan handle a fixed launch date without a code freeze?

**Answer:** Feature-flag every launch item and toggle off what isn't ready

CI/CD ships behind flags to shared staging.

**Q120.** How is the overseas client time-zone gap handled?

**Answer:** A recorded walkthrough for client review, plus a 2-hour daily overlap window for live work

Async by default; sync for decisions.

## Level 4 · Master

### [01 · Agile Transformation &amp; Change Management](level-4/01-agile-transformation-change-management.md)

**Q121.** What is 'agile theater'?

**Answer:** Ceremonies exist but the mindset doesn't

It happens when transformation ignores how people experience change.

**Q122.** Which are common reasons transformations stall?

**Answer:** Mandated with no buy-in, framework-first, middle management left out, no slack for the learning curve

Kotter's model maps onto the rollout.

**Q123.** What does Kotter's 'Generate short-term wins' mean for agile?

**Answer:** Pick 1–2 pilot teams likely to succeed and publicise results early

Then consolidate gains and adjust rather than copy-paste.

**Q124.** What does 'Anchor in culture' involve?

**Answer:** Updating hiring, promotion and performance criteria to reward the new behaviours

Otherwise old incentives win.

### [02 · Coaching Teams](level-4/02-coaching-teams.md)

**Q125.** How do facilitating, coaching and managing differ?

**Answer:** Facilitating guides process with no content; coaching helps people find their own answer through questions; managing makes the call

Conflating them is the most common new-coach mistake.

**Q126.** What does a coach who always directs produce?

**Answer:** Compliant teams that never build their own judgment

One who never directs leaves teams flailing in a real crisis.

**Q127.** What does GROW stand for?

**Answer:** Goal, Reality, Options, Will

Will asks what they'll commit to, and by when.

**Q128.** A Scrum Master quietly cuts scope mid-sprint to hide under-delivery. What should the coach do?

**Answer:** Use coaching questions to surface the issue and the team's own insight, rather than just directing

The pattern has run for four sprints and hides real information.

### [03 · Enterprise SDLC Governance](level-4/03-enterprise-sdlc-governance.md)

**Q129.** What is the master-level governance skill?

**Answer:** Satisfying audit, compliance and security obligations without recreating stage-gated waterfall around every sprint

Governance obligations don't vanish with agile.

**Q130.** What agile-compatible alternative replaces a security-gate phase?

**Answer:** Security-as-code checks (SAST/DAST) run in the pipeline continuously

Likewise automated logged approvals instead of per-release CAB sign-off.

**Q131.** What is the design principle for governance layers?

**Answer:** Push decisions down to the lowest layer that can make them safely, and automate mechanical checks

Layers: team, program/product, portfolio, enterprise/compliance.

**Q132.** A single CAB meeting gates every team's every release. What is it?

**Answer:** An anti-pattern: a historical control point never re-examined after agile adoption

Fix with risk-based, automated approvals.

### [04 · Choosing the Right Methodology per Project Type](level-4/04-choosing-right-methodology.md)

**Q133.** What is the core question for choosing a methodology?

**Answer:** How well is the work understood?

Well understood, fixed deadline leans predictive; emerging requirements lean iterative.

**Q134.** When does Kanban fit better than Scrum?

**Answer:** A continuous flow of similarly sized work, no discrete projects (e.g. support ticket flow)

Scrum on support work creates artificial sprint boundaries.

**Q135.** What helps when deep technical unknowns exist?

**Answer:** A time-boxed spike or discovery phase before any plan is credible

Then pick the delivery approach.

**Q136.** What's the symptom of applying agile to fixed regulatory filing work?

**Answer:** Ceremonies feel like theatre; iteration adds no value

Waterfall on exploratory work makes the big spec wrong.

### [05 · Building an Internal Agile Center of Excellence](level-4/05-internal-agile-center-of-excellence.md)

**Q137.** Should a CoE mandate one framework or act as an approval gate?

**Answer:** No: it should curate practices, provide pull-based coaching and run a community of practice

It must enable, not control.

**Q138.** How should health metrics be used?

**Answer:** To direct coaching capacity, never to rank or punish teams

For example psychological safety and cycle time trends.

**Q139.** How does CoE shape vary with size?

**Answer:** Under ~100 engineers 1–2 part-time coaches; 100–500 a small team of 3–5; 500+ federated with embedded coaches

A CoE growing faster than the organisation drifts toward control.

**Q140.** In the worked example, what went wrong?

**Answer:** Coaches embedded permanently and became a required approval step for process change

That makes the CoE a control layer.

### [06 · Measuring Transformation Success](level-4/06-measuring-transformation-success.md)

**Q141.** Why is 'Are we agile yet?' the wrong question?

**Answer:** It invites checklist theatre instead of measuring business outcomes

Prefer outcome metrics to compliance metrics.

**Q142.** Which is an outcome metric?

**Answer:** Lead time from idea to production, deployment frequency and change failure rate

Compliance metrics are easy to game.

**Q143.** Why track a balanced set across speed, stability, people and business?

**Answer:** Optimising only speed can hide quality and sustainability costs

DORA-adjacent measures plus engagement and customer satisfaction.

**Q144.** What does MTTR measure?

**Answer:** Mean time to restore service after a failure (stability)

It sits with change failure rate.

### [07 · Leading Agile at Portfolio Level](level-4/07-leading-agile-portfolio-level.md)

**Q145.** What is the portfolio-level equivalent of sprint planning?

**Answer:** Quarterly (or PI-based) capacity allocation across investment themes

The backlog becomes investment themes.

**Q146.** What is the WSJF score?

**Answer:** (value + time criticality + risk reduction/opportunity) ÷ job size

It favours high-value, low-effort work and penalises large slow bets.

**Q147.** Why rank by WSJF rather than political capital?

**Answer:** It prioritises by economics, not by who pushes hardest

Time criticality captures value that decays when delayed.

**Q148.** What must portfolio governance not control?

**Answer:** How a funded team runs its sprints or its technical implementation

Govern investment, not internals.

### [08 · Agile &amp; AI-Assisted Delivery](level-4/08-agile-ai-assisted-delivery.md)

**Q149.** What shifts with AI-assisted delivery?

**Answer:** Writing code is often faster than review, testing and integration, so the bottleneck moves

Human review effort becomes the real constraint.

**Q150.** How might WIP limits change?

**Answer:** May need lowering, since faster implementation can pile unreviewed work into the pipeline

Otherwise the bottleneck moves unnoticed.

**Q151.** What belongs in the Definition of Done for AI-assisted work?

**Answer:** AI-specific checks such as no hallucinated dependencies and no unreviewed generated code

Code review must check AI-specific failure modes.

**Q152.** How should AI-drafted release notes be treated?

**Answer:** Needs a human accuracy pass before anything ships

Don't let AI replace the team's own reflection in retros either.

### [09 · Career Growth: Scrum Master to Agile Coach/Director](level-4/09-career-growth-scrum-master-to-coach.md)

**Q153.** What changes at each level of the ladder?

**Answer:** The unit of impact and the skill that matters most, not just scope

Scope increase alone is why promoted SMs struggle.

**Q154.** What do Agile Coach candidates often underestimate?

**Answer:** Letting go of fixing it yourself: coaching tolerates a team's slower self-discovery

Directors must speak business and financial terms.

**Q155.** Which skill helps either path credibly?

**Answer:** Data literacy: using outcome metrics to make a credible case

Anecdotes alone aren't enough.

**Q156.** Which evidence best supports promotion?

**Answer:** A documented before/after with metrics, a practice that spread beyond your team, and an honest failure with lessons

Certifications are table stakes externally.

### [10 · Capstone — Full Organizational Agile Transformation Roadmap](level-4/10-capstone-organizational-transformation-roadmap.md)

**Q157.** What constraint shapes the capstone roadmap?

**Answer:** An 18-month plan for 400 engineers with no budget increase

The CoE is staffed from internal Scrum Masters.

**Q158.** What rollout pattern does it use?

**Answer:** Pilot-then-scale: 2 teams in months 1–3, the whole organisation by month 12, not a big-bang mandate

A change coalition includes respected engineers and skeptical managers.

**Q159.** How are cross-team dependencies handled?

**Answer:** A lightweight Scrum-of-Scrums, with a class-of-service lane in the platform backlog for blockers

From Level 3 modules 1 and 7.

**Q160.** What supports the coaches?

**Answer:** A monthly community of practice open to all 400 engineers

The CoE is 3 pooled coaches.

## Mixed questions across all levels

**Q161.** Your project's launch date is fixed by a trade show, and scope is negotiable. Which approach fits, and what flexes?

**Answer:** Agile: ship the highest-value subset; scope flexes

Whichever of scope, schedule or cost is truly fixed determines the fit.

**Q162.** A regulator requires a fixed spec, and changes after fabrication are very costly. Which approach fits best?

**Answer:** Waterfall-like (predictive) with sign-off gates

Stable requirements, safety-critical and audit-heavy work reward up-front certainty.

**Q163.** The Scrum Master runs the Daily Scrum as a round-robin status report to them. What is the failure and the fix?

**Answer:** It should be the Developers re-planning the next 24 hours; reframe to 'what's in the way of the Sprint Goal'

Only the team can act on blockers.

**Q164.** Stakeholders never attend the Sprint Review and the backlog is never updated afterward. What is lost?

**Answer:** The outer feedback loop: the team may efficiently build the wrong thing

The Review's output is an updated Product Backlog from stakeholder feedback.

**Q165.** Dev A: 10 days, Dev B: 8 days, Dev C: 10 days at focus factor 0.8; QA: 10 days at 0.7. What is the team's effective capacity?

**Answer:** 29.4 person-days

8 + 6.4 + 8 + 7 = 29.4 (verified by computing).

**Q166.** Backlog 140 points; the last six sprints delivered 18, 22, 15, 24, 19 and 21. About how many sprints, and how should you present it?

**Answer:** About 7 (140 ÷ 19.8 ≈ 7.06), as a range (about 6 to 9) not a single date

Velocity varies; a range avoids the 'you said 7 sprints' trap. Verified by computing.

**Q167.** Team B's velocity is 30 and Team A's is 20, and a manager wants Team A to 'match B'. What is wrong?

**Answer:** Story points are relative and team-specific, so cross-team comparison is meaningless and invites inflation

Velocity is for forecasting a team's own capacity.

**Q168.** A team has a WIP limit of 4 in Development, all 4 slots full, and one developer finishes early. What is the best move?

**Answer:** Help unblock work stuck downstream (e.g. Review) instead of pulling a new item

Pull systems start new work only when downstream capacity exists.

**Q169.** A CFD shows 'In Progress' widening while 'Done' flattens for three weeks. What does it indicate?

**Answer:** WIP is growing and throughput is dropping: a bottleneck is forming

Parallel bands signal stable flow.

**Q170.** Average cycle time is 10 days with 20 items in progress. What throughput does Little's Law imply?

**Answer:** 2 items per day (WIP ÷ cycle time)

Average cycle time = WIP ÷ throughput, so throughput = 20 ÷ 10 = 2.

**Q171.** A story reads 'Improve search' and is 'too big to estimate'. What should refinement do?

**Answer:** Split it (e.g. by workflow step, business rule or happy path versus edge cases) into independent, testable stories

Large epics are the most common refinement blocker.

**Q172.** Mid-sprint, someone asks to 'squeeze in' a nice-to-have unrelated to the Sprint Goal. What do you do?

**Answer:** Defer it to the backlog for refinement and the next sprint

The filter is whether it threatens the Sprint Goal.

**Q173.** A critical production outage lands mid-sprint. What is right?

**Answer:** Accept it and renegotiate sprint scope to protect the Sprint Goal

Critical bugs threaten the goal if unfixed.

**Q174.** Four initiatives compete: A has value 8, time criticality 3, risk reduction 5, size 2; B has 13, 8, 3, size 13; C has 5, 13, 2, size 3. Which has the highest WSJF, and what is it?

**Answer:** A, with (8+3+5) ÷ 2 = 8.0 (B ≈ 1.8, C ≈ 6.7)

WSJF = (value + time criticality + risk reduction) ÷ job size. Verified by computing.

**Q175.** Which contract structure supports agile best?

**Answer:** A fixed budget and cadence with a flexible backlog, plus 'money for nothing, change for free'

The vendor's incentive shifts from defending scope to delivering the highest value first.

**Q176.** A hardcoded payment provider was added during a launch crunch and never logged. What kind of debt is it, and why is it dangerous?

**Answer:** Deliberate and untracked: nobody else knows it exists, so the interest silently compounds

Log it as a tech-debt item and prioritise by how often the interest is paid.

**Q177.** A team adopts an AI coding assistant, and code is written much faster but quality drops and reviews pile up. What adjustment fits?

**Answer:** Lower WIP, add AI-specific checks to the Definition of Done and invest in review capacity

Review becomes the constraint, so the bottleneck has moved.

**Q178.** An organisation mandates Scrum from the top with no buy-in, and managers still demand status reports. What is the likely result?

**Answer:** Agile theatre: ceremonies exist but the mindset doesn't

Use pilots, a coalition, and change management (Kotter).

**Q179.** Which measures best show an agile transformation is working?

**Answer:** Lead time to production, deployment frequency, change failure rate/MTTR, engagement and customer satisfaction

Compliance metrics are easy to game; outcome metrics aren't.

**Q180.** A Centre of Excellence embeds coaches permanently and becomes the approval step for process changes. What is wrong?

**Answer:** It has become a control function; a CoE should curate practices and offer pull-based coaching

A CoE growing faster than the organisation is a warning sign.

---

More free practice: the [Agile & Software Delivery Mastery Path](index.md) curriculum, the [Interview Prep Pack](https://learnmasterypath.com/interview-pack/) and the [free resume ATS check](https://learnmasterypath.com/resume/).
