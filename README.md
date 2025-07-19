# 🚀 DevOps Portfolio Project

This project is designed to showcase essential DevOps skills by implementing a full CI/CD pipeline for a Python web application using modern DevOps tools and best practices.

##  What i learned

- How to create a CI/CD pipeline using **GitHub Actions**
- Automatically build and push Docker images
- Deploy a **Flask** (Python) app to a **Kubernetes** cluster
- Use `kubectl` and Kubernetes manifests in CI/CD workflows
- Configure **RBAC**, **ServiceAccounts**, and secure access with **Secrets** and **kubeconfig**
- Apply best practices for building real-world DevOps portfolio projects

---

## ✅ Tech Stack

- **Python (Flask)**
- **Docker**
- **GitHub Actions (CI/CD)**
- **Kubernetes (AKS)**
- **Azure Cloud**
- **RBAC, ServiceAccounts, Secrets**
- **kubeconfig, ClusterRoleBinding**
---
## ⚙️ CI/CD Pipeline

1. **Push to GitHub** triggers the pipeline
2. GitHub Actions:
   - Builds Docker image
   - Pushes image to Docker Hub Registry
   - Uses `kubectl` with a secured **kubeconfig** to deploy on K8s
---
## 🔐 Security & Access Control

This project demonstrates **production-ready access controls**:

- **ServiceAccount**: Dedicated K8s identity for CI/CD agent
- **RBAC**: `Role` and `RoleBinding` limit access to specific namespaces
- **ClusterRoleBinding**: Grants access to perform `kubectl apply` in CI
- **Secrets**: Used to store sensitive values (e.g., Docker credentials or app config)
- **kubeconfig**: A restricted kubeconfig file is used in the GitHub Actions workflow to interact with the cluster

> ✅ These practices align with DevSecOps principles for secure automation.
## ☁️ Cloud Environment

This project was deployed on **Azure Kubernetes Service (AKS)**.

- Cluster created and managed using Azure CLI
- Kubeconfig securely used in CI/CD pipeline
- Azure RBAC and IAM handled through AKS integrations
- Azure Container Registry (optional) supported for Docker images

---
