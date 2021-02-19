# Manage Kubernetes Resources via Terraform
source: [Hashicorp tutorials](https://learn.hashicorp.com/tutorials/terraform/kubernetes-provider?in=terraform/kubernetes)  
In this tutorial, you will learn how to interact with Kubernetes using Terraform, by scheduling and exposing a NGINX deployment on a Kubernetes cluster.

- Install kind in a windows machine:   
 `choco install kind`
- `curl https://raw.githubusercontent.com/hashicorp/learn-terraform-deploy-nginx-kubernetes-provider/master/kind-config.yaml --output kind-config.yaml`
- Create a kind Kubernetes cluster: `kind create cluster --name terraform-learn --config kind-config.yaml`
- Verify that your cluster exists by listing your kind clusters: `kind get clusters`  
- Point kubectl to interact with this cluster. The context is kind- followed by the name of your cluster: `kubectl cluster-info --context kind-terraform-learn`
- Configure the provider: create a new file named kubernetes.tf . add   
    provider "kubernetes" {  
      config_path = "~/.kube/config"  
    }  
Copy from kubernetes.tf in this repo.  
- Follow next steps in this lab [Hashicorp tutorials](https://learn.hashicorp.com/tutorials/terraform/kubernetes-provider?in=terraform/kubernetes)