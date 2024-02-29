# Keycloak-Operator

![Version: 23.0.6](https://img.shields.io/badge/Version-23.0.6-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 23.0.6](https://img.shields.io/badge/AppVersion-23.0.6-informational?style=flat-square)

## Description

A Helm chart for Kubernetes

**Homepage:** <https://ktijssen.github.io/helmCharts>

## Source Code

* <https://github.com/ktijssen/helmCharts>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| ktijssen | <kevin.tijssen@gmail.com> |  |

## Usage

Please add the keycloak-operator repository before installing any chart provided by this repository:

```bash
helm repo add ktijssen https://ktijssen.github.io/helmCharts
helm repo update
```

### Installing the Chart

To install the chart with the release name keycloak-operator run:

```bash
helm install keycloak-operator ktijssen/keycloak-operator --version 23.0.6
```

After a few seconds, keycloak-operator should be running.

To install the chart in a specific namespace use following commands:

```bash
helm install keycloak-operator ktijssen/keycloak-operator --namespace keycloak-operator --create-namespace --version 23.0.6
```

> **Tip**: List all releases using `helm list`, a release is a name used to track a specific deployment

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| namespaceOverride | string | `""` | Override the deployment namespace; defaults to .Release.Namespace |

