# Bootstrap

We use SSH authentications to manage git access from flux, so ensure private/public key-pair is registered in your git repository.
```bash

$ cd ./bootstrap

# Upload gpg secret key
$ kustomize build . | kubectl apply -f -

# Bootstrap flux components
$ flux bootstrap git \
    --components-extra=image-reflector-controller,image-automation-controller \
    --url=ssh://git@github.com/ardikabs/flux-k8s-runtimes.git \
    --private-key-file=./id_rsa \
    --branch master \
    --path=s-cluster-01/
```