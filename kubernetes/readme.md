# Helm Chart Deployment Templates for Kubernetes

This repository provides examples of different deployment strategies for deploying the **Raynet One Data Hub** to a Kubernetes cluster using a Helm chart.

## Basics

The simplest way to deploy the chart is as follows:

1. **Prepare the Chart**  
   Copy the Helm chart to a location where `helm` and `kubectl` are available.

2. **Configure Deployment**  
   Edit the `values.yaml` file to have the correct deployment configuration, or use the default settings.

3. **Deploy the Chart**  
   Run the following command to install the chart:

       helm install -f './<helm-chart-directory>/values.yaml' '<deployment-name>' './<helm-chart-directory>/'

   For example:

       helm install -f './datahub-mariadb-full/values.yaml' dh './datahub-mariadb-full/'

4. **Monitor Deployment**  
   Wait for all services to start and check the logs of all deployed containers.

5. ***Troubleshooting***  
   If there are any issues:

   5.1 Uninstall the deployment:  

       helm uninstall '<deployment-name>'

   For example:

       helm uninstall dh

   5.2 Adjust the values in values.yaml as needed.

   5.3 Re-deploy the chart with the updated values.