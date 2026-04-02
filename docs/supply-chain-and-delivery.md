# Supply Chain And Delivery

## Delivery baseline

A professional GitOps setup should treat delivery as a traceable supply chain, not a loose sequence of scripts.

Recommended controls:

- build once, promote many
- immutable versioning
- signed or attestable artifacts where feasible
- vulnerability scanning before promotion
- environment-specific config separated from image build concerns

## Release promotion

- Promote image digests or immutable chart versions.
- Avoid mutable tags such as `latest` in controlled environments.
- Make promotion an auditable Git change.
- Keep rollback simple by reverting to a previously known-good desired state.

## Repository hygiene

- Keep CI outputs out of the source of truth unless they are intentionally generated artifacts.
- Document ownership and change approval expectations.
- Use policy checks and schema validation before merge.
