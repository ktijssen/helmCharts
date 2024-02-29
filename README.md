# Helm Charts
## Usage
[Helm](helm.sh) is required to use and operate these charts. You can add the Helm Repository like below:
[Helm](helm.sh) is required to use and operate these charts. You can add the Helm Repository like below:
```
helm repo add ktijssen https://ktijssen.github.io/helmCharts/
helm repo update
```

To list all the available charts.
```
helm searh repo ktijssen
```

Documentation and the default values.yaml can be found in relevant chart repository:

* [Certificates](https://github.com/ktijssen/helmCharts/tree/main/charts/certificates)
* [Keycloak Operator](https://github.com/ktijssen/helmCharts/tree/main/charts/keycloak-operator)
* [Keycloak Instance](https://github.com/ktijssen/helmCharts/tree/main/charts/keycloak-instance)