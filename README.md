# DeVops-task--1-submission--Dare.io
This guide provides a step-by-step process for preparing a local development environment for DevOps, Cloud, Kubernetes, Infrastructure as Code (IaC), automation, and AI-assisted workflows.

The setup is suitable for macOS, Linux, and Windows using WSL2.

📋 Prerequisites

Before starting, ensure your host machine meets the following minimum requirements:

Requirement	Minimum
RAM	4 GB
Disk Space	10 GB free
Operating System	macOS, Linux, or Windows + WSL2
Internet	Required

Recommendation: 8 GB+ RAM and 20 GB+ free disk space will provide a more comfortable experience, especially when running Docker containers and Kubernetes locally.

1. Prepare the Host Environment

Verify that your operating system is supported and up to date.

Supported Platforms
macOS
Linux
Windows with WSL2

Ensure that:

System updates are installed.
At least 4 GB RAM is available.
At least 10 GB of free disk space is available.
You have administrative privileges where required.
Your system has a stable internet connection.

For Windows users, ensure WSL2 is installed and configured before continuing.

2. Establish Version Control

Git is required for source-code management and integration with platforms such as GitHub and GitLab.

Install Git

Verify whether Git is already installed:

git --version

Configure your Git identity:

git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

Verify the configuration:

git config --global --list
Git Hosting

Configure access to your preferred Git hosting platform:

GitHub
GitLab
Other compatible Git repositories

SSH authentication is recommended for secure repository access.

Install Visual Studio Code

Install Visual Studio Code as the primary development environment.

Recommended extensions include:

Docker
Kubernetes
YAML
Terraform
Ansible
GitHub Actions
GitLens
3. Integrate AI Capabilities

AI-assisted development and DevOps tooling is optional but can significantly improve productivity.

Consider installing and evaluating tools such as:

GitHub Copilot
Amazon Q
Gemini CLI
Codex CLI
LocalStack

These tools can assist with:

Code generation
Troubleshooting
Infrastructure configuration
Kubernetes manifests
Terraform configuration
CLI workflows
Cloud development
DevOps automation

Note: AI tools may require separate accounts, subscriptions, API keys, or local resources depending on the tool.

4. Install Containerization Tools

Docker provides the foundation for building and running containerized applications.

Install:

Docker
Docker Compose

Verify the installation:

docker --version
docker compose version

Run a basic verification:

docker run hello-world

Confirm Docker is able to start containers successfully before continuing.

5. Set Up Kubernetes Tooling

Install the following Kubernetes tools:

Tool	Purpose
Minikube	Local Kubernetes cluster
kubectl	Kubernetes command-line client
Helm	Kubernetes package manager
Verify kubectl
kubectl version --client
Verify Minikube
minikube version

Start a local Kubernetes cluster:

minikube start

Check the cluster status:

minikube status

Verify Kubernetes connectivity:

kubectl get nodes
Verify Helm
helm version
6. Configure Cloud and Language Runtimes

Install the required cloud CLIs and development utilities.

Required Tools
AWS CLI
Azure CLI
Node.js
npm
jq
Verify AWS CLI
aws --version
Verify Azure CLI
az version
Verify Node.js
node --version
npm --version
Verify jq
jq --version

jq is particularly useful for processing and querying JSON returned by cloud APIs and command-line tools.

7. Install Infrastructure & Configuration Tools

This environment uses Terraform for Infrastructure as Code and Ansible for configuration management and automation.

Terraform

Verify the installation:

terraform version

Terraform can be used to define and provision infrastructure across cloud and local environments.

Ansible

Verify the installation:

ansible --version

Ansible can be used for:

Configuration management
Application deployment
Server provisioning
Task automation
Infrastructure orchestration
8. Verification and Security

After installing all required tools, run a final verification.

Tool Verification

Run the following commands:

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

All commands should return a valid version or installation response.

Kubernetes Verification

If Minikube is running:

minikube status
kubectl get nodes
kubectl get pods -A
Docker Verification
docker info
docker run --rm hello-world
🔐 Security Checklist

Before using the environment for real projects, verify:

Git credentials are configured securely.

SSH keys have appropriate file permissions.

Cloud credentials are not committed to Git repositories.

API keys and tokens are stored securely.

.env files containing secrets are included in .gitignore.

Docker is running with appropriate user permissions.

Kubernetes configuration files are protected.

Cloud CLI credentials use the principle of least privilege.

Operating system security updates are installed.

Unnecessary services and ports are disabled.

Never commit credentials, private keys, access tokens, or cloud secrets to a Git repository.
