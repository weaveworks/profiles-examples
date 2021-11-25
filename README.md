# profiles-examples
This repository is used to host a dummy Helm Repository. You can checkout the `gh-pages` branch to find the HelmRepository files.
You can access this repo as a Helm Repository via `https://weaveworks.github.io/profiles-examples`

IMPORTANT: This repo is used in tests in github.com/weaveworks/weave-gitops. When making a change to this repository
that might break the tests, please ensure you have a PR ready to fix them in github.com/weaveworks/weave-gitops.

Example `HelmRepository` resource:
```
apiVersion: source.toolkit.fluxcd.io/v1beta1
kind: HelmRepository
metadata:
  name: weaveworks-charts
  namespace: test-namespace
spec:
  interval: 1m0s
  timeout: 1m0s
  url: https://weaveworks.github.io/profiles-examples
```
