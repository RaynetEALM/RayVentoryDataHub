# Helm chart deployment templates for Kubernetes

Here one can find examples of different deployment strategies of Raynet One Data Hub to a kubernetes cluster using a helm chart.

## Basics

The simplest way to deploy the chart as is would be:

1. Make a copy of a chart to a location where helm/kubectl are available
2. Execute adjust 'values.yaml' file to have correct deployment configuration (or use defaults)
3. Run:

``` bash
helm install -f './<helm-char-directory>/values.yaml' '<deployment-name>' './<helm-char-directory>/'
```

for example

``` bash
helm install -f './datahub-mariadb-full/values.yaml' dh './datahub-mariadb-full/'
```

4. Wait some time for all services to go up and check logs of all deployed containers.
5. If there are issues, 
  5.1. uninstall the deployment:

``` bash
helm uninstall '<deployment-name>'
```

for example

``` bash
helm uninstall dh
```

  5.2 Adjust values
  5.3 Re-deploy the chart with new values
