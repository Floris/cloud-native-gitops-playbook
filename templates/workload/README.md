# Workload Template

This starter intentionally keeps the workload example simple while encoding a safer default posture:

- explicit resource requests and limits
- non-root execution
- read-only root filesystem
- probes and rolling strategy
- environment overlays with Kustomize

