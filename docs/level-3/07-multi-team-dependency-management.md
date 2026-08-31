# 07 · Multi-Team Dependency Management

Once more than one team shares a product, a codebase, or a platform, "Team
A is blocked on Team B" becomes routine. Left unmanaged, dependencies
silently determine the real schedule regardless of what any single team's
Sprint Backlog says. This module covers making them visible and manageable.

## Types of dependencies

| Type | Example | Typical fix |
|---|---|---|
| Technical | Team A's feature needs an API Team B hasn't built yet | Sequence work; build a stub/mock in the meantime |
| Resource | Both teams need the one engineer who knows the legacy billing system | Cross-train, or explicitly schedule that person's time across teams |
| Knowledge | Team A doesn't know a constraint only Team B's domain expert knows | Early cross-team refinement session, not discovered mid-sprint |
| Sequencing | Feature B can't ship before feature A per business/legal reasons | Backlog ordering reflects the constraint, visible to both teams |

## Making dependencies visible

A dependency invisible until the sprint it blocks is a dependency that
already cost you the sprint. Visibility has to happen at refinement/planning
time, not discovery time.

| Technique | How it works |
|---|---|
| Dependency board / cross-team backlog tags | Every story tagged with which other team(s) it depends on or is depended on by |
| Scrum of Scrums | A short, regular sync (not a status meeting) among representatives of dependent teams, focused on blockers |
| Big-room/PI planning (SAFe-style, or a lightweight equivalent) | Teams jointly sequence work across a shared timeline before committing |
| Shared roadmap view | One visual timeline showing all teams' major work, dependencies drawn as arrows |

## Scrum of Scrums, done well

| Healthy version | Common failure mode |
|---|---|
| Each rep reports only cross-team blockers, not their team's full status | Turns into a second Daily Scrum re-reporting internal team status |
| Short (15 min), focused, action-oriented | Runs long because it tries to solve problems live instead of parking them |
| Attendees can act — escalate or unblock on the spot | Attendees are messengers with no authority, so nothing resolves |

The single fix that prevents the most common failure: cap the question at
"what does another team need from us, or what do we need from another
team" — anything else belongs in that team's own Daily Scrum.

## A worked example

Three teams building a checkout redesign discover in week 6 of an 8-week
project that Team A's payment-method story depends on a shared component
Team C was refactoring — and Team C's refactor isn't scheduled to finish
until week 7. Neither team knew until Team A's story failed integration
testing.

Root cause: no dependency board existed; refinement happened per-team in
isolation. The fix: the three teams start a twice-weekly 15-minute Scrum of
Scrums, add a dependency-tag column to each team's backlog, and hold one
joint refinement session before each new initiative to surface
cross-team dependencies before sprint commitments are made. The next
initiative surfaces a similar dependency in week 1 instead of week 6,
giving Team C's refactor time to be resequenced ahead of the dependent
work.

## Exercise

For three teams sharing one platform, where Team X needs a shared library
change from Team Y before it can start its own top-priority story: (1)
classify the dependency type using the table, (2) propose a visibility
mechanism to catch this two sprints earlier than discovery-time, (3) draft
a 4-question Scrum of Scrums agenda focused only on cross-team blockers,
and (4) name one resequencing decision the backlog should reflect once the
dependency is known.
