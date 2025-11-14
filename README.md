# 🗳️ voting-micro-service-application---azurepipelines

![Home Page](./screenshots/devops_theme.png)


 
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
- **Vote Service** – The UI where votes are cast  
- **Result Service** – Aggregates and displays voting outcomes  
- **worker Service** – fetch data from redis store in pstgres data base
- **PostgreSQL** – Persistent datastore for votes & users  
- **Redis** – Optional caching

### Workflow  
1. Developer commits code → triggers pipeline  
2. Build stage: compile/build microservices → produce Docker images  
3. Push stage: Docker images pushed to ACR with tags  
4. Deploy stage: Kubernetes manifests applied to AKS cluster  
5. External endpoint exposed via LoadBalancer 

---

## 🧰 Tech Stack  
| Layer        | Technology                |
|------------- |---------------------------|
| Front-end/API | Node.js  (Vote)  |
| Back-end     | Python or Java (Result) |
| Data Store   | PostgreSQL 15             |
| Cache        | Redis                     |
| Container    | Docker                    |
| Registry     | Azure Container Registry  |
| Orchestration| Azure Kubernetes Service  |
| CI/CD        | Azure DevOps Pipelines    |

---

## 📂 Repository Structure 

![Pods Running](./screenshots/structure.png)


## 📸 Application Screenshots

### 🏠Voting Page
![Home Page](./screenshots/voting_page.png)

### 🔐 Result Page
![Login Page](./screenshots/result-page.png)

### 🔐 azure-devops-repo Page
![Login Page](./screenshots/repo-page.pnG)


### 🔐 CI/CD Pipelines
![Login Page](./screenshots/all-pipelines.png)


### 🚀 CI/CD Pipelines Success
![CI/CD Pipeline](./screenshots/result_pipeline_runs.png)

![CI/CD Pipeline](./screenshots/vote_pipeline_runs.png)

![CI/CD Pipeline](./screenshots/worker_pipeline_runs.png)

### ✅ repos-AZURE-CONTAINER-REGISTRY
![Pods Running](./screenshots/acr_repository.png)

### ✅ Deployments  loads in AKS
![Pods Running](./screenshots/dep.png)

### ✅ Pods Running in AKS
![Pods Running](./screenshots/pods_aks.png)

### ✅ Pods Running in AKS terminal
![Pods Running](./screenshots/pods_cluster.png)

### ✅ configured self-hosted runner for CICD pipeline
![Pods Running](./screenshots/azure_agent.png)

### ✅ personal-hosted agent listening for jobs
![Pods Running](./screenshots/jobs_lis.png)


### 🌐 Services
![Service](./screenshots/serv.png)











