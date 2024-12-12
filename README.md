[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

# Helm Repo

## Usage

1. Add or update a Helm chart: push your source code of Helm chart under `charts/<your chart>`
1. New release will be created by [GitHub Actions]
1. Add this helm chart repo to your helm client configuration
    ```
    helm repo add azurecloudops https://azurecloudops.github.io/helm
    helm repo update
    ```
1. Update repo and search
    ```
    helm search repo nakamasato
    NAME                     	CHART VERSION	APP VERSION	DESCRIPTION
    azurecloudops/helm-example  	0.1.0        	v0.0.1     	Simple API application.
    azurecloudops/mysql-operator	0.1.0        	v0.2.0     	A Helm chart for Kubernetes
    ```
1. Install
    ```
    helm install example-from-my-repo azurecloudops/helm-example
    ```
1. Upgrade (optional)
    ```
    helm upgrade example-from-my-repo azurecloudops/helm-example --set xxx=aaa
    ```
1. Uninstall
    ```
    helm uninstall example-from-my-repo
    ```

## Setup

follow [chart-releaser Action](https://github.com/marketplace/actions/helm-chart-releaser#pre-requisites)

