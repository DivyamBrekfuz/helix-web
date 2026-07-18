# ADR 0001: Covering index for dashboard aggregation

## Context
The new events partition key broke the composite index the dashboard aggregation relied on; p95 regressed to 4s.

## Decision
Add a covering index on (workspace_id, metric, bucket) and verify p95 < 800ms on the load test.

## Consequences
Dashboard p95 returns under target; no query-plan regressions.
