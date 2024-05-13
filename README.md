# Toolset

This helm chart bootstaps a complete toolset on a new cluster.
It deploys [argocd](https://argo-cd.readthedocs.io/) in a sensible default configuration which is then used to deploy several tools you will eventually need to support your apps on your cluster.

## Tools

Argocd is always installed.
All other tools can be disabled in the `values.yaml`

| tool                                                                                         | namespace | purpose |
|:---------------------------------------------------------------------------------------------|:----------|:--------|
| [argocd](https://argo-cd.readthedocs.io/)                                                    | argocd    | deploy and reconcile all applications on the cluster |
| [nfs-subdir-provisioner](https://github.com/kubernetes-sigs/nfs-subdir-external-provisioner) | storage   | provide a storage class to provision pv for pvc      |
| [zalando postgres operator](https://opensource.zalando.com/postgres-operator/)               | postgres-operator | deploy & manage postgres databases           |
| [lgtm-distributed](https://github.com/grafana/helm-charts/tree/main/charts/lgtm-distributed) | observability | complete grafana observability stack ([loki](https://grafana.com/oss/loki/), [grafana](https://grafana.com/oss/grafana/), [tempo](https://grafana.com/oss/tempo/), [mimir](https://grafana.com/oss/mimir/)) |
