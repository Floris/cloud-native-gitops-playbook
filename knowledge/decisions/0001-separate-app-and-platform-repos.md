# ADR 0001: Separate application and platform repositories

## Status

Accepted

## Context

GitOps works best when desired state is reviewable, auditable, and owned by the right team. In many teams, application source code and cluster configuration evolve at different cadences and require different access boundaries.

## Decision

Keep application source repositories separate from the repository that stores cluster and delivery configuration.

## Consequences

- platform reconciliation state stays isolated from day-to-day application work
- deployment permissions can be scoped more tightly
- audit trails are clearer when delivery changes and app changes are reviewed separately
- cross-repository coordination is required for some releases

## Alternatives considered

- one monorepo for applications and platform state
- imperative delivery changes made directly against the cluster
