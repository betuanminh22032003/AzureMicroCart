# Azure Microservices E-Commerce System 🚀

[![Azure Container Apps](https://img.shields.io/badge/Azure-Container%20Apps-0078D4?logo=microsoft-azure)](https://azure.microsoft.com/en-us/products/container-apps/)
[![.NET 8](https://img.shields.io/badge/.NET-8-512BD4?logo=dotnet)](https://dotnet.microsoft.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A cloud-native e-commerce microservices system built with .NET 8, Docker, and Azure Free Tier services, implementing API-first and Zero Trust architectures.

## 📋 Project Overview
```mermaid
graph TD
    A[Frontend] --> B[Azure API Management]
    B --> C[User Service]
    B --> D[Cart Service]
    B --> E[Order Service]
    C & D & E --> F[Azure SQL DB]
    E --> G[Azure Storage Queue]
```

## 🛠️ Tech Stack
| Component | Technology |
|-----------|------------|
| Microservices | .NET 8 Minimal API |
| Containerization | Docker + Azure Container Apps |
| API Gateway | Azure API Management (Developer) |
| Database | Azure SQL DB (Free Tier) |
| Event-Driven | Azure Storage Queue |
| CI/CD | GitHub Actions |
| Infrastructure | Bicep (IaC) |
| Security | Azure AD + Managed Identities |

## 📅 4-Week Implementation Plan
### Week 1: Core Setup

```mermaid
gantt
    title Week 1 - Foundation
    dateFormat  YYYY-MM-DD
    section Setup
    Environment Setup          :done, env1, 2024-01-01, 0.5d
    section Microservices
    User Service (GET/POST)    :active, user, 2024-01-01, 3d
    Cart Service (GET/PUT)     :active, cart, after user, 3d
    Order Service (POST)       :active, order, after cart, 3d
    section Deployment
    Dockerize & ACR Push       :crit, docker, 2024-01-04, 1d
```

### Week 2-4: Advanced Integration
| Week | Focus Area | Key Tasks |
|------|------------|-----------|
| 2 | API Management & Auth | • APIM Developer Tier Setup<br>• Azure AD JWT Integration<br>• Storage Queue Eventing |
| 3 | DevSecOps | • GitHub Actions CI/CD<br>• Bicep Infrastructure<br>• Trivy Container Scanning |
| 4 | Zero Trust & Demo | • Managed Identities<br>• k6 Load Testing<br>• Final Presentation |

## 🚀 Getting Started
### Prerequisites
- Azure Student Account ($100 credit)
- Docker Desktop
- .NET 8 SDK

### Quick Deployment
```bash
# Deploy infrastructure with Bicep
az deployment group create \
  --resource-group myResourceGroup \
  --template-file main.bicep

# Deploy microservices
az containerapp up \
  --name userservice \
  --source ./UserService \
  --resource-group myResourceGroup
```

## 🌐 Architecture
![System Architecture](docs/architecture.png)

## 📊 Monitoring
```mermaid
graph LR
    A[Container Apps] --> B[Application Insights]
    B --> C[Azure Monitor]
    C --> D[Custom Dashboards]
```

## 📜 License
MIT License - See LICENSE for details.