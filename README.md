# Guestbook Helm Chart 

## Introduction

This is a Helm Chart for the deployment of the guestbook example provided here: https://kubernetes.io/docs/tutorials/stateless-application/guestbook/
<br />
# guestbook

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

A Helm Chart for guestbook example

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Wes Emery | we3kb.we@gmail.com |  |

## Requirements

| Repository | Name | Version |
|------------|------|---------|
|  | redis | 0.1.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| autoscaling.enabled | bool | `true` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| env[0].name | string | `"GET_HOSTS_FROM"` |  |
| env[0].value | string | `"dns"` |  |
| fullnameOverride | string | `"frontend"` |  |
| image.name | string | `"php-redis"` |  |
| image.repository | string | `"gcr.io/google_samples/gb-frontend:v5"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| labels.app | string | `"guestbook"` |  |
| labels.tier | string | `"frontend"` |  |
| matchLabels.app | string | `"guestbook"` |  |
| matchLabels.tier | string | `"frontend"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| replicaCount | int | `3` |  |
| resources.limits.cpu | string | `"100m"` |  |
| resources.limits.memory | string | `"128Mi"` |  |
| resources.requests.cpu | string | `"100m"` |  |
| resources.requests.memory | string | `"128Mi"` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |

----------------------------------------------
# redis

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Wes Emery | we3kb.we@gmail.com |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| fullnameOverride | string | `"redis-leader"` |  |
| image.name | string | `"redis-leader"` |  |
| image.repository | string | `"docker.io/redis:6.0.5"` |  |
| imagePullSecrets | list | `[]` |  |
| labels.app | string | `"redis"` |  |
| labels.role | string | `"leader"` |  |
| labels.tier | string | `"backend"` |  |
| matchLabels.app | string | `"redis"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `3` |  |
| resources.requests.cpu | string | `"100m"` |  |
| resources.requests.memory | string | `"100Mi"` |  |
| securityContext | object | `{}` |  |
| service.port | int | `6379` |  |
| service.targetport | int | `6379` |  |
| service.type | string | `"ClusterIP"` |  |

----------------------------------------------
