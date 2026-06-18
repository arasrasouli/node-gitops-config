# node-gitops-config

GitOps config repo — the source of truth ArgoCD watches.

- `namespace.yaml`  — the `demo` namespace
- `deployment.yaml` — how the app runs (image tag, replicas, health probes)
- `service.yaml`    — exposes the app

ArgoCD syncs the `demo` namespace to match these manifests.
The app's CI updates the image tag in `deployment.yaml` on each release.
