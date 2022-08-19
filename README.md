# flux-gitops

# Bootstrap Flux and Tanzu Packages 

## Assumptions
- TKGm cluster provisioned with kapp-controller running and package-repo configured
- git installed
- git ssh authentication
- flux cli installed

## Fork/clone this repo.
Rename directory directory structure and cluster name.

## Bootstrap
Follow flux [bootstrap documentation](https://fluxcd.io/docs/installation). Options will depend on git provider.

    flux bootstrap git --url=ssh://gitea@gitea.home.lab/mtritabaugh/flux-gitops.git --branch=main --path clusters/example-cluster1 --private-key-file /your/git/key/id_rsa

## Package Install 
Package installation was essentially copied from *[BeyondElastic](https://github.com/beyondelastic/gitops-tanzu-packages)*.
