# 01 · What Is the SDLC?

The **Software Development Life Cycle (SDLC)** is the sequence of phases a
piece of software passes through from "someone has an idea" to "someone is
using it in production and it's being maintained." Every methodology you'll
meet in this course — Waterfall, Scrum, Kanban, hybrid models — is really
just a different way of *arranging and repeating* the same underlying set of
phases. Learning the SDLC first means every later methodology becomes a
variation on a theme instead of a brand-new thing to memorize.

## The six phases, and what each one actually produces

| Phase | Core question it answers | Typical output |
|---|---|---|
| 1. Requirements | What does the business/user actually need? | Requirements document, user stories, acceptance criteria |
| 2. Design | How will the system be structured to meet that need? | Architecture diagram, data model, UI wireframes, API contracts |
| 3. Implementation | Build the thing | Working code, unit tests |
| 4. Testing | Does it actually do what was specified, correctly? | Test results, defect log, sign-off |
| 5. Deployment | Get it into the hands of real users | Release, deployment runbook, rollback plan |
| 6. Maintenance | Keep it working and improve it over time | Bug fixes, patches, feature updates, monitoring |

These phases exist regardless of methodology — the difference between
Waterfall and Agile is not *which* phases exist, but **how often you cycle
through them and in what order**. Waterfall runs the six phases once, in
strict sequence, for the whole product. Agile runs a compressed version of
all six phases repeatedly, in small increments (a sprint), for a thin slice
of the product each time.

## A worked example: password reset feature, traced through all six phases

Take a concrete feature — "let users reset a forgotten password" — and trace
it through the SDLC to see what each phase means in practice:

| Phase | Concrete work for "password reset" |
|---|---|
| Requirements | User story: "As a user who forgot my password, I want to request a reset link by email so I can regain access." Acceptance criteria: link expires in 30 minutes, one active link per user, rate-limited to 3 requests/hour. |
| Design | Sequence diagram: user submits email → server generates a signed, time-limited token → email sent via provider → user clicks link → server validates token → password-change form shown. Data model: add `reset_token`, `reset_token_expires_at` columns to the `users` table. |
| Implementation | Write the `POST /password-reset/request` and `POST /password-reset/confirm` endpoints, the token generator, the email template, and the new-password form. |
| Testing | Unit test the token expiry logic; test rate limiting triggers on the 4th request; manually verify the email actually arrives and the link works end-to-end; test an expired-token error path. |
| Deployment | Run the database migration adding the two new columns; deploy the API and frontend behind a feature flag; monitor error rates for the first hour. |
| Maintenance | Two weeks later, a support ticket reports users on corporate email filters never receive the link — investigate, discover it's landing in spam, adjust the sender domain's SPF/DKIM records. |

Notice that "maintenance" isn't an afterthought bolted onto the end — it is
where most software actually spends most of its life. A feature that took
two weeks to build commonly gets patched and adjusted for years afterward.

## Why the SDLC matters even if you never touch Waterfall again

Some learners are tempted to skip straight to Scrum because "that's what my
company uses." Two things go wrong if you do:

1. **You can't debug a broken process you don't understand.** If a team's
   Scrum implementation is producing buggy releases, the actual defect is
   usually that one of the six underlying SDLC phases is being skipped or
   rushed (often testing) — and you won't spot that if you only know Scrum
   ceremony names, not what those ceremonies are supposed to accomplish.
2. **Every real methodology is a dialect of the SDLC, not a replacement for
   it.** Scrum's sprint review is doing the work of "deployment sign-off";
   its Definition of Done is doing the work of "testing phase complete."
   Kanban's "Done" column is doing the same job with different vocabulary.

## Exercise

Pick a feature you've used recently in any app (a "like" button, a search
filter, a checkout flow — anything with real user-facing behavior). Fill out
a table with the same six phases as above, and write one concrete,
plausible sentence for what happened in each phase for that specific
feature — including at least one specific *test case* you'd expect the team
to have run in the Testing phase, and one specific *maintenance* issue that
could plausibly come up two months after launch. Do not write generic
descriptions ("they tested it") — be as concrete as the password-reset
example.
