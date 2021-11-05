# flux k8s runtimes
This is sample repository to manage multiple Kubernetes cluster with GitOps approach using [FluxCD](https://fluxcd.io/docs/). Beside this repo, there is another repo related to the implementation which belong to [service deployment manifest repository](https://github.com/ardikabs/flux-podinfo-manifesto).


## Feature implementation covered
* Onboarding new Kubernetes cluster a.k.a [bootstrap](./bootstrap)
* Multi Kubernetes cluster management.
* Modular, each service maintain their resources [example](s-cluster-01/apps/podinfo).
* Secret management using [SOPS](https://github.com/mozilla/sops). Example could be seen [here](./s-cluster-01/global/ssh-credentials).
* [Automate container image update](https://fluxcd.io/docs/guides/image-update/#configure-image-updates).
* [Rollback mechanism](https://fluxcd.io/docs/guides/image-update/#configure-image-updates).