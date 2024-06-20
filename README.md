# Argo CD Apps

## Documentation

This repository contains Kubernetes and ArgoCD configuration files essential for deploying and managing applications in a Kubernetes environment. Below is a brief overview of the purpose and structure of each file and directory within this repository.

### Directory Structure

- `apps/`: Contains Kubernetes deployment and service configurations for individual applications. Each application, such as `app1`, `app2`, `pgadmin`, and `task`, has its own `deployment.yaml` file, specifying how the application should be deployed and managed within the Kubernetes cluster.

- `argocd/apps/`: Houses ArgoCD Application configurations for each application managed by ArgoCD. This includes configurations for applications like `app1`, `app2`, as well as system configurations such as `clusterrole.yaml` and `multi-juicer.yaml`. These files define how ArgoCD should deploy and maintain these applications in sync with the repository.

### Kubernetes Files

- `apps/app1/deployment.yaml`: Defines the deployment configuration for `app1`, including the Docker image to use and the desired number of replicas.

- `apps/app2/deployment.yaml`: Similar to `app1`, this file specifies the deployment details for `app2`, focusing on the Docker image and replica count.

- `apps/pgadmin/deployment.yaml`: Configures the deployment for `pgadmin`, including the service to expose it externally and the Docker image details.

- `apps/task/deployment.yaml`: Specifies the deployment and service configuration for the `task` application, detailing the Docker image to use and how to expose the service.

### ArgoCD Files

- `argocd/apps/app1.yaml`: ArgoCD application configuration for `app1`, detailing the source repository, path, and sync policy.

- `argocd/apps/app2.yaml`: Defines how ArgoCD should manage the deployment of `app2`, including the repository details and sync policy.

- `argocd/apps/clusterrole.yaml`: Specifies a cluster role configuration managed by ArgoCD, important for defining access controls within the Kubernetes cluster.

- `argocd/apps/multi-juicer.yaml`: Configuration for deploying the `multi-juicer` application via ArgoCD, including details on the Helm chart and parameters.

- `argocd/apps/pgadmin.yaml`: ArgoCD configuration for managing the `pgadmin` application, outlining the deployment path and sync policy.

- `argocd/apps/task.yaml`: Details the ArgoCD management of the `task` application, including the source path and sync policy.

- `application.yaml`: The root ArgoCD Application configuration, defining the global settings for how ArgoCD interacts with this repository to manage applications within the Kubernetes cluster.
