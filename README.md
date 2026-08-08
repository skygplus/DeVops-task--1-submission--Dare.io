# DeVops-task--1-submission--Dare.io
# DevOps Environment Setup Guide

This guide walks you through setting up a **production-ready local DevOps environment** for cloud-native development, automation, Kubernetes, Infrastructure as Code (IaC), and AI-assisted engineering workflows.

It is designed for engineers working on **macOS, Linux, and Windows (WSL2)**.

---

## 📋 Prerequisites

Before you begin, make sure your machine meets the minimum requirements:

| Requirement | Minimum                        |
| ----------- | ------------------------------ |
| RAM         | 4 GB                           |
| Disk Space  | 10 GB free                     |
| OS          | macOS / Linux / Windows (WSL2) |
| Internet    | Stable connection required     |

> **Recommended:** 8 GB+ RAM and 20–30 GB disk space for smooth Docker and Kubernetes workloads.

---

# 1. Prepare the Host Environment

Start by ensuring your system is clean, updated, and ready for development workloads.

### Supported Platforms

* macOS (latest stable)
* Linux (Ubuntu/Debian recommended)
* Windows with WSL2 enabled

### Checklist

* System is fully updated
* You have admin/sudo access
* At least 4 GB RAM available
* At least 10 GB free disk space
* Stable internet connection
* WSL2 configured (Windows users only)

---

# 2. Install and Configure Version Control (Git)

Git is the backbone of any DevOps workflow.

### Install Git

Verify installation:

```bash
git --version
```

### Configure Identity

Set your global Git identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

Confirm configuration:

```bash
git config --global --list
```

### Git Hosting Setup

Connect Git to your preferred platform:

* GitHub
* GitLab
* Bitbucket (optional)

> ✅ Best practice: Use **SSH authentication** instead of HTTPS for secure and seamless access.

---

### Install Visual Studio Code

VS Code is the recommended IDE for DevOps workflows.

Install and add essential extensions:

* Docker
* Kubernetes
* YAML
* Terraform
* Ansible
* GitLens
* GitHub Actions

---

# 3. (Optional) Enable AI-Assisted Development

AI tools are optional but highly recommended for productivity and automation.

### Recommended Tools

* GitHub Copilot
* Amazon Q
* Gemini CLI
* Codex CLI
* LocalStack

### What they help with:

* Writing infrastructure code faster
* Debugging Kubernetes manifests
* Generating Terraform modules
* Automating CLI workflows
* Cloud architecture assistance

> ⚠️ Note: Some tools require API keys, subscriptions, or local runtime setup.

---

# 4. Install Containerization Tools (Docker)

Docker is the foundation of modern DevOps pipelines.

### Install:

* Docker Engine
* Docker Compose

### Verify installation:

```bash
docker --version
docker compose version
```

### Test Docker:

```bash
docker run hello-world
```

If the container runs successfully, Docker is correctly installed.

---

# 5. Set Up Kubernetes Tooling

Install the core Kubernetes toolchain:

| Tool     | Purpose                        |
| -------- | ------------------------------ |
| Minikube | Local Kubernetes cluster       |
| kubectl  | Kubernetes CLI                 |
| Helm     | Package manager for Kubernetes |

### Verify tools:

```bash
kubectl version --client
minikube version
helm version
```

### Start local cluster:

```bash
minikube start
```

### Validate cluster:

```bash
kubectl get nodes
minikube status
```

---

# 6. Install Cloud CLIs & Runtime Tools

These tools are essential for cloud-native development.

### Install:

* AWS CLI
* Azure CLI
* Node.js (LTS)
* npm
* jq

### Verify installations:

```bash
aws --version
az version
node --version
npm --version
jq --version
```

### Why jq matters:

`jq` is essential for parsing JSON from APIs, CI/CD pipelines, and cloud services.

---

# 7. Install Infrastructure as Code & Automation Tools

## Terraform (Infrastructure as Code)

Used for provisioning cloud infrastructure.

```bash
terraform version
```

## Ansible (Configuration Management)

Used for automation and system configuration.

```bash
ansible --version
```

### What you can build:

* Cloud infrastructure (AWS, Azure, GCP)
* Automated server provisioning
* CI/CD infrastructure
* Multi-environment deployments

---

# 8. Final Verification & System Health Check

Run a full validation of your DevOps toolchain:

```bash
git --version
code --version
docker --version
docker compose version
kubectl version --client
minikube version
helm version
aws --version
az version
node --version
npm --version
jq --version
terraform version
ansible --version
```

---

## Kubernetes Health Check

```bash
minikube status
kubectl get nodes
kubectl get pods -A
```

---

## Docker Health Check

```bash
docker info
docker run --rm hello-world
```

---

# 🔐 Security Best Practices

Before using this environment in real projects:

* Never commit secrets or credentials to Git
* Use `.gitignore` for `.env` files
* Rotate cloud access keys regularly
* Use least-privilege IAM policies
* Secure SSH keys (`chmod 600`)
* Keep OS and tools updated
* Disable unused services and ports
* Store secrets in vaults (AWS Secrets Manager, Azure Key Vault, etc.)

---

# ✅ DevOps Environment Checklist

## 🖥️ Host Setup

* [ ] OS updated
* [ ] 4GB+ RAM available
* [ ] 10GB+ disk space free
* [ ] WSL2 configured (Windows)

## 🧰 Core Tools

* [ ] Git installed & configured
* [ ] VS Code installed
* [ ] SSH keys configured

## 📦 Containers

* [ ] Docker installed
* [ ] Docker Compose working
* [ ] hello-world container runs

## ☸️ Kubernetes

* [ ] Minikube installed
* [ ] kubectl installed
* [ ] Helm installed
* [ ] Cluster running

## ☁️ Cloud & Runtime

* [ ] AWS CLI installed
* [ ] Azure CLI installed
* [ ] Node.js installed
* [ ] jq installed

## ⚙️ Automation

* [ ] Terraform installed
* [ ] Ansible installed

## 🔐 Security

* [ ] Secrets secured
* [ ] Git protected
* [ ] Permissions reviewed

---

# 🚀 What’s Next?

Once your environment is ready, you can start building real-world DevOps workflows:

```text
Git → CI/CD → Docker → Kubernetes → Helm → Terraform → Ansible → Cloud (AWS/Azure)
```

### You are now ready to:

* Build containerized applications
* Deploy Kubernetes workloads
* Automate infrastructure provisioning
* Implement CI/CD pipelines
* Work with multi-cloud environments
* Integrate AI into DevOps workflows

