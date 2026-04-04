# Cloud Native GitOps Playbook

An opinionated, AI-readable knowledge repository for GitOps, platform operations, Kubernetes best practices, and shared web experience standards.

This repository is designed as a professional reference point for platform engineers and ops engineers who want a clean, defensible baseline for running Kubernetes through GitOps. It combines:

- human-readable best-practice guides
- machine-readable manifests for AI ingestion
- reusable repository and workload templates
- governance files that make the project portfolio-ready

## Why this exists

Modern platform work often gets scattered across wikis, tickets, local notes, and tribal knowledge. This repo turns that into a curated source of truth with two goals:

1. Capture operational best practices that align with cloud-native standards and common production expectations.
2. Make the content easy for AI systems to index, retrieve, and extend without losing structure.

## Scope

The current baseline focuses on:

- GitOps operating principles
- repository design for platform teams
- Kubernetes security and tenancy guardrails
- release and supply chain controls
- observability and operations patterns
- AI-ready content organization
- shared portfolio and product website design guidance

## Repository map

- [`docs/`](./docs) contains the narrative guidance
- [`knowledge/taxonomy.yaml`](./knowledge/taxonomy.yaml) defines the information model
- [`knowledge/manifests/`](./knowledge/manifests) contains machine-readable best-practice controls
- [`knowledge/decisions/`](./knowledge/decisions) contains Architecture Decision Records
- [`clusters/`](./clusters) contains example `dev` and `prod` environment composition
- [`templates/`](./templates) contains reusable GitOps and workload skeletons
- [`.github/PULL_REQUEST_TEMPLATE.md`](./.github/PULL_REQUEST_TEMPLATE.md) enforces contribution quality

## Opinionated principles

- Git is the source of truth for desired state.
- Platform configuration and application source code should be separated.
- Declarative delivery beats imperative drift-prone operations.
- Least privilege, multi-tenancy boundaries, and auditability come first.
- Immutable artifacts and traceability are required for reliable promotion.
- Documentation should be optimized for both engineers and AI retrieval.

## Best-practice sources

This repository is informed by primary documentation and community standards, including:

- OpenGitOps principles
- Kubernetes declarative configuration guidance
- Flux security guidance
- Argo CD operational best practices

See [`docs/references.md`](./docs/references.md) for source links.

## Suggested usage

Use this repo as:

- a portfolio repository for platform engineering work
- a starter for internal platform standards
- a knowledge base that AI assistants can query
- a reference when setting up new GitOps-managed clusters or services
- a central source of truth for shared website look and feel

## Progress on next steps

Recent improvements:

1. Added example environments in [`clusters/dev`](./clusters/dev) and [`clusters/prod`](./clusters/prod).
2. Added concrete ADRs in [`knowledge/decisions/`](./knowledge/decisions).
3. Kept repository validation in CI and extended the repo structure to support Kubernetes manifest validation.

Still a good future enhancement:

1. Add a `docs/` site generator such as MkDocs if you want a browsable handbook later.
