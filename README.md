# Helm NGINX Chart

You need to provide these attributes.

## Prerequisites

- Kubernetes 1.19+
- Helm 3.2.0+

## Installing the Chart

To install the chart with the release name `my-release`:

```bash
$ helm repo add nginx ./edu-helm-nginx-chart
$ helm install my-nginx ./edu-helm-nginx-chart
```

## Parameters

| Name                 | Description                                                                           | Value          |
|----------------------|---------------------------------------------------------------------------------------|----------------|
| `nameOverride`       | String to partially override nginx.fullname template (will maintain the release name) | `""`           |
| `image.registry`     | NGINX image registry                                                                  | `docker.io`    |
| `image.repository`   | NGINX image repository                                                                | `nginx`        |
| `image.tag`          | NGINX image tag (immutable tags are recommended)                                      | `1.20.2`       |
| `image.pullPolicy`   | NGINX image pull policy                                                               | `IfNotPresent` |
| `image.pullSecrets`  | Specify docker-registry secret names as an array                                      | `[]`           |
| `image.debug`        | Set to true if you would like to see extra information on logs                        | `false`        |
| `replicaCount`       | Number of NGINX replicas to deploy                                                    | `1`            |
| `resources.limits`   | The resources limits for the NGINX container                                          | `{}`           |
| `resources.requests` | The requested resources for the NGINX container                                       | `{}`           |
