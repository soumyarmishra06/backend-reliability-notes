# Observability Over Metrics

Metrics are a great early warning system, but they rarely tell the whole story. You can see that something broke—error rates rose or latency spiked—but it’s often unclear what happened, where it started, or why.

In systems I’ve worked on, teams had many dashboards and alerts and still struggled to answer simple incident questions:
- What failed first?
- Which dependency caused user impact?
- How did a specific request move through the system?

## Metrics show symptoms, not stories

Metrics are excellent at signalling problems:
- error rates increasing
- latency percentiles worsening
- resource utilization spiking

But metrics usually show symptoms, not sequence or cause. They rarely explain how a failure propagated across services, so responders end up piecing together many dashboards under pressure.

## Logs and traces give the context

Structured logs and distributed traces are what let you tell the story behind the metrics. They help answer:
- which users or requests were affected
- where time was actually spent
- which dependency was slow or failing

When logs include consistent correlation IDs and traces reflect real dependency relationships, diagnosing incidents becomes much faster and more reliable.

## Design for observability, not just monitoring

Observability works best when treated as a design principle. Useful practices include:
- consistent correlation identifiers across services
- logs that record meaningful state transitions
- traces that map real calls between services
- a focused set of metrics tied to user impact

These practices reduce noisy dashboards and make on-call investigations more focused and effective.

## Trade-offs

Adding good observability takes effort: thoughtful schemas, clearer logging, and resisting the urge to log everything. Those costs are typically repaid by shorter incident resolution times and better operational understanding.

## Bottom line

Use metrics to detect that something is wrong; use logs and traces to understand why. Building systems that can "explain themselves" makes operations more reliable and teams more confident.
