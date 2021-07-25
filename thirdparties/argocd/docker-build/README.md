## Custom argocd build with git-crypt

We need to add `git-crypt` in our argocd image, in order to decrypt the files in this repository.s

Basically we mount a secret as a volume with the gpg key, so the argo instance can decrypt the repo before applying the files.

The `Dockerfile` in this directory contains the custom docker image. Remember to update the image as new versions of argo will be released.

## Build docker-image

Refer to https://argoproj.github.io/argo-cd/operator-manual/custom_tools/

Please build and push the image with a tag equals to the argocd version we are using.

For example `v2.0.0-0.0.1` so we can recognize the argo version involved in the custom image.

```sh
    docker build -t locura/argocd-custom-git-crypt:<argocd-version>-<custom-image-version> .
```

The version of the custom image is set on the `kustomization` of base.