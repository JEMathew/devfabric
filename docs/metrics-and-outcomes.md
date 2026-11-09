# Metrics and Outcomes

| Question | Measure and interpretation |
| --- | --- |
| Where is onboarding slow? | In a pilot, time team registration to first successful staging and count handoffs and retries. Report the completion rate and waiting time for teams that stall. |
| Does self-service reduce waiting? | The workspace reports mean request-to-ready time on its simulation clock and successful provisions per completed attempt. A pilot would measure wall-clock waiting time by template and track rejected and failed requests separately. |
| Do teams return to a golden path? | For a pilot, divide weekly active teams using the path by eligible teams and distinguish first use from repeat use. The local self-service measure counts eligible developers with admitted requests divided by eligible developers. |
| Do agent tasks succeed without excess review? | The workspace computes success, straight-through completion, escalation, reviewer interventions and policy denial from admitted local task records. Pending work stays visible. See the task definitions below. |
| Can teams operate safely and affordably? | Inspect gate blocks, duplicate suppression and review coverage locally. For a pilot, measure recovery time and actual cost per eligible task beside completion. A sandbox cost estimate is illustrative. |
| Is the modeled value realized? | Business ROI multiplies projected annual adopted tasks by assumed hours released and hourly cost. Net value subtracts operating and enablement cost. ROI divides net value by total cost when defined. Validate volumes, elapsed time, cost and business outcomes with a pilot before reporting savings. |

The product's outcome measure is eligible reminders completed once with attributable policy evidence. Read it alongside skipped invoices, opt-outs and required reviews so a larger send count alone cannot stand in for customer value.

## How task rates are counted

Each admitted lookup or collection run contributes one task. A retry has its own ID. A review updates the existing task. Invalid input is counted separately. Eligible attempts exclude deliberate production probes and include pending, skipped, superseded and failed business tasks.

| Metric | Numerator | Denominator |
| --- | --- | --- |
| Agent task success | Completed tasks | Eligible attempts |
| Straight-through completion | Tasks completed without routing to human review | Eligible attempts |
| Human interventions per eligible task | Accepted task-level reviewer decisions | Eligible attempts |
| Escalation rate | Eligible tasks routed to review | Eligible attempts |
| Policy-denial rate | Policy-denied attempts | All admitted attempts, including production probes |

A completed collection run recorded a reminder. A completed scoped lookup passed its evaluator and received review approval. An empty denominator displays a dash. For example, one approved lookup plus one denied production probe gives 1/1 task success, 0/1 straight-through completion and 1/2 policy denial. These are synthetic workspace results.
