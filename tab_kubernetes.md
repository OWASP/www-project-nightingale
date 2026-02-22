---
title: Kubernetes
displaytext: Kubernetes
layout: col-sidebar
tab: true
tags: Nightingale
order: 4
level: 2
type: tool
---

# Helm Package for Nightingale 🦉

Nightingale is an open-source tool that aims to address this problem by providing a ready-to-use environment for pentesters.

This chart bootstraps a Nightingale deployment on a Kubernetes cluster using the Helm package manager.

Let's Open Feathers in the Cloud: Nightingale Meets Kubernetes! 🌥️

## Prerequisites

- Kubernetes 1.19+
- Helm 3.7+

## Get Repository Info

To add the Nightingale Helm repository and update it, run the following commands:

```helm
helm repo add nightingale https://rajanagori.github.io/Nightingale
helm repo update
```

## Install/Upgrade Chart

Install the Nightingale chart with the release name `nightingale` in the `nightingale` namespace.

```helm
helm upgrade --install nightingale nightingale/nightingale -n nightingale --create-namespace
```

## Install/Upgrade the chart using just one command

This command will add the Nightingale Helm repository, update it, and install the Nightingale chart with the release name `nightingale` in the `nightingale` namespace.
```helm
helm upgrade --install nightingale nightingale --repo https://rajanagori.github.io/Nightingale -n nightingale --create-namespace
```

## Values

The provided selection is a table of configuration values typically used in a Kubernetes deployment. Each row represents a different configuration option.

- `namespaceOverride` is a string that can be used to override the default namespace in which the Kubernetes resources are deployed.
- `replicaCount` is an integer that specifies the number of pod replicas to create.
- `image.repository`, `image.tag`, and `image.pullPolicy` are strings that define the Docker image to use for the pods, the tag of the image, and the policy for pulling the image, respectively.
- `strategy.type` and `strategy.rollingUpdate.maxUnavailable` and `strategy.rollingUpdate.maxSurge` are used to define the update strategy for the deployment. The `RollingUpdate` strategy gradually replaces old pods with new ones.
- `podSecurityContext` and `securityContext` are objects that define the security contexts for the pods and containers, respectively.
- `resources.limits.cpu`, `resources.limits.memory`, `resources.requests.cpu`, and `resources.requests.memory` are used to set the CPU and memory resource limits and requests for the containers in the pods.
- `volumes` and `volumeMounts` are lists that define the volumes to create and where to mount them in the containers, respectively.
- `tolerations` is a list that defines the tolerations for the pods.
- `affinity` is an object that defines the affinity/anti-affinity rules for the pods.
- `service.type` and `service.port` are used to define the type of service to create and the port it should expose.
- `ingress.enabled` is used to define the ingress resource if `ingress.enabled` is set to true. This includes the ingress class name, annotations, host settings, and TLS settings.
- `autoscaling` related keys are used to define the horizontal pod autoscaler resource if `autoscaling.enabled` is set to true. This includes the minimum and maximum number of pod replicas and the CPU and memory utilization thresholds for scaling.

| Key                         | Type   | Default                 |
|-----------------------------|--------|-------------------------|
| namespaceOverride           | String | ""                      |
| replicaCount                | Int    | 1                       |
| image.repository            | String | ghcr.io/rajanagori/nightingale |
| image.tag                   | String | stable                  |
| image.pullPolicy            | String | IfNotPresent            |
| strategy.type               | String | RollingUpdate           |
| strategy.rollingUpdate.maxUnavailable | String | 25%                |
| strategy.rollingUpdate.maxSurge | String | 25%                   |
| podSecurityContext          | Object | {}                      |
| securityContext             | Object | {}                      |
| resources.limits.cpu        | String | 100m                    |
| resources.limits.memory     | String | 200Mi                   |
| resources.requests.cpu      | String | 50m                     |
| resources.requests.memory   | String | 100Mi                   |
| volumes                     | List   | []                      |
| volumeMounts                | List   | []                      |
| tolerations                 | List   | []                      |
| affinity                    | Object | {}                      |
| service.type                | String | ClusterIP               |
| service.port                | Int    | 80                      |
| ingress.enabled             | Bool   | false                   |
| ingress.ingressClassName    | String | nginx                   |
| ingress.annotations         | Object | {}                      |
| ingress.host.enabled        | Bool   | false                   |
| ingress.host.name           | String | ""                      |
| ingress.tls.enabled         | Bool   | false                   |
| autoscaling.enabled         | Bool   | false                   |
| autoscaling.minReplicas     | Int    | 1                       |
| autoscaling.maxReplicas     | Int    | 10                      |
| autoscaling.cpuUtilization  | Int    | 80                      |
| autoscaling.memoryUtilization | Int   | 95                      |

## Uninstall Chart
To uninstall the Nightingale chart, run the following command:
```helm
helm uninstall nightinfgale -n nightingale
```

