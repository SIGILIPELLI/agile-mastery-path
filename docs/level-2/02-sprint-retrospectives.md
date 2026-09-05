# 02 · Sprint Retrospectives

A Retrospective that produces the same three complaints sprint after sprint
isn't failing by accident — it's usually missing a structure that turns
observations into owned, checked actions. This module gives you that
structure.

## The five-stage retrospective

Ad-hoc "what went well / what didn't" retros tend to collapse into venting.
A structured retro moves deliberately through five stages, each with a
different purpose:

| Stage | Purpose | Typical technique |
|---|---|---|
| Set the stage | Get everyone present and safe to speak | Check-in question, restate the Prime Directive |
| Gather data | Surface facts and events from the sprint, not opinions yet | Timeline, mood chart, sprint metrics |
| Generate insights | Ask *why* patterns occurred | 5 Whys, fishbone diagram, grouping/affinity mapping |
| Decide what to do | Convert insight into 1–3 concrete actions | Dot-voting, effort/impact grid |
| Close | Confirm ownership and appreciate the team | Restate owners + due sprint, retro-on-the-retro |

Skipping straight from "set the stage" to "decide what to do" is the most
common failure — it produces actions aimed at symptoms because the team
never separated *what happened* from *why it happened*.

## The Prime Directive

> "Regardless of what we discover, we understand and truly believe that
> everyone did the best job they could, given what they knew at the time,
> their skills and abilities, the resources available, and the situation at
> hand." — Norm Kerth

Reading this aloud at the start reframes the retro from blame-assignment to
system-improvement. A recurring bug isn't "Dana's fault" — it's a gap in the
Definition of Done, a missing test suite, or an unclear requirement that the
team can fix together.

## Anti-patterns and fixes

| Anti-pattern | Symptom | Fix |
|---|---|---|
| Groundhog day | Same complaint every sprint, no follow-through | Open the retro by reviewing last sprint's action items first |
| Blamestorm | Retro turns into finger-pointing | Reinforce the Prime Directive; reframe to systems, not people |
| Action item graveyard | 8 actions logged, 0 done | Cap at 1–3 actions, each with a named owner and a sprint deadline |
| Facilitator fatigue | Same person runs every retro the same way | Rotate facilitation; vary the technique (see table above) |
| Silent majority | 2 people talk, rest nod | Use written brainstorming (sticky notes / async doc) before discussion |

## A worked example

A 6-person team has run 12 identical retros: "testing is rushed at the end
of the sprint" comes up every time, with no lasting fix. Applying the
five-stage structure:

1. **Gather data**: the team builds a timeline of the last sprint and
   notices testing always starts on day 8 of a 10-day sprint — not because
   testers are slow, but because stories aren't "ready to test" until
   development finishes near the end.
2. **Generate insights**: a 5 Whys chain traces this to the Definition of
   Ready not requiring stories to be split small enough to finish mid-sprint.
3. **Decide**: one action — amend the Definition of Ready to cap story size
   at 3 days of dev work, owned by the Product Owner, effective next sprint.
4. **Close**: the team schedules a 10-minute check at the mid-sprint Daily
   Scrum to confirm at least one story has reached "ready to test."

Two sprints later, testing starts by day 5 on average — the retro action
addressed the upstream cause, not the symptom.

## How It Actually Works

"Groundhog day" retros aren't a facilitation-skill problem so much as a
*root-cause depth* problem — and the five-stage structure works specifically
because it enforces a minimum depth before anyone is allowed to propose a
fix.

**Why skipping straight to "decide what to do" produces symptom-fixes.**
Without a data-gathering step, the loudest, most recent memory in the room
becomes the working theory of what happened — usually the surface symptom
("testing was rushed"), not the mechanism that produced it. An action item
proposed straight off that surface symptom ("let's just test earlier") has
no mechanism to change anything, because it doesn't address *why* testing
was starting late — it's a wish, not a lever. The 5 Whys chain in the worked
example is doing real work: each "why" moves one causal link upstream, from
"testing is rushed" → "testing starts day 8" → "stories aren't ready to test
until late" → "the Definition of Ready doesn't cap story size" — and only at
that fourth link does an actual controllable variable (story size cap)
appear. Stop at link one or two and every proposed fix targets something the
team can't actually control (telling testers to "hurry up" isn't a lever;
capping story size is).

**Why capping actions at 1-3 is a completion-rate mechanism, not a
politeness rule.** Each action item competes for the same scarce resource —
someone's attention amid a new sprint's work — and attention allocated to
action 6 is attention *not* allocated to actions 1-3 finishing. Teams that
log 8 actions per retro don't have 8x the improvement capacity; they have the
same capacity spread thin enough that the marginal action gets essentially
zero follow-through, which is exactly the "action item graveyard" pattern —
it's not that people forget, it's that an 8-item list was never going to be
executed by a team also shipping a sprint's worth of feature work.

**Why the Prime Directive changes what data actually surfaces.** People
under implicit threat of blame systematically under-report the facts that
would implicate them — which means a retro run without it doesn't just feel
worse, it structurally gathers *less accurate data*, because the person who
knows the real reason testing ran late (they were also fixing an unrelated
production issue no one else saw) has an incentive to stay quiet rather than
supply the fact that would actually unlock the correct root cause.

## Exercise

Take a recurring complaint from a real or invented team's retros. Run it
through the five-stage structure: (1) one fact-based data point (not an
opinion) that would appear in "gather data," (2) a 5-Whys chain of at least
three "why"s that reaches a systemic root cause, (3) one action item with an
owner and a deadline, and (4) how you'd verify at the next retro that the
action actually worked.
