# CircleCI AKS GitOps
This repository contains a CircleCI pipeline definition for deploying containerized ASP.NET 5 sample application to the Kubernetes cluster in Azure Kubernetes Service (AKS).

# Info
The pipeline has two jobs (see [.circleci/config.yml](https://github.com/dawidborycki/CircleCI-AKS-GitOps/blob/main/.circleci/config.yml)):
1. azure-aks/create-cluster - this creates the cluster of name **aks-dotnet** (in the **eastus** region, and **aks-dotnet-rg** resource group).
2. create-deployment - deploys ASP.NET 5 sample app to the cluster using [all-in-one.yml](https://github.com/dawidborycki/CircleCI-AKS-GitOps/blob/main/k8s/all-in-one.yml)

# How to use it
1. Login to CircleCI using your GitHub account
2. Setup the project in CircleCI
3. Provide login credentials to Azure. To do so provide user or service principal. Use CircleCI's project environmental variables for that
