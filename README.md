# Toolset

This helm chart bootstaps a complete toolset on a new cluster.
It deploys [argocd](https://argo-cd.readthedocs.io/) in a sensible default configuration which is then used to deploy several tools you will eventually need to support your apps on your cluster.

## Tools

Argocd is always installed.
All other tools can be disabled in the `values.yaml`

| tool                   | namespace | purpose |
|:-----------------------|:----------|:--------|
| argocd                 | argocd    | deploy and reconcile all applications on the cluster |
| nfs-subdir-provisioner | storage   | provide a storage class to provision pv for pvc      |

