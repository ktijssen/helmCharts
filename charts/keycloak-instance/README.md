# keycloak-instance

![Version: 0.0.1](https://img.shields.io/badge/Version-0.0.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 23.0.6](https://img.shields.io/badge/AppVersion-23.0.6-informational?style=flat-square)

A Helm chart for Kubernetes

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| file://../keycloak-operator | keycloak-operator | 23.0.6 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| additionalOptions | object | `{}` |  |
| customImage.registry | string | `""` | Custom keycloak-instance image host registry |
| customImage.repository | string | `""` | Custom keycloak-instance  image repository |
| customImage.tag | string | `""` | OCustom keycloak-instance  image tag |
| db.database | string | `"keycloak"` | Sets the database name of the default JDBC URL of the chosen vendor. If the `url` option is set, this option is ignored. |
| db.host | string | `"localhost"` | Sets the hostname of the default JDBC URL of the chosen vendor. If the `url` option is set, this option is ignored. |
| db.passwordSecret | object | `{}` | The reference to a existing secret holding the password of the database user. |
| db.poolInitialSize | string | `""` | The initial size of the connection pool. |
| db.poolMaxSize | string | `""` | The maximum size of the connection pool. |
| db.poolMinSize | string | `""` | The minimal size of the connection pool. |
| db.port | string | `"5432"` | Sets the port of the default JDBC URL of the chosen vendor. If the `url` option is set, this option is ignored. |
| db.schema | string | `""` | The database schema to be used. |
| db.url | string | `""` | For instance, if using 'postgres', the default JDBC URL would be 'jdbc:postgresql://localhost/keycloak'. |
| db.usernameSecret | object | `{}` | The reference to a existing secret holding the username of the database user. |
| db.vendor | string | `"postgres"` | Possible options: dev-file (default), dev-mem, mariadb, mssql, mysql, oracle, postgres |
| dbCredentialsSecret | object | `{"create":false}` | Create a Secret for the database credetials instead of using a Secret that already exists |
| features | object | `{"disabled":[],"enabled":[]}` | In this section you can configure Keycloak features, which should be enabled/disabled. |
| fullnameOverride | string | `""` |  |
| hostname.admin | string | `""` | The hostname for accessing the administration console. |
| hostname.adminUrl | string | `""` | Set the base URL for accessing the administration console, including scheme, host, port and path |
| hostname.hostname | string | `"localhost"` | Hostname for the Keycloak server. |
| hostname.strict | bool | `false` | Disables dynamically resolving the hostname from request headers. |
| hostname.strictBackchannel | bool | `false` | By default backchannel URLs are dynamically resolved from request headers to allow internal and external applications. |
| http.httpEnabled | bool | `true` | Enables the HTTP listener. |
| http.httpPort | string | `"8080"` | The used HTTP port. |
| http.httpsPort | string | `"8443"` | The used HTTPS port. |
| http.tlsSecret | string | `""` | A secret containing the TLS configuration for HTTPS. |
| imagePullSecrets | list | `[]` | Secret(s) that might be used when pulling an image from a private container image registry or repository. |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `"nginx"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"keycloak-instance.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| ingress.tls | list | `[]` |  |
| instances | int | `1` | Number of Keycloak instances in HA mode. Default is 1. |
| nameOverride | string | `""` |  |
| transaction.xaEnabled | bool | `false` | Determine whether Keycloak should use a non-XA datasource in case the database does not support XA transactions. |
| unsupported | object | `{}` | Use at your own risk and open an issue with your use-case if you don't find an alternative way. |
| keycloak-operator | | | |
| keycloak-operator.enabled | bool | `false` | Install Keycloak Operator |
| keycloak-operator.namespaceOverride | string | `""` | Override the deployment namespace; defaults to .Release.Namespace |
