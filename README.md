# GitOps talk Jul 27

Each scenario is in a branch.
* `wild-west` for the first scenario where not everything is versioned and/or aligned
* `kustomize-bundle` for a structured repository (per-service and per-environment) and versioned secrets
* `fully-automated` contains the above and a complete automation with ArgoCD, RBAC example and integration with OIDC
