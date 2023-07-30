# PlatformUI Helm Chart

This Helm chart deploys the PlatformUI application on a Kubernetes cluster.

## Prerequisites

- Kubernetes 1.16+
- Helm 3.1.0

## Chart details

| Parameter                 | Description                              | Default                                                |
| --------------------------| ---------------------------------------- | ------------------------------------------------------ |
| `deployment.replicaCount` | Number of PlatformUI replicas            | `1`                                                    |
| `deployment.image.repo`   | PlatformUI Image repository              | `501485087463.dkr.ecr.us-east-1.amazonaws.com/platformui` |
| `deployment.image.tag`    | PlatformUI Image tag                     | `v1.0`                                                 |
| `deployment.pullPolicy`   | PlatformUI Image pull policy             | `Always`                                               |
| `deployment.resources`    | CPU/Memory resource requests/limits      | Memory: `500Mi`, CPU: `500m`                           |
## Get Repo Info


```console
$ helm repo add platformui https://platformui.github.io/charts
$ helm repo update
$ helm install [RELEASE_NAME] platformui/platformui
$ helm uninstall [RELEASE_NAME]

