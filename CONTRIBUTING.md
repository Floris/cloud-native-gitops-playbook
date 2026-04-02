# Contributing

This repository is intentionally opinionated. Contributions should improve operational clarity, production readiness, and machine readability.

## Contribution rules

- Prefer primary sources such as Kubernetes, CNCF, Flux, Argo CD, or vendor documentation.
- Separate guidance from opinion. If something is contextual, say so explicitly.
- Keep examples declarative and GitOps-friendly.
- Avoid secrets, cluster-specific identifiers, and environment-specific hostnames.
- When adding new guidance, update [`knowledge/taxonomy.yaml`](./knowledge/taxonomy.yaml) if a new concept is introduced.
- Keep front matter, headings, and file naming consistent so AI tools can retrieve content reliably.

## Pull request expectations

- explain what changed
- explain why the change is a better practice
- reference at least one source for normative guidance when relevant
- call out any assumptions or trade-offs
