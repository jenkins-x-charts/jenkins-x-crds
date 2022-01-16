# jenkins-x-crds chart

Custom Resource Definitions for Jenkins X

To regenerate the crd manifests:

- Clone [jx-api](https://github.com/jenkins-x/jx-api) repository outside this repository
- Run `make manifests` inside the jx-api repo
- Copy the manifests from config/crd/bases folder in jx-api into the templates folder in this repository
- Manually add `preserveUnknownFields: false` in the spec section of the templates. This is required for crds migrating from v1beta1 to v1
