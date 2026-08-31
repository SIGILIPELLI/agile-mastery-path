# 02 · Agile in Distributed Teams

Scrum's ceremonies assume people can gather in a room, read body language,
and pair informally at a whiteboard. Distributed and remote teams keep the
events but lose those assumptions — this module covers what has to change
deliberately to compensate.

## What breaks first, and why

| Ceremony/practice | Co-located assumption | What breaks remotely |
|---|---|---|
| Daily Scrum | Quick, informal, easy to read the room | Becomes a scheduling puzzle across time zones; harder to sense disengagement |
| Sprint Planning | Whiteboard, sticky notes, spontaneous side-conversations | Needs a shared digital board and explicit facilitation to avoid silent non-participation |
| Retrospective | Psychological safety builds from informal hallway trust | Requires deliberate anonymous-input tools to surface honest feedback |
| Pairing/collaboration | Walk over and look at someone's screen | Requires explicit screen-share norms; async by default unless scheduled |

## Time-zone strategy

| Strategy | How it works | Trade-off |
|---|---|---|
| Follow-the-sun | Work handed off at end of day to the next timezone's team | Needs excellent handoff documentation; can hide who "owns" a problem |
| Overlap window | A required 2–4 hour window where all timezones are online | Simplest to reason about; someone's window is always inconvenient |
| Async-first | Ceremonies default to written/recorded, live meetings are the exception | Slower to resolve ambiguity; needs strong written-communication discipline |

A useful rule: synchronous time is the scarcest resource on a distributed
team — reserve it for things that genuinely need real-time back-and-forth
(sprint planning discussion, retro discussion), and push everything else
(status updates, FYI-style Daily Scrum content) to async written form.

## Making the Daily Scrum async-friendly

A fully synchronous Daily Scrum across a 10-hour time-zone spread forces
someone to attend at 6am or 10pm every day. A hybrid pattern:

1. Each person posts their "what's blocking the Sprint Goal" update in a
   shared async channel within their own working hours.
2. A short synchronous window (15 min, rotating fairness across time
   zones) is reserved only for items that need real-time discussion,
   flagged in the async post.
3. The Scrum Master reads all async posts daily and follows up 1:1 on
   anything that looks blocked but wasn't flagged.

## Building trust and safety without hallway time

Retrospectives need psychological safety to surface real problems; that
safety often comes from informal in-person rapport that distributed teams
don't get for free.

| Technique | Purpose |
|---|---|
| Anonymous input tools (sticky-note boards, forms) before discussion | Lets people raise sensitive points without being first to speak aloud |
| Rotating facilitation across time zones | Prevents one region's culture from dominating retro tone |
| Deliberate non-work time (virtual coffee, informal channel) | Rebuilds some of the rapport hallway conversations used to provide |
| 1:1 check-ins outside ceremonies | Catches disengagement a Daily Scrum update alone won't reveal |

## A worked example

A team split across California and India has a Daily Scrum scheduled at
7am Pacific — 7:30pm in India. Attendance from the India half is
consistently late and disengaged; retro data (via an anonymous board)
reveals two engineers feel the meeting exists for the US half's
convenience. The Scrum Master switches to the async-first pattern above:
written updates posted within each region's working hours, with a 15-minute
synchronous slot rotated weekly between a US-morning and an India-morning
time. Engagement in the sync window becomes near-100% within a month
because attendance is fair across time zones instead of a fixed cost one
side always pays.

## Exercise

For a team split evenly across two time zones 9 hours apart: (1) choose one
of the three time-zone strategies and justify it, (2) redesign the Daily
Scrum using the async-hybrid pattern, specifying exact windows, (3) name
one retro technique from the table you'd use to compensate for lost hallway
trust, and (4) describe one metric or signal (e.g., participation rate)
you'd track for a month to confirm the redesign actually improved fairness.
