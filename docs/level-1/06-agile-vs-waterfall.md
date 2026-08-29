# 06 · Agile vs. Waterfall

Modules 2 and 3 covered Waterfall and Agile separately. This module puts
them side by side and gives you a repeatable test for choosing between them
— because in the real world, the question is never "which one is better?"
(neither is, universally) but "which one fits the shape of *this* project's
uncertainty?"

## Head-to-head comparison

| Dimension | Waterfall | Agile |
|---|---|---|
| Requirements | Fixed up front, formally signed off | Expected to evolve; captured as a living backlog |
| Delivery | One release at the end of the project | Incremental releases every sprint/iteration |
| Customer involvement | Concentrated at the start (requirements) and end (acceptance) | Continuous — every sprint review |
| Change mid-project | Formal change-request process, expensive | Expected and routine — the backlog absorbs it |
| Documentation | Comprehensive, produced per phase, often contractually required | "Just enough" — working software is the primary evidence of progress |
| Risk discovery | Late (often in Testing, near the end) | Early and often (every sprint surfaces new information) |
| Budget/schedule certainty | High, if requirements really are stable | Lower per-feature certainty, but total spend rate is knowable |
| Team structure fit | Works with a chain of specialist hand-offs across teams | Needs a small, cross-functional, co-located-or-well-synced team |
| Best contract type | Fixed-price, fixed-scope | Time-and-materials, or scope-flexible fixed-budget |

## The decision test: is scope, schedule, or cost the fixed variable?

Every project has exactly one of these three that is genuinely fixed, and
the other two must flex to accommodate it. Naming which one is fixed for
your specific project answers the Agile-vs-Waterfall question directly:

| If this is truly fixed... | ...then this should flex | Fits |
|---|---|---|
| Scope (a legally mandated form, a hardware spec, a contractual deliverable list) | Schedule and/or cost | **Waterfall** |
| Schedule (a trade show launch date, a regulatory deadline) | Scope | **Agile** — ship the highest-value subset that's ready by the date |
| Cost (a fixed annual budget, a fixed team size) | Scope and schedule | **Agile** — a fixed team working fixed-length sprints, delivering whatever the backlog yields |

Most requests to "just be more agile" without examining this test are
really requests to fix all three variables simultaneously — scope, schedule,
*and* cost — which is not something either methodology can deliver; it's a
planning contradiction, not a process choice.

## A worked comparison: the same project, two ways

Imagine an insurance company needs a new claims-intake web form.

**As Waterfall**: Legal and Compliance sign off on every required field and
validation rule up front (this data feeds regulatory reporting, so scope is
genuinely fixed). The vendor delivers the form as a single release after 4
months, tested against the full signed-off spec, because there's no benefit
to a stakeholder seeing a half-built regulatory form early — it can't go
live until it's complete and compliant anyway.

**As Agile**: A separate internal team needs an employee expense-reporting
tool. Requirements are a rough sketch ("employees should be able to submit
and track expense reports"); nobody outside the company sees it, so
compliance risk is low, and internal users can start giving feedback the
moment a bare-bones version exists. The team ships a minimal "submit an
expense" flow in sprint 1, adds approval routing in sprint 2, adds receipt
photo upload in sprint 3 — each sprint's actual usage reshapes what gets
built next.

Same company, same general category of software ("an intake form"), opposite
methodology — because the fixed variable is different: regulatory scope in
the first case, an open-ended internal tool with no external deadline in the
second.

## The hybrid reality

Most real organizations run **both**, in different parts of the same
portfolio, or even the same team in different phases — an Agile delivery
team operating inside a Waterfall-style annual budget cycle with quarterly
stage gates is extremely common, and is not a contradiction; it's matching
each layer of the work to the kind of certainty available at that layer.
Level 3 of this course covers these hybrid models in depth.

## Exercise

Take two software projects — one you'd argue should be Waterfall, one you'd
argue should be Agile (real or invented, but be specific about the domain).
For each, name which of scope/schedule/cost is genuinely fixed and why, then
fill in one row of the head-to-head comparison table with a concrete detail
specific to that project (not a generic restatement of the table). Finally,
write two sentences describing what a hybrid version of one of your two
projects might look like — which parts would run Waterfall-style and which
would run Agile-style.
