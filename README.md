# My Live Kubernetes Configuration

This Repo contains my live configuration for my Kubernetes cluster, it uses Flux CD to monitor this exact repo and push out the configuration to my cluster. Flux CD is a tool that automates the deployment of applications to **Kubernetes clusters**. It follows the **GitOps** methodology, where Git repositories are the single source of truth for defining the desired state of your applications and infrastructure.

## How it Works

Flux CD runs in my Kubernetes cluster and continuously monitors your Git repositories for any changes. When I push a change to your repository, Flux CD automatically applies those changes to my cluster, ensuring that the live state of your applications matches the configuration defined in Git. This process is called **reconciliation**.

This approach provides several benefits:

* **Automation**: Eliminates manual deployments, reducing the risk of human error.
* **Version Control**: All changes are tracked in Git, providing a clear audit trail and the ability to easily roll back to previous versions.
* **Consistency**: Ensures that all your environments (development, staging, production) are configured consistently.
* **Security**: By using a pull-based model, you don't need to expose your Kubernetes API server to external CI/CD systems.
