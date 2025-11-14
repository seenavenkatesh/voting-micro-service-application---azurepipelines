# 🗳️ Voting-Application  
**Microservices Voting System** | CI/CD with Azure DevOps → Azure Container Registry → Azure Kubernetes Service  

[![Azure DevOps](https://img.shields.io/badge/AzureDevOps-CI%2FCD-blue?logo=azuredevops)](#)  
[![Docker](https://img.shields.io/badge/Docker-Containerized-blue?logo=docker)](#)  
[![Kubernetes](https://img.shields.io/badge/Kubernetes-AKS-%23326ce5?logo=kubernetes)](#)  

---

## 📖 Project Overview  
This repository implements a voting application composed of multiple microservices, containerised and deployed via a full DevOps pipeline on Microsoft Azure.  
It is designed to demonstrate:  
- Modular microservices architecture  
- Docker containerisation for each service  
- Pushing images to Azure Container Registry (ACR)  
- Deploying services to Azure Kubernetes Service (AKS) with Kubernetes manifests  
- Automated CI/CD via Azure DevOps Pipelines  

---

## 🏗 Architecture & Service Breakdown  
### Services  
- **Vote Service** – The UI or API endpoint where votes are cast  
- **Result Service** – Aggregates and displays voting outcomes  
- **Auth Service** – Handles authentication/authorization for users  
- **PostgreSQL** – Persistent datastore for votes & users  
- **Redis** – Optional caching / speed layer  

### Workflow  
1. Developer commits code → triggers pipeline  
2. Build stage: compile/build microservices → produce Docker images  
3. Push stage: Docker images pushed to ACR with tags  
4. Deploy stage: Kubernetes manifests applied to AKS cluster  
5. External endpoint exposed via LoadBalancer / Ingress → users interact  

---

## 🧰 Tech Stack  
| Layer        | Technology                |
|------------- |---------------------------|
| Front-end/API | Node.js / Express (Vote)  |
| Back-end     | Python or Java (Result/Auth) |
| Data Store   | PostgreSQL 15             |
| Cache        | Redis                     |
| Container    | Docker                    |
| Registry     | Azure Container Registry  |
| Orchestration| Azure Kubernetes Service  |
| CI/CD        | Azure DevOps Pipelines    |

---

## 📂 Repository Structure  

voting-application/
│
├── vote/           # voteapp microservice
│   ├── Dockerfile
│   └── src/...
│
├── result/         # resultapp microservice
│   ├── Dockerfile
│   └── src/...
│
├── worker/         # worker microservice (replaces auth)
│   ├── Dockerfile
│   └── app/...
│
├── manifests/      # Kubernetes YAML files
│   ├── voteapp/
│   ├── resultapp/
│   ├── worker/
│   ├── redis.yaml
│   ├── postgres.yaml
│   └── ingress.yaml
│
├── pipeline/       # Azure DevOps YAML pipeline
│   └── azure-pipeline.yml
│
└── README.md


