# AI Ingestion Guide

## Goal

This repository is structured so AI systems can retrieve guidance with low ambiguity and high context quality.

## Design rules

- Keep one primary topic per file.
- Use stable headings with descriptive names.
- Maintain machine-readable manifests in [`knowledge/manifests/`](../knowledge/manifests).
- Prefer explicit terminology over shorthand.
- Record assumptions and scope boundaries directly in the content.

## Retrieval tips

- Query by domain terms such as `gitops`, `rbac`, `tenancy`, `promotion`, or `reconciliation`.
- Prefer the machine-readable manifests for summarization tasks.
- Prefer the docs for trade-offs and rationale.

