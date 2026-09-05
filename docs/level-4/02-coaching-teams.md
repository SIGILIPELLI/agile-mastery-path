# 02 · Coaching Teams

At the master level, the job shifts from running ceremonies to developing
the people and teams who run them. Coaching is a distinct skill from
facilitation or management, and conflating the three is the most common
mistake new agile coaches make.

## Coaching vs. facilitating vs. managing

| Mode | What it does | When to use it |
|---|---|---|
| Facilitating | Guides a process to a group's own outcome, contributes no content | Running a retro, a planning session |
| Coaching | Helps someone find their own answer through questions, doesn't supply the answer | Team is capable but stuck, avoiding a hard conversation, or repeating a pattern |
| Managing/directing | Makes the call and tells people what to do | Genuine emergencies, or when the team lacks the information/authority to decide |

Coaches who default to directing produce compliant teams that never build
their own judgment. Coaches who never direct leave teams flailing in a
genuine crisis. The skill is knowing which mode a situation calls for.

## The coaching stances (ICF-influenced, adapted to agile)

| Stance | Core move | Example question |
|---|---|---|
| Teaching | Explicit knowledge transfer | "Here's how a Definition of Ready works and why it matters" |
| Mentoring | Sharing experience-based judgment | "When I've seen this before, the root cause was usually X — worth checking?" |
| Coaching | Questions that surface the team's own insight | "What do you think is really blocking this, underneath the symptom you named?" |
| Facilitating | Neutral process guidance | "Let's timebox this to 10 minutes and vote on the top three items" |

## A coaching conversation framework (GROW)

| Stage | Purpose | Sample question |
|---|---|---|
| Goal | What does the person/team actually want? | "What would 'better' look like here?" |
| Reality | What's actually happening now? | "What have you already tried?" |
| Options | What could be done? | "What are two or three ways you could approach this?" |
| Will | What will they actually commit to? | "Which of these will you try, and by when?" |

## A worked example

A Scrum Master asks a coach for help because the team consistently
under-delivers on sprint commitments, and the Scrum Master has taken to
quietly cutting scope mid-sprint to protect the team from looking bad. This
has been going on for four sprints.

Using the mode table, the coach recognizes the Scrum Master is stuck in
"managing" (unilaterally fixing the symptom) instead of coaching the team
toward its own fix. Rather than telling the Scrum Master what to change, the
coach runs a GROW conversation: *Goal* — what would the Scrum Master want
the team's relationship with commitments to look like? *Reality* — what has
the Scrum Master tried, and what happened? *Options* — what could surface
the estimation problem to the team instead of hiding it? *Will* — the Scrum
Master commits to raising the pattern openly in the next retrospective
instead of continuing to quietly adjust scope. The team itself then
identifies that estimates aren't accounting for a recurring code-review
bottleneck — a root cause the coach never needed to name, because the team
found it once given the room to.

## How It Actually Works

The Scrum Master's quiet mid-sprint scope-cutting is the specific failure
this module is built to prevent, and understanding *why* coaching works
where directing wouldn't requires looking at what each mode actually does
to the team's own diagnostic capacity.

**Why "quietly fixing the symptom" makes the real problem permanently
invisible.** Every time the Scrum Master trims scope to protect the team
from a missed commitment, the team experiences a sprint that "worked" —
there's no visible failure prompting anyone to ask why the original estimate
was wrong. This is the same mechanism as Module 05, Level 2's DoD-erosion
and Module 06's velocity inflation: hiding the gap between plan and reality
doesn't close the gap, it just prevents the system's own feedback loop
(Retrospective, Module 02, Level 2) from ever detecting it, because the
input that loop needs — a visible miss — never reaches it. The code-review
bottleneck that's actually causing the under-delivery keeps compounding
sprint after sprint, entirely undiagnosed, because the standard signal that
would surface it (a consistently missed commitment) was being manually
suppressed.

**Why a directing answer from the coach would have reproduced the exact
pattern it's trying to fix.** If the coach had simply told the Scrum Master
"stop hiding the miss, raise it in retro," that's technically the right
answer, but delivered as an instruction, it teaches the Scrum Master that
problems get solved by receiving direction from someone with more
experience — which is precisely the dynamic the Scrum Master has been
running with the team, one level down (protecting them rather than exposing
them to the discomfort of finding their own fix). Coaching mode is the only
mode that breaks the pattern at its source, because a GROW conversation's
questions are structurally incapable of transmitting "do X" — they can only
help the Scrum Master arrive at their own version of X, which is what
survives after the coach leaves the room and the Scrum Master faces the next
similar situation alone.

**Why the code-review bottleneck surfacing "on its own" is the actual
success condition, not a lucky accident.** The coach's GROW conversation
only reached the Scrum Master's *behavior* (raise it openly), not the
team's root cause — the team found the bottleneck themselves once given
real, unfiltered information about their own miss rate. This is the direct
payoff of restoring the feedback loop: a team with accurate information
about its own performance has both the motive (an uncomfortable, visible
pattern) and the local knowledge (they experience the code-review delay
directly) to diagnose it faster and more accurately than an outside coach
ever could from secondhand description — coaching's leverage comes from
putting the right people in contact with the right information, not from
being smarter about the problem than they are.

## Exercise

A team lead comes to you frustrated that a senior engineer on the team
consistently overrides other members' technical decisions in code review,
and morale is dropping. Using GROW: (1) write one Goal-stage question you'd
ask the team lead, (2) one Reality-stage question, (3) one Options-stage
question that avoids supplying the answer yourself, and (4) explain how
you'd recognize if this situation actually needed you to shift from
coaching mode into directing mode instead.
