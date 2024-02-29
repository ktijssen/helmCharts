# Certificate

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

## Description

A Helm chart to generate individual certificate for Kubernetes

**Homepage:** <https://ktijssen.github.io/helmCharts>

## Source Code

* <https://github.com/ktijssen/helmCharts>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| ktijssen | <kevin.tijssen@gmail.com> |  |

## Usage

Please add the certificate repository before installing any chart provided by this repository:

```bash
helm repo add ktijssen https://ktijssen.github.io/helmCharts
helm repo update
```

### Installing the Chart

To install the chart with the release name certificate run:

```bash
helm install certificate ktijssen/certificate --version 1.0.0
```

After a few seconds, certificate should be running.

To install the chart in a specific namespace use following commands:

```bash
helm install certificate ktijssen/certificate --namespace certificate --create-namespace --version 1.0.0
```

> **Tip**: List all releases using `helm list`, a release is a name used to track a specific deployment

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| nameOverride | string | `""` |  |
| fullnameOverride | string | `""` |  |
| annotations | object | `{}` | Add annotations |
| dnsNames | list | `[]` | List of all the domain for this certificate |
| issuerRef.name | string | `""` | Name of the ClusterIssuer or Issuer |
| issuerRef.kind | string | `""` | Kind of the ClusterIssuer or Issuer |
| secretName | string | `""` | Name of the secret |
| commonName | string | `""` | Common name (Optional) |

