# ADR 0002: Pin production images by digest

## Status

Accepted

## Context

Mutable image tags make it harder to prove what was deployed, reproduce incidents, and reason about promotion between environments.

## Decision

Use immutable image digests for production-oriented manifests and examples.

## Consequences

- deployed artifacts are traceable to an exact build output
- rollback and incident review become more reliable
- teams need automation that updates digests during promotion

## Alternatives considered

- mutable tags such as `latest`
- environment tags without immutable digests
