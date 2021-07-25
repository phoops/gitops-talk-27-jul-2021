# GitOps talk Jul 27

Each scenario is in a branch.
* `wild-west` for the first scenario where not everything is versioned and/or aligned

## Test setup
This POC can run in minikube:
```
minikube start
minikube addons enable ingress
minikube addons enable ingress-dns
```

## Wild-west
Not everything is versioned, in the example a secret has been created manually via "kubectl create" because of the fear of versioning secrets
```
kubectl create secret generic common-secret --from-literal=redis.host=redis.default.svc.cluster.local:6379
```

## Structuring the repository and saving the secrets
We'll use git-crypt.

The repository is divided into `services` that contain our (micro)services and `thirdparties` that will hold things like postgres or other software not made internally.

Each environment is a different kustomize overlay