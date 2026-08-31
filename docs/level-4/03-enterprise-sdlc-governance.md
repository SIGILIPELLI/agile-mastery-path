# 03 · Enterprise SDLC Governance

Large enterprises carry real governance obligations — audit, compliance,
security sign-off, financial controls — that don't disappear because
delivery teams adopt agile. The master-level skill is designing governance
that satisfies those obligations without recreating a stage-gated waterfall
process around every sprint.

## Where governance and agile collide

| Governance need | Traditional mechanism | Agile-compatible alternative |
|---|---|---|
| Change approval / audit trail | Change Advisory Board sign-off before each release | Automated, logged approvals baked into the CI/CD pipeline (who approved, what changed, when) |
| Security review | A dedicated security-gate phase before release | Security-as-code checks (SAST/DAST) run on every build; a human reviews only flagged exceptions |
| Financial controls (capitalization, budget) | Fixed project budgets tied to a fixed scope | Budgets tied to a team/product for a period (quarter), not to a project's fixed deliverable list |
| Regulatory documentation | A large document produced at the end of a phase | Documentation generated incrementally, alongside the work, from artifacts already produced (tickets, PRs, test results) |

## A governance model that scales

| Layer | What it governs | Cadence |
|---|---|---|
| Team | Day-to-day technical and process decisions | Continuous |
| Program/product | Cross-team priorities, dependencies, release readiness | Sprint/PI boundary |
| Portfolio | Investment allocation across products, strategic risk | Quarterly |
| Enterprise/compliance | Regulatory, security, audit obligations | Continuous, automated where possible; exception-based human review |

The design principle: push governance decisions down to the lowest layer
capable of making them safely, and automate the enterprise layer wherever
the check is mechanical (a lint rule, a security scan) rather than
judgment-based.

## Common anti-patterns

| Anti-pattern | Why it happens | Fix |
|---|---|---|
| A single CAB meeting gates every team's every release | Historical control point never re-examined after agile adoption | Replace with automated, logged approval for standard changes; reserve CAB for genuinely high-risk changes |
| Compliance documentation written after the fact, disconnected from real work | Documentation treated as a separate deliverable instead of a by-product | Generate docs from the actual artifacts (commit history, test reports, ticket trail) continuously |
| Portfolio budgeting still assumes fixed-scope annual projects | Finance processes never updated for iterative delivery | Fund persistent teams/products for a period, not one-off projects with fixed scope |

## A worked example

A financial-services company's release process requires every production
change to pass a weekly Change Advisory Board meeting, regardless of size —
a habit inherited from a pre-agile era when releases were rare and risky.
Teams now deploy daily but batch changes into the weekly window to satisfy
the CAB, reintroducing the large, risky, infrequent-release pattern agile
was meant to eliminate.

The fix: the CAB is redefined to review only high-risk changes (touching
payment processing, PII, or external regulatory reporting), identified by
an automated risk-classification check in the pipeline. Standard changes
that pass all automated gates (tests, security scans, a peer-reviewed PR)
deploy continuously with an auto-generated audit log satisfying the same
compliance requirement the CAB previously covered — and the audit trail is
provably more complete, since it's generated from every change instead of a
weekly sample.

## Exercise

Your organization requires a compliance officer to manually approve every
production deployment, and this has become the single largest bottleneck to
daily releases. Using this module's framework: (1) classify this governance
need using the "governance need" table, (2) propose an agile-compatible
alternative mechanism, (3) define which layer (team/program/portfolio/
enterprise) should own the exception-based human review going forward, and
(4) name one piece of evidence the automated version would need to produce
to satisfy an auditor that manual sign-off previously provided.
