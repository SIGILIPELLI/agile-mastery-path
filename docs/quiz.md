---
title: "Final Quiz"
description: "Test what you have learned across all four levels of Agile \u0026 Software Delivery Mastery Path with a 20-question final quiz."
---

# Final Quiz

20 questions drawn from all four levels of this course. You need **70% (14 out of 20)** to pass —
you can retake it as many times as you like. Your best result is saved in this browser.

<div id="mp-quiz-root"></div>

<script type="application/json" id="mp-quiz-data">
[
  {
    "question": "Your project's launch date is fixed by a trade show, and scope is negotiable. Which approach fits, and what flexes?",
    "options": [
      "Waterfall: cut testing",
      "Agile: ship the highest-value subset; scope flexes",
      "Neither",
      "Waterfall: extend the date"
    ],
    "correctIndex": 1,
    "explanation": "Whichever of scope, schedule or cost is truly fixed determines the fit."
  },
  {
    "question": "A regulator requires a fixed spec, and changes after fabrication are very costly. Which approach fits best?",
    "options": [
      "Hackathon mode",
      "Kanban with no limits",
      "Waterfall-like (predictive) with sign-off gates",
      "Pure Scrum with no plan"
    ],
    "correctIndex": 2,
    "explanation": "Stable requirements, safety-critical and audit-heavy work reward up-front certainty."
  },
  {
    "question": "The Scrum Master runs the Daily Scrum as a round-robin status report to them. What is the failure and the fix?",
    "options": [
      "It should be the Developers re-planning the next 24 hours; reframe to 'what's in the way of the Sprint Goal'",
      "Make it longer",
      "Move it to weekly",
      "Nothing is wrong"
    ],
    "correctIndex": 0,
    "explanation": "Only the team can act on blockers."
  },
  {
    "question": "Stakeholders never attend the Sprint Review and the backlog is never updated afterward. What is lost?",
    "options": [
      "Nothing",
      "Velocity",
      "The outer feedback loop: the team may efficiently build the wrong thing",
      "Estimation"
    ],
    "correctIndex": 2,
    "explanation": "The Review's output is an updated Product Backlog from stakeholder feedback."
  },
  {
    "question": "Dev A: 10 days, Dev B: 8 days, Dev C: 10 days at focus factor 0.8; QA: 10 days at 0.7. What is the team's effective capacity?",
    "options": [
      "28 person-days",
      "38 person-days",
      "30.4 person-days",
      "29.4 person-days"
    ],
    "correctIndex": 3,
    "explanation": "8 + 6.4 + 8 + 7 = 29.4 (verified by computing)."
  },
  {
    "question": "Backlog 140 points; the last six sprints delivered 18, 22, 15, 24, 19 and 21. About how many sprints, and how should you present it?",
    "options": [
      "3, because velocity is 40",
      "14, a single number",
      "About 7 (140 ÷ 19.8 ≈ 7.06), as a range (about 6 to 9) not a single date",
      "Exactly 7, firm"
    ],
    "correctIndex": 2,
    "explanation": "Velocity varies; a range avoids the 'you said 7 sprints' trap. Verified by computing."
  },
  {
    "question": "Team B's velocity is 30 and Team A's is 20, and a manager wants Team A to 'match B'. What is wrong?",
    "options": [
      "Story points are relative and team-specific, so cross-team comparison is meaningless and invites inflation",
      "Use hours instead",
      "Nothing, set it as a target",
      "Team A is slower"
    ],
    "correctIndex": 0,
    "explanation": "Velocity is for forecasting a team's own capacity."
  },
  {
    "question": "A team has a WIP limit of 4 in Development, all 4 slots full, and one developer finishes early. What is the best move?",
    "options": [
      "Help unblock work stuck downstream (e.g. Review) instead of pulling a new item",
      "Pull a new item anyway",
      "Raise the limit",
      "Take a break always"
    ],
    "correctIndex": 0,
    "explanation": "Pull systems start new work only when downstream capacity exists."
  },
  {
    "question": "A CFD shows 'In Progress' widening while 'Done' flattens for three weeks. What does it indicate?",
    "options": [
      "Faster delivery",
      "WIP is growing and throughput is dropping: a bottleneck is forming",
      "Stable flow",
      "Fewer items"
    ],
    "correctIndex": 1,
    "explanation": "Parallel bands signal stable flow."
  },
  {
    "question": "Average cycle time is 10 days with 20 items in progress. What throughput does Little's Law imply?",
    "options": [
      "10 items per day",
      "2 items per day (WIP ÷ cycle time)",
      "200 items per day",
      "0.5 items per day"
    ],
    "correctIndex": 1,
    "explanation": "Average cycle time = WIP ÷ throughput, so throughput = 20 ÷ 10 = 2."
  },
  {
    "question": "A story reads 'Improve search' and is 'too big to estimate'. What should refinement do?",
    "options": [
      "Pull it into the sprint",
      "Delete it",
      "Split it (e.g. by workflow step, business rule or happy path versus edge cases) into independent, testable stories",
      "Estimate it as 100"
    ],
    "correctIndex": 2,
    "explanation": "Large epics are the most common refinement blocker."
  },
  {
    "question": "Mid-sprint, someone asks to 'squeeze in' a nice-to-have unrelated to the Sprint Goal. What do you do?",
    "options": [
      "Silently accept it",
      "Add it and drop tests",
      "Defer it to the backlog for refinement and the next sprint",
      "Cancel the sprint"
    ],
    "correctIndex": 2,
    "explanation": "The filter is whether it threatens the Sprint Goal."
  },
  {
    "question": "A critical production outage lands mid-sprint. What is right?",
    "options": [
      "Accept it and renegotiate sprint scope to protect the Sprint Goal",
      "Refuse until next sprint",
      "Cancel the sprint always",
      "Hide it"
    ],
    "correctIndex": 0,
    "explanation": "Critical bugs threaten the goal if unfixed."
  },
  {
    "question": "Four initiatives compete: A has value 8, time criticality 3, risk reduction 5, size 2; B has 13, 8, 3, size 13; C has 5, 13, 2, size 3. Which has the highest WSJF, and what is it?",
    "options": [
      "C, with 20",
      "A, with (8+3+5) ÷ 2 = 8.0 (B ≈ 1.8, C ≈ 6.7)",
      "B, with 24",
      "B, with 1.8"
    ],
    "correctIndex": 1,
    "explanation": "WSJF = (value + time criticality + risk reduction) ÷ job size. Verified by computing."
  },
  {
    "question": "Which contract structure supports agile best?",
    "options": [
      "Pay on final acceptance only",
      "Unlimited T&M with no cap",
      "A fixed budget and cadence with a flexible backlog, plus 'money for nothing, change for free'",
      "Fixed price with a frozen feature list"
    ],
    "correctIndex": 2,
    "explanation": "The vendor's incentive shifts from defending scope to delivering the highest value first."
  },
  {
    "question": "A hardcoded payment provider was added during a launch crunch and never logged. What kind of debt is it, and why is it dangerous?",
    "options": [
      "Accidental, discovered",
      "Bit rot",
      "Deliberate and untracked: nobody else knows it exists, so the interest silently compounds",
      "No debt"
    ],
    "correctIndex": 2,
    "explanation": "Log it as a tech-debt item and prioritise by how often the interest is paid."
  },
  {
    "question": "A team adopts an AI coding assistant, and code is written much faster but quality drops and reviews pile up. What adjustment fits?",
    "options": [
      "Double the sprint length",
      "Raise WIP",
      "Lower WIP, add AI-specific checks to the Definition of Done and invest in review capacity",
      "Skip review"
    ],
    "correctIndex": 2,
    "explanation": "Review becomes the constraint, so the bottleneck has moved."
  },
  {
    "question": "An organisation mandates Scrum from the top with no buy-in, and managers still demand status reports. What is the likely result?",
    "options": [
      "Self-organising teams",
      "Better quality",
      "Fast transformation",
      "Agile theatre: ceremonies exist but the mindset doesn't"
    ],
    "correctIndex": 3,
    "explanation": "Use pilots, a coalition, and change management (Kotter)."
  },
  {
    "question": "Which measures best show an agile transformation is working?",
    "options": [
      "Percent of teams doing Scrum",
      "Number of certifications",
      "Lead time to production, deployment frequency, change failure rate/MTTR, engagement and customer satisfaction",
      "Points per sprint"
    ],
    "correctIndex": 2,
    "explanation": "Compliance metrics are easy to game; outcome metrics aren't."
  },
  {
    "question": "A Centre of Excellence embeds coaches permanently and becomes the approval step for process changes. What is wrong?",
    "options": [
      "It has become a control function; a CoE should curate practices and offer pull-based coaching",
      "It needs more coaches",
      "It needs a mandate",
      "Nothing"
    ],
    "correctIndex": 0,
    "explanation": "A CoE growing faster than the organisation is a warning sign."
  }
]
</script>
