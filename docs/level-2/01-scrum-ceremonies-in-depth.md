# 01 · Scrum Ceremonies in Depth

Level 1 introduced the five Scrum events as a table of timeboxes and
purposes. That's enough to recognize Scrum on paper. Running the ceremonies
well — so they actually produce the outcomes they're designed for, instead
of becoming calendar filler — takes a deeper look at *how* each one should
be facilitated, and the specific ways each one degrades in practice.

## The four inspect-and-adapt loops

Scrum's events aren't independent — they're four nested feedback loops, each
inspecting a different thing at a different frequency.

| Loop | Event(s) | Inspects | Frequency |
|---|---|---|---|
| Product direction | Sprint Review | The Increment, against real stakeholder needs | Every sprint |
| Sprint execution | Daily Scrum | Progress toward the Sprint Goal | Every day |
| Process health | Sprint Retrospective | How the team works together | Every sprint |
| Plan formation | Sprint Planning | What's achievable and valuable next | Every sprint |

Notice the pattern: the *outer* loop (Sprint Review) checks whether you
built the right thing; the *inner* loop (Daily Scrum) checks whether you're
on track to build what you planned. Teams that only run the inner loop well
(tight daily standups) but skip a genuine Sprint Review can be extremely
efficient at building the wrong thing.

## Facilitation failure modes, event by event

| Event | Healthy version | Common failure mode | Fix |
|---|---|---|---|
| Sprint Planning | Team pulls work and forms its own Sprint Goal | PO or manager assigns work top-down | PO presents *why*, team decides *how much* |
| Daily Scrum | Developers re-plan the next 24 hours together | Round-robin status report to the Scrum Master | Ask "what's blocking the Sprint Goal?" not "what did you do yesterday?" |
| Sprint Review | Working software demoed, backlog updated live | Slide deck, no stakeholders, no backlog change | Only demo what's actually done-done; invite real users |
| Sprint Retrospective | Concrete, owned action items | Venting session with no follow-through | Cap at 1–3 actions; review last sprint's actions first |

The single highest-leverage fix here is the last row of the Daily Scrum:
reframing the question from "what did I do" (which produces a status report
to whoever's listening) to "what's in the way of the Sprint Goal" (which
produces a self-organizing team, since only the team can act on blockers).

## Timeboxing is a design constraint, not a suggestion

Every Scrum event is timeboxed for a reason: the timebox forces the
*minimum viable version* of the conversation. A Sprint Planning that runs 6
hours for a 2-week sprint usually means the Product Backlog wasn't refined
beforehand (see Module 03) — the timebox is surfacing an upstream problem,
not causing one. Extending the timebox treats the symptom; fixing backlog
refinement treats the cause.

## A worked example: rescuing a broken Daily Scrum

A support-tooling team's Daily Scrum has become a 25-minute status report to
their tech lead, who then assigns the day's tasks. The Scrum Master
diagnoses this against the table above: this is the "status report" failure
mode, root-caused by a Product Owner/tech-lead pattern that never
established self-organization. Over two sprints, the fix is incremental:

1. **Sprint 1**: The Scrum Master stops calling on people by name and asks
   the team to self-organize the speaking order. The tech lead is coached to
   ask *questions* ("what do you need to unblock that?") instead of giving
   *assignments*.
2. **Sprint 1, Retrospective**: The team names the pattern explicitly and
   agrees the Daily Scrum's only output should be a plan for the next 24
   hours, decided by whoever is doing the work.
3. **Sprint 2**: Daily Scrum drops to 12 minutes. The tech lead now attends
   as a resource to unblock people, not as the person assigning the day's
   work.

## Exercise

Pick one Scrum event from the table above that you believe is running
poorly on a team you've observed (or invent a plausible scenario). Write:
(1) which failure mode from the table it matches, (2) the specific symptom
that reveals it (a quote, a pattern, a duration), (3) a two-sprint
remediation plan like the worked example above, and (4) one metric or
observable sign you'd check after two sprints to confirm the fix worked.
