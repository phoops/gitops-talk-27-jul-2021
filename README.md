# GitOps talk Jul 27

This repository is in support of [this Codemotion event](https://live.codemotion.com/devcast/devops-serie-summer21?fbclid=IwAR22OEfLStAPefjt_3WUMVzb23kq7jND15fA-V-kAs7ms-M_0Sx92YHlEng)

Each scenario is in a branch.
* `wild-west` for the first scenario where not everything is versioned and/or aligned
* `kustomize-bundle` for a structured repository (per-service and per-environment) and versioned secrets
* `fully-automated` contains the above and a complete automation with ArgoCD, RBAC example and integration with OIDC
