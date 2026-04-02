# Platform Operating Model

## Team responsibilities

A mature platform or ops team acts as an enablement function, not a manual deployment queue.

Useful responsibility boundaries include:

- platform team owns shared controllers, guardrails, tenancy models, and paved roads
- application teams own service-level configuration within defined policy boundaries
- security owns control objectives and policy review, in partnership with platform engineering

## Engineering practices

- Define a platform contract for what every workload must provide.
- Automate onboarding for namespaces, quotas, policies, and observability hooks.
- Standardize release promotion through pull requests and environment promotion workflows.
- Treat cluster access as a last resort, not a default operating mechanism.

## Anti-patterns

- Every team gets broad cluster-admin style access.
- Production fixes happen directly through kubectl without follow-up reconciliation.
- Platform standards live only in slides, tickets, or tribal memory.

