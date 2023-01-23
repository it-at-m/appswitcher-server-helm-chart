[![Contributors][contributors-shield]][contributors-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

# appswitcher-server-helm-chart

## Introduction

This chart bootstraps a [appswitcher-server](https://github.com/it-at-m/appswitcher-server) deployment on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

This documentation is rendered from the `main` branch.

## Add Helm repo

```bash
helm repo add appswitcher-server https://it-at-m.github.io/appswitcher-server-helm-chart
```

## Installing the Chart

Install this chart using:

```bash
helm install appswitcher-server appswitcher-server/appswitcher-server --values values.yaml
```

The command deploys appswitcher-server on the Kubernetes cluster with some default configuration. The [values](#values) section lists the parameters that can or **must** be configured during installation.

## Values

:construction: TODO document custom values

| Key                                     | Type   | Default                      | Description                             |
| --------------------------------------- | ------ | ---------------------------- | --------------------------------------- |
| image.imagePullSecrets                  | list   | `[]`                         | Image pull secrets specification        |
| image.pullPolicy                        | string | `"IfNotPresent"`             | Image pull policy                       |
| image.repository                        | string | `"itatm/appswitcher-server"` | Image to use for deploying              |
| image.tag                               | string | `""`                         | Image tag                               |
| ingress.annotations                     | object | `{}`                         |                                         |
| ingress.className                       | string | `""`                         |                                         |
| ingress.enabled                         | bool   | `false`                      | Enable ingress                          |
| ingress.hosts                           | list   | `[]`                         |                                         |
| ingress.tls                             | list   | `[]`                         |                                         |
| nameOverride                            | string | `""`                         | Override chart name                     |
| podSecurityContext                      | object | `""`                         | Security Context                        |
| service.annotations                     | object | `{}`                         | Service annotations                     |
| service.port                            | int    | `3000`                       | Service pot                             |
| service.type                            | string | `"ClusterIP"`                | Service type                            |
| serviceAccount.annotations              | object | `{}`                         | Service account annotations             |
| serviceAccount.create                   | bool   | `true`                       | Create service account                  |
| serviceAccount.name                     | string | `""`                         | Service account name                    |
| extraEnvVars                            | list   | `[]`                         | Extra environment variables             |
| extraVolumes                            | list   | `[]`                         | Extra volumes                           |
| extraVolumeMounts                       | list   | `[]`                         | Extra volumeMounts for the pods         |
| route.enabled                           | bool   | `false`                      | Create OpenShift route                  |
| route.annotations                       | object | `{}`                         | Route annotations                       |
| route.host                              | string | `""`                         | Route host                              |
| route.path                              | string | `""`                         | Route path                              |
| route.wildcardPolicy                    | string | `"None"`                     | Route wildcard policy                   |
| route.tls.termination                   | string | `"Edge"`                     | Route tsl termination                   |
| route.tls.insecureEdgeTerminationPolicy | string | `"Redirect"`                 | Route tls insecureEdgeTerminationPolicy |
| route.tls.key                           | string | `""`                         | Route tls key                           |
| route.tls.certificate                   | string | `""`                         | Route tls certificate                   |
| route.tls.caCertificate                 | string | `""`                         | Route tls ca certificate                |
| route.tls.destinationCACertificate      | string | `""`                         | Route tls destination ca certificate    |

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/it-at-m/appswitcher-server-helm-chart.svg?style=for-the-badge
[contributors-url]: https://github.com/it-at-m/appswitcher-server-helm-chart/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/it-at-m/appswitcher-server-helm-chart.svg?style=for-the-badge
[forks-url]: https://github.com/it-at-m/appswitcher-server-helm-chart/network/members
[stars-shield]: https://img.shields.io/github/stars/it-at-m/appswitcher-server-helm-chart.svg?style=for-the-badge
[stars-url]: https://github.com/it-at-m/appswitcher-server-helm-chart/stargazers
[issues-shield]: https://img.shields.io/github/issues/it-at-m/appswitcher-server-helm-chart.svg?style=for-the-badge
[issues-url]: https://github.com/it-at-m/appswitcher-server-helm-chart/issues
[license-shield]: https://img.shields.io/github/license/it-at-m/appswitcher-server-helm-chart.svg?style=for-the-badge
[license-url]: https://github.com/it-at-m/appswitcher-server-helm-chart/blob/main/LICENSE
