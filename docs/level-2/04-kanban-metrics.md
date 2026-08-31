# 04 · Kanban Metrics (Cycle Time, Lead Time, CFD)

Level 1 covered WIP limits and pull as Kanban's mechanics. This module
covers the metrics that tell you whether those mechanics are actually
working — and how to read them without over-interpreting noise.

## The core measurements

| Metric | Definition | Answers |
|---|---|---|
| Lead time | Time from request created to delivered | "How long does a customer wait?" |
| Cycle time | Time from work started to delivered | "How long does work take once we commit to it?" |
| Throughput | Items completed per unit time | "How much do we ship?" |
| WIP | Items currently in progress | "How much is in flight right now?" |

Little's Law ties three of these together: **Average Cycle Time = Average
WIP ÷ Average Throughput**. This is the mathematical justification for WIP
limits — for a fixed throughput, lowering WIP mechanically lowers cycle
time. Teams that want faster delivery without hiring more people should
look at WIP first.

## Reading a Cumulative Flow Diagram (CFD)

A CFD stacks cumulative counts of items in each column (To Do, In Progress,
Done) over time.

| CFD signal | What to look for | What it means |
|---|---|---|
| Band width (vertical gap) | Widening "In Progress" band | Growing WIP — bottleneck forming |
| Band slope | Flattening "Done" line | Throughput dropping |
| Parallel bands | Consistent, near-parallel lines | Stable, predictable flow |
| Diverging bands | Gap between "In Progress" and "Done" widening steadily | Work is starting faster than it's finishing |

The horizontal distance between two bands at a given height is an
approximate cycle time; the vertical distance between bands at a given date
is WIP. A CFD makes bottlenecks visible weeks before they show up as missed
commitments.

## Cycle time distributions, not averages

Cycle time is rarely normally distributed — it has a long right tail from
outlier items (blocked stories, forgotten items). Reporting only the average
hides this. A cycle time scatterplot with 50th/85th/95th percentile lines is
more honest:

| Percentile | Use |
|---|---|
| 50th (median) | Typical item — good for day-to-day expectations |
| 85th | A reasonable "when will this likely be done" forecast |
| 95th | Worst-case planning for commitments to external stakeholders |

## A worked example

A support team's CFD shows the "In Review" band widening over three weeks
while "Done" flattens. Cycle time scatterplot confirms: median cycle time
rose from 3 to 6 days, driven entirely by items sitting in "In Review."
Investigation finds the team has one designated reviewer who's also doing
feature work. The fix: cap "In Review" WIP at 2, and rotate review duty
among three people instead of one. Four weeks later, the CFD bands run
parallel again and median cycle time returns to 3 days — a case of the
metric localizing a bottleneck that a status meeting alone hadn't
surfaced.

## Exercise

Using a real or invented set of 15 completed items with start and finish
dates, (1) compute median and 85th-percentile cycle time, (2) sketch (in
words or a simple table) what the CFD bands would look like if WIP were
rising, and (3) propose one WIP-limit change using Little's Law to justify
the expected effect on cycle time, and (4) state what you'd check two weeks
later to confirm the change worked.
