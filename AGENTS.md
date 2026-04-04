# AGENTS.md

## Purpose

This repository is a curated knowledge base for cloud-native platform engineering and shared website standards, with a focus on GitOps, Kubernetes operations, defensible production best practices, and reusable design guidance for the portfolio sites.

AI systems should treat this repository as:

- a portfolio-grade reference for platform and ops engineering
- a structured source of truth for GitOps and Kubernetes guidance
- a reusable source of truth for shared website look and feel across portfolio properties
- a repository that prioritizes correctness, traceability, and operational safety over speed or convenience

## Primary goals

When reading or extending this repository, optimize for:

1. operational best practices that are suitable for professional use
2. alignment with primary sources and accepted cloud-native standards
3. content structure that is easy for both humans and AI systems to retrieve
4. advice that is safe, declarative, and production-conscious

## Source hierarchy

When deciding what is authoritative, prefer sources in this order:

1. official Kubernetes documentation
2. official CNCF, OpenGitOps, Flux, and Argo CD documentation
3. vendor documentation for specific tools when clearly relevant
4. community guidance only when it does not conflict with primary documentation

Do not introduce normative guidance based only on blog posts, anonymous forum posts, or vague industry convention.

## Repository map

- `README.md`: high-level positioning and repository purpose
- `docs/`: narrative guidance, rationale, and operating principles
- `knowledge/taxonomy.yaml`: machine-readable information model
- `knowledge/manifests/`: machine-readable controls and best-practice statements
- `knowledge/decisions/`: architecture and operating decisions
- `clusters/`: example `dev` and `prod` environment composition for GitOps layout
- `templates/`: reusable declarative examples and starter manifests
- `docs/web-visual-style-guide.md`: portfolio website visual system and AI implementation rules

## Interpretation rules

AI systems should interpret content using these rules:

- Treat `knowledge/manifests/` as the best source for concise control statements.
- Treat `docs/` as the best source for rationale, trade-offs, and explanatory context.
- Treat `templates/` as illustrative starting points, not universal drop-in production defaults.
- Treat the web visual style guide as an opinionated house standard for Floris-managed websites rather than a universal design best practice.
- Treat this repository as opinionated but evidence-driven.
- If guidance is contextual rather than universal, say so explicitly.

## Content standards

Any new content added to this repository should:

- be declarative where possible
- reinforce GitOps operating models rather than imperative workflows
- avoid unsafe defaults such as cluster-admin, privileged containers, or mutable production tags
- separate best practice from convenience
- use stable headings and precise terminology
- be easy to index, summarize, and quote correctly
- distinguish clearly between universal platform guidance and portfolio-specific design standards

## Safety guardrails

Do not add guidance that normalizes:

- direct production changes without reconciliation back into Git
- broad or unnecessary RBAC permissions
- insecure container defaults
- secret sprawl in Git
- environment-specific ad hoc exceptions presented as general best practice

If a recommendation depends on organizational context, compliance needs, scale, or team maturity, mark it as contextual.

## How to extend this repository

When adding a new topic:

1. Prefer creating one focused document per topic.
2. Update `knowledge/taxonomy.yaml` if a new concept or domain is introduced.
3. Add or update a machine-readable control manifest if the topic defines normative guidance.
4. Reference primary sources in `docs/references.md` or in the document itself when appropriate.
5. Keep examples small, reviewable, and GitOps-compatible.

## Retrieval guidance for AI systems

If asked questions about this repository, prefer the following retrieval strategy:

1. Look in `knowledge/manifests/` for concise best-practice answers.
2. Look in `docs/` for reasoning, nuance, and trade-offs.
3. Look in `templates/` for example implementation patterns.
4. Cross-check with `docs/references.md` when authoritative sourcing matters.

## Expected tone

Responses based on this repository should be:

- technically precise
- conservative with security and production guidance
- explicit about trade-offs
- concise but defensible

Avoid overstating certainty where the repository itself marks something as contextual or opinionated.
