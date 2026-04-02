# GitOps Principles

## Core model

GitOps works best when Git is treated as the authoritative declaration of desired state and reconciliation is continuous, observable, and reversible.

The OpenGitOps model is especially useful because it anchors GitOps in four practical ideas:

- declarative system descriptions
- versioned and immutable desired state
- automated pull-based reconciliation
- continuous drift detection and correction

## Operating guidance

- Store deployment intent in Git, not in ad hoc runbooks or shell history.
- Use pull-based agents in the cluster so deployment credentials do not need to live in CI systems.
- Require reviewable pull requests for production changes.
- Promote immutable artifacts across environments instead of rebuilding per environment.
- Keep emergency imperative actions exceptional, documented, and reconciled back into Git quickly.

## What good looks like

- Every production change has a Git commit, reviewer trail, and rollback path.
- Clusters converge automatically to the declared target state.
- Drift is visible and corrected or explicitly acknowledged.
- Environment differences are intentional and minimal.

