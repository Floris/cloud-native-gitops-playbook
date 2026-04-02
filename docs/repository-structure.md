# Repository Structure

## Preferred split

A strong GitOps estate usually separates:

- application source repositories
- platform configuration repositories
- cluster bootstrap repositories
- shared infrastructure modules

This separation improves auditability, ownership boundaries, and delivery flow. It also avoids noisy commit histories where application development changes are mixed with operational configuration updates.

## Practical layout

Recommended top-level patterns:

- `clusters/` for cluster-specific desired state
- `platform/` for shared controllers and services
- `apps/` for application deployment definitions
- `policies/` for admission, security, and governance controls
- `tenants/` for namespace or team-scoped onboarding artifacts

## Rules of thumb

- Keep environment overlays small and explicit.
- Favor composition with Kustomize or a consistent Helm strategy, not both everywhere without a rule.
- Separate reusable modules from environment instantiations.
- Do not let generated manifests become your primary authored source unless generation is tightly controlled.

