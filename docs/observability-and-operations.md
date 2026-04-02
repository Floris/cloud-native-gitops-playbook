# Observability And Operations

## Golden operational baseline

A GitOps platform is only reliable if reconciliation, workload health, and platform health are observable.

Track at least:

- GitOps reconciliation status and drift
- workload readiness and rollout failures
- cluster capacity and saturation
- policy violations
- deployment frequency and rollback events

## Operational patterns

- Expose GitOps controller alerts for reconciliation failures.
- Standardize labels and annotations so logs, metrics, and dashboards remain queryable.
- Include runbook links in alerts.
- Prefer SLO-driven alerting over raw symptom spam.

## Incident handling

If an imperative fix is required during an incident:

1. document the action
2. reconcile the intended state back into Git
3. review why the platform path was insufficient
