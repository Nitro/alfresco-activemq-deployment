# Alfresco ActiveMQ Deployment

A Kubernetes deployment of [Apache ActiveMQ](http://activemq.apache.org/).

This chart is meant to be used with the [Alfresco Infrastructure chart](https://github.com/Alfresco/alfresco-infrastructure-deployment).

## Prerequisites

### Kubernetes Cluster

Please check the Anaxes Shipyard documentation on [running a cluster](https://github.com/Alfresco/alfresco-anaxes-shipyard/blob/master/docs/running-a-cluster.md).

### Persistence

Note that this chart is meant to be used with the [Alfresco Infrastructure chart](https://github.com/Alfresco/alfresco-infrastructure-deployment) and expects a persistent volume claim to be available, specified by the `persistence.existingClaim` value.

## Configuration
The following table lists some of the more important configurable parameters of the chart and their default values.

| Parameter                   | Description                                           | Default                 |
| --------------------------- | ----------------------------------------------------  | ----------------------- |
| `adminUser.username`        | The admin user username                               | `admin`                 |
| `adminUser.password`        | The admin user password                               | `admin`                 |
| `resources.requests.memory` | The minimum memory for the broker                     | `512Mi`                 |
| `resources.limits.memory`   | The maximum memory for the broker                     | `2048Mi`                |
| `persistence.existingClaim` | The name of the persistent volume claim to use        | `alfresco-volume-claim` |
| `nameOverride`              | An overriding name for the deployment and broker name | null                    |

