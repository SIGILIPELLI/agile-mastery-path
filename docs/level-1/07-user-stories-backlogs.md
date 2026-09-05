# 07 · User Stories & Backlogs

A **user story** is a small, specific expression of a need, written from the
perspective of the person who has it — not a technical specification. A
**backlog** is the ordered collection of all such stories (and other work
items) a team might build. Together they're how Agile teams capture "what
to build" without writing the kind of exhaustive up-front specification
Waterfall relies on. Getting this format right is what makes flexible,
incremental delivery possible at all — a vague or oversized story is where
most sprint failures actually start.

## The standard format, and why each part exists

> **As a** [role], **I want** [capability], **so that** [benefit].

| Part | Purpose | What goes wrong if it's missing |
|---|---|---|
| Role | Identifies *whose* need this is | Stories become generic feature requests disconnected from a real user's actual problem |
| Capability | The concrete thing being asked for | Without it, there's nothing to build — this is the only part people usually remember |
| Benefit ("so that") | The *reason* the capability matters | Without it, a developer can't make good judgment calls on edge cases — they don't know what the feature is actually for |

Example: *"As a returning customer, I want my saved shipping address to be
pre-filled at checkout, so that I don't have to re-type it every order."*
The "so that" clause tells the developer that the point is reducing repeated
typing — which means if the saved address is out of date, the right
behavior is to let the user edit it inline, not force a full re-entry from
scratch. Without the benefit clause, that judgment call has no anchor.

## Acceptance criteria: the definition of "done" for this one story

A story alone is too vague to build against. **Acceptance criteria** are the
specific, testable conditions that must hold for the story to be considered
complete:

> Story: *As a returning customer, I want my saved shipping address
> pre-filled at checkout, so that I don't have to re-type it every order.*
>
> Acceptance criteria:
> - Given a logged-in customer with a saved address, when they reach
>   checkout, the address fields are pre-filled.
> - The customer can edit any pre-filled field before submitting.
> - A customer with no saved address sees an empty form (no crash, no
>   placeholder garbage).
> - A customer with two saved addresses is shown a selector, not just the
>   most recent one silently applied.

This "Given/When/Then" phrasing (from Behavior-Driven Development) is not
mandatory, but it forces the same discipline Waterfall gets from a formal
requirements document — just scoped to one small story instead of the whole
system.

## The INVEST checklist for a well-formed story

| Letter | Means | Bad example | Fixed |
|---|---|---|---|
| I — Independent | Can be built and delivered without waiting on another unfinished story | "Add checkout page" (depends on 6 other unstated stories) | Split into address, payment, and order-summary stories |
| N — Negotiable | A starting point for a conversation, not a rigid contract | "Build exactly this Figma mockup pixel-for-pixel" | "Let the user review their order before confirming" |
| V — Valuable | Delivers value to a user or the business, not just a technical task | "Refactor the OrderService class" | "Reduce checkout errors by validating card numbers before submit" (the refactor becomes the *how*, not the story itself) |
| E — Estimable | The team has enough information to size it | "Improve performance" (of what? by how much?) | "Checkout page loads in under 2 seconds on a 3G connection" |
| S — Small | Fits comfortably in one sprint | "Build the entire checkout flow" | Split into 5–8 stories, each independently shippable |
| T — Testable | Clear pass/fail acceptance criteria exist | "Make the UI nicer" | "Error messages appear inline, in red, within 200ms of a failed validation" |

## The backlog: ordered, not just a list

A Product Backlog is **ordered by priority**, not organized by category or
chronology. The top few items should be small and detailed enough to pull
directly into a sprint; items further down can stay large and vague until
they're closer to the top — a discipline called "backlog grooming" or
"refinement" (covered in depth in Level 2).

| Position | Item | State |
|---|---|---|
| 1 | Pre-fill saved address at checkout | Fully specified, ready to pull into next sprint |
| 2 | Support saved payment methods | Fully specified |
| 3 | One-click reorder from order history | Rough acceptance criteria, needs a design review |
| 4 | "Buy for a friend" gifting flow | One-sentence idea, not yet broken into stories |
| 47 | Explore AR product preview | A note in a "someday" section, unestimated |

## A worked example: splitting an oversized story

"As a user, I want to manage my account" is a classic INVEST failure — too
big, not testable, not really one thing. Splitting it:

- As a user, I want to update my email address, so that account
  notifications reach me.
- As a user, I want to change my password, so that I can recover from a
  suspected compromise.
- As a user, I want to delete my account, so that I can leave the service
  and have my data removed per privacy policy.
- As a user, I want to download my data, so that I comply with my own
  record-keeping or move to another service.

Each of these is independently small, testable, and shippable — a team
could deliver "change password" in one sprint without needing "delete
account" to exist yet.

## How It Actually Works

User stories work as a planning unit because they encode *just enough*
information to make three different decisions later, and INVEST is really a
checklist for whether those decisions are still possible.

**Why the "so that" clause changes what happens during implementation, not
just documentation.** A developer implementing "pre-fill the saved address"
without the benefit clause has no way to resolve an edge case that the
acceptance criteria didn't anticipate — say, an address with a typo the
customer never noticed. With the benefit clause ("so I don't have to
re-type it"), the developer can reason from intent: pre-fill *and* leave it
editable, because forcing a full re-entry on a typo defeats the entire
purpose of the story. Without it, the developer either guesses or stops and
asks — and a team of eight developers each stopping to ask on ambiguous
edge cases is the throughput cost that a well-formed story is specifically
designed to avoid.

**Why splitting for INVEST is a dependency-graph operation, not just
"making things smaller."** "Manage my account" fails Independent because it
secretly bundles several features that share no code path (email change
touches notification settings; password change touches the auth session;
account deletion touches the data-retention pipeline) — bundling them means
none can ship until all are done, so if deletion needs a legal review that
stalls for two weeks, email-change sits blocked behind it for no technical
reason. Splitting along the natural seams in the underlying system (each
piece touches a different subsystem) is what actually makes each piece
Independent — the INVEST letters aren't independent virtues, they're mostly
downstream consequences of finding the right seam: split correctly and a
story becomes small, testable, and estimable almost automatically; split
along the wrong seam (e.g., by UI screen instead of by subsystem) and you get
several "small" stories that are still secretly coupled.

**Why backlog ordering has to be a single ranked list, not buckets.** A
backlog organized into "High/Medium/Low" buckets still leaves ambiguous which
of ten "High" items to pull first — the moment two items compete for the same
sprint capacity, someone has to break the tie anyway, just later and under
more time pressure. A single ordered list forces that tie-breaking judgment
to happen during refinement, when there's time to think about it, rather
than during Sprint Planning under a ticking clock — which is also why only
the top few items need to be fully detailed: detailing item 47 today is work
that will very likely be thrown away before it's ever relevant.

## Exercise

Write five user stories for a product of your choosing (real or invented),
each in the "As a / I want / so that" format. For each, write at least two
acceptance criteria. Then take one deliberately oversized, vague story (like
"As a user, I want to manage my profile") and split it into 3–4 INVEST-
compliant stories, showing your reasoning for the split. Finally, arrange
all your stories into a single ordered backlog and justify the ordering in
one sentence per item — priority order, not just a list.
