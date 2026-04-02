# Kubernetes Security Baseline

## Minimum baseline

Every platform baseline should define secure defaults for workloads and namespaces.

Recommended focus areas:

- Pod Security Standards or equivalent admission enforcement
- namespaced least-privilege RBAC
- network policy defaults
- image provenance and trusted registries
- secret management through external secret systems or sealed workflows
- resource requests and limits

## Namespace expectations

Each namespace should have:

- an owner
- clear environment classification
- quota and limit ranges where appropriate
- baseline security labels
- logging and metrics enabled by default

## Workload expectations

Every deployment should aim to include:

- non-root containers unless there is a justified exception
- read-only root filesystem where possible
- explicit probes
- pinned images by digest for promotion-sensitive environments
- minimal service account permissions

