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

## How It Actually Works

The nested-loop model isn't just a taxonomy — the loops actually depend on
each other in a specific direction, and most "ceremony theater" failures are
a lower loop silently substituting for a higher one it can't actually
replace.

**Why a tight Daily Scrum can coexist with building the wrong thing.** The
Daily Scrum's feedback signal is purely internal — it only checks "are we on
pace against the plan we already made," which says nothing about whether the
plan itself is still correct. A team can run a crisp, efficient 12-minute
Daily Scrum every single day while the Sprint Review — the loop that checks
the plan against outside reality — gets skipped or reduced to a slide deck.
The inner loop optimizing something that was never validated against the
outer loop is exactly how a team reports "we're on track" for eight straight
sprints while shipping something stakeholders don't actually want; the inner
loop has no mechanism to detect that failure, because detecting it isn't its
job.

**Why timeboxes surface upstream problems instead of causing them.** A
timebox is a fixed amount of "conversation budget" for a fixed scope of
decision. When Sprint Planning needs 6 hours, the actual bottleneck is
almost never "the team talks too much" — it's that the items being planned
arrive underspecified, so the room has to do real analysis work (What does
this actually mean? Is this even one story or three?) live, in the meeting,
that should have already happened in backlog refinement. Extending the
timebox absorbs that missing work without fixing it, which is why the same
6-hour Planning recurs sprint after sprint until refinement itself is fixed
— the symptom is portable, the timebox just relocates it.

**Why "what did you do yesterday" and "what's blocking the goal" produce
structurally different meetings.** The first question's natural audience is
whoever is listening and evaluating — it invites a status report because it's
literally asking for one. The second question has no sensible audience
except teammates who might be able to help, because only they can act on a
blocker; a manager hearing "I'm blocked on the categorization API" can't fix
it, but the developer sitting three feet away who wrote that API can. This is
why the tech-lead-coaching step in the worked example is necessary and not
optional — as long as the tech lead answers with assignments, the room
correctly learns that the real audience for the meeting is the tech lead,
and reverts to reporting to them regardless of which question is nominally
asked.

## Exercise

Pick one Scrum event from the table above that you believe is running
poorly on a team you've observed (or invent a plausible scenario). Write:
(1) which failure mode from the table it matches, (2) the specific symptom
that reveals it (a quote, a pattern, a duration), (3) a two-sprint
remediation plan like the worked example above, and (4) one metric or
observable sign you'd check after two sprints to confirm the fix worked.
