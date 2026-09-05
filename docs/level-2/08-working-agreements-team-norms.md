# 08 · Working Agreements & Team Norms

Two teams can run identical Scrum ceremonies and still feel completely
different to work on — the difference is usually an unwritten (or written
and honored) set of norms about how people actually treat each other and
their work. This module makes those norms explicit and actionable.

## What belongs in a working agreement

A working agreement is a short, team-authored, team-owned document — not
imposed by a manager — covering the friction points that ceremonies alone
don't resolve.

| Category | Example agreements |
|---|---|
| Communication | Core hours everyone is reachable; response-time expectation for Slack/chat |
| Meetings | Cameras on/off norm; no meetings before 10am; Daily Scrum starts on time regardless of who's missing |
| Code/work quality | PR review turnaround within 1 business day; no merging your own PR |
| Conflict | Disagreements raised directly first, escalated to the team only if unresolved after one attempt |
| Focus | No pinging people during marked "deep work" blocks; interruptions reserved for true blockers |
| Decision-making | Reversible decisions made by whoever's doing the work; irreversible ones brought to the team |

## Why "the team writes it" matters more than what it says

A rule imposed by a manager is compliance; a rule the team wrote for itself
is a commitment. The mechanism: people follow agreements they helped author
because violating them means letting down peers they chose these terms
with, not breaking a policy from someone external to the work.

| Imposed norm | Team-authored norm |
|---|---|
| "Cameras must be on" (from HR) | "We agreed cameras on helps us read the room — let's do it" |
| Compliance is grudging, decays fast | Compliance is social, self-reinforcing |
| Violations handled by management | Violations handled peer-to-peer, in the retro |

## Building and maintaining agreements

1. Draft in a retrospective, not a separate "culture" meeting — norms
   emerge naturally from friction the team just experienced.
2. Keep it short (5–10 items) and visible (pinned in the team channel or
   board), not buried in a wiki no one opens.
3. Review it explicitly every few sprints, or immediately after a new
   member joins — a new hire should read it on day one.
4. Treat violations as a retro topic, not a performance conversation —
   the norm may be wrong, or need adjusting, before assuming the person is.

## A worked example

A team has recurring friction: half the team joins Daily Scrum 5 minutes
late, so it either starts late or restarts information for latecomers. In
retro:

1. The team names the actual cost: 5 minutes × 6 people × 5 days = 150
   person-minutes/week lost to re-explaining.
2. They agree a norm: "Daily Scrum starts at :00 sharp, no waiting; if you
   miss it, catch up async in the channel — you don't get a re-summary."
3. They write it into the working agreement doc, visible on the team
   board.
4. Two sprints later, in retro, lateness is down but not zero — one person
   is consistently blocked by a prior meeting. The team adjusts the Daily
   Scrum time itself by 15 minutes rather than continuing to penalize one
   person for a scheduling conflict outside their control.

The fix worked because the team owned both the diagnosis and the norm, and
revisited it when it didn't fully solve the problem the first time.

## How It Actually Works

The "team writes it, not a manager" rule isn't a feel-good preference — it
changes the actual enforcement mechanism a norm runs on, and that mechanism
is what determines whether it survives contact with a bad week.

**Why authorship changes the cost of violating a norm.** A rule imposed
externally is enforced by threat of consequence from someone outside the
day-to-day work — which means the moment that person isn't watching, the
cost of violating drops to near zero, and compliance decays. A rule the team
wrote together is enforced by a different, cheaper-to-trigger, harder-to-
evade mechanism: social reciprocity among people who see each other daily.
Showing up late to a Daily Scrum you personally agreed to start on time
means letting down five specific people you'll sit in the next meeting with,
not an abstract policy — and that social cost doesn't require anyone to be
"watching" in the enforcement sense, because the team *is* the audience,
every day. This is why imposed norms need active policing to persist and
team-authored ones mostly self-sustain.

**Why quantifying the friction (150 person-minutes/week) is the step that
actually produces buy-in, not just data.** A vague complaint ("people are
late") is easy to individually dismiss ("I'm only 5 minutes late, that's not
a big deal") because each person only sees their own small contribution.
Converting it into a team-wide cost makes the externality visible — the
5-minutes-times-six-people framing is what lets someone reconsider whether
being personally "only a little" late is actually the small thing it feels
like from the inside. This is the same mechanism behind why teams don't fix
problems they haven't measured: the cost has to be made visible before
anyone will trade off against it.

**Why treating a violation as a retro topic (not a performance issue) keeps
the agreement adaptive instead of brittle.** When the recurring latecomer
turns out to have a genuine scheduling conflict, escalating to a performance
conversation would punish a person for a norm that was actually miscalibrated
to the team's real constraints. Routing it back through retro treats the
*norm itself* as the variable under test, not the person — which is exactly
why the team's second fix (moving the meeting time) targets the actual root
cause instead of demanding the one person keep failing to meet an
unreasonable norm. A working agreement that can't be revised when it turns
out to be wrong isn't a living agreement, it's a rule — and rules decay the
same way imposed ones do.

## Exercise

Draft a working agreement (6–8 items) for a newly formed 5-person team.
For each item: (1) name the specific friction it prevents, (2) state how a
violation would be raised (peer-to-peer? retro topic?), and (3) pick one
item and describe how you'd revise it if, two sprints later, it turned out
to cause a *new* problem instead of solving the old one.
