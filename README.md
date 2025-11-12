🗳️ Voting Microservices Application — CI/CD with Azure DevOps, ACR & AKS
🔍 Overview

This project demonstrates a complete DevOps CI/CD pipeline for deploying a containerized microservices-based voting application using Azure DevOps, Azure Container Registry (ACR), and Azure Kubernetes Service (AKS).

It automates the entire workflow — from code commit to deployment — ensuring consistent, repeatable, and fast application delivery.

🧩 Architecture
Component	Description	Technology
🗳️ Vote App	Frontend where users cast votes	Node.js
📊 Result App	Backend service showing results	Python (Flask)
🔐 Auth Service	Handles authentication	Java (Spring Boot)
🗄️ Database (PostgreSQL)	Stores application and user data	Postgres 15-alpine
⚡ Redis	Caching layer for performance	Redis Alpine

All microservices are containerized and deployed to AKS using Kubernetes Deployments and Services.

🧰 Technology Stack
Category	Tools / Services
Cloud Platform	Microsoft Azure
CI/CD	Azure DevOps Pipelines
Containerization	Docker
Registry	Azure Container Registry (ACR)
Orchestration	Azure Kubernetes Service (AKS)
Source Control	Azure Repos / GitHub

