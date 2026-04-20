# -devops-docker-app
# -devops-docker-app
# 🚀 End-to-End DevOps CI/CD Pipeline with Kubernetes on AWS

## 📌 Project Overview

This project demonstrates a complete end-to-end DevOps pipeline that automates infrastructure provisioning, containerization, CI/CD >

The application is containerized using Docker, deployed on Kubernetes (Minikube), and automated using GitHub Actions. The infrastruc>

---

## 🏗️ Architecture

Developer
        ↓
GitHub Repository
        ↓
GitHub Actions (CI/CD Pipeline)
        ↓
DockerHub (Container Registry)
        ↓
AWS EC2 Instance
        ↓
Minikube Kubernetes Cluster
        ↓
Kubernetes Deployment (Multiple Pods)
        ↓
NodePort Service
        ↓
Live Web Application
---

## 🛠️ Technologies Used

- AWS EC2
- Terraform
- Docker
- Kubernetes (Minikube)
- GitHub Actions
- DockerHub
- Linux (Ubuntu)
- Nginx Web Server

---

## ⚙️ Features Implemented

✔ Infrastructure provisioning using Terraform
✔ Docker containerization
✔ CI/CD pipeline using GitHub Actions
✔ Kubernetes Deployment with multiple replicas
✔ Kubernetes Service (NodePort)
✔ Rolling Updates
✔ Rollback capability
✔ Horizontal scaling
✔ High Availability with multiple pods
✔ Live application deployment on AWS
---

## 📁 Project Structure
project-root/
│
├── Terraform/
│ ├── provider.tf
│ ├── main.tf
│ └── variables.tf
│
├── Docker/
│ ├── Dockerfile
│ └── index.html
│
├── Kubernetes/
│ ├── deployment.yaml
│ └── service.yaml
│
├── .github/workflows/
│ └── main.yml
│
└── README.md

---

## 🚀 Deployment Steps

### Step 1 — Provision Infrastructure Using Terraform

```bash
terraform init
terraform plan
terraform apply

This creates:

AWS EC2 Instance
Security Groups
Networking configuration
 Build Docker Image
docker build -t abh12gupta/myapp:v1 .
 Push Docker Image to DockerHub
docker login
docker push abh12gupta/myapp:v1
 Deploy to Kubernetes
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
 Verify Deployment
kubectl get pods
kubectl get svc
 Scale Application
kubectl scale deployment myapp-deployment --replicas=3
kubectl scale deployment myapp-deployment --replicas=3
Rolling Update
kubectl set image deployment/myapp-deployment \
myapp-container=abh12gupta/myapp:v2
 Rollback Deployment
kubectl rollout undo deployment/myapp-deployment
📸 Screenshots



Kubernetes Pods Running

Kubernetes Services

Deployment Rollout History
Screenshot%202026-04-20%20165445.png
Live Web Application
Screenshot%202026-04-20%20170444.png
GitHub Actions Pipeline Success
Screenshot%202026-04-20%20170524.png
🌐 Live Application Access

Application is accessible via:
http://43.205.211.177:30007
🎯 Key Learning Outcomes

Through this project, the following DevOps concepts were implemented:

Infrastructure as Code (Terraform)
Containerization using Docker
CI/CD Automation using GitHub Actions
Kubernetes Deployment and Services
Rolling Updates with Zero Downtime
Rollback Strategy Implementation
Horizontal Pod Scaling
Cloud Deployment on AWS
🔄 Kubernetes Rollout History Example
kubectl rollout history deployment/myapp-deployment

Output:

REVISION
2
3
📊 Kubernetes Pod Status Example
kubectl get pods

Output:

myapp-deployment-xxxxx   Running
myapp-deployment-yyyyy   Running
myapp-deployment-zzzzz   Running
🧪 Health Verification Commands
kubectl get pods
kubectl get svc
kubectl rollout status deployment/myapp-deployment
📈 Future Improvements
Add Kubernetes Ingress Controller
Implement Helm Charts
Add Monitoring using Prometheus & Grafana
Configure Auto-scaling (HPA)
Implement Load Balancer Service
Add Logging with ELK Stack
👨💻 Author

Abhay Gupta

DevOps Engineer | AWS | Kubernetes | Docker | Terraform

⭐ Project Highlights

✔ End-to-End DevOps Pipeline
✔ Cloud Infrastructure Automation
✔ Kubernetes Deployment with High Availability
✔ CI/CD Pipeline Integration
✔ Production-Style Deployment Workflow
