# Wanderlust Deployment on Kubernetes

### In this project, we will learn about how to deploy wanderlust application on Kubernetes.

### Pre-requisites to implement this project:
-  Create 2 AWS EC2 instance (Ubuntu) with instance type t2.medium and root volume 29GB.
-  Setup <a href="https://github.com/DevMadhup/wanderlust/blob/devops/kubernetes/kubeadm.md"><u> Kubeadm </a></u>

### 📌 Overview

This project demonstrates how to deploy the Wanderlust MERN application on a Kubernetes cluster using Kubeadm.
It includes containerization, service exposure, and multi-tier deployment with MongoDB, Redis, backend, and frontend services.

### 🧠 Architecture
Frontend (React) → exposed via NodePort
Backend (Node.js API) → handles business logic
Database → MongoDB (persistent storage)
Cache → Redis
Orchestration → Kubernetes cluster (Kubeadm setup)

### ⚙️ Tech Stack
Containerization: Docker
Orchestration: Kubernetes (Kubeadm)
Cloud: AWS EC2
Database: MongoDB
Caching: Redis

### 🚀 Deployment Flow
Clone application code from GitHub
Build Docker images for frontend and backend
Push images to DockerHub
Create Kubernetes namespace
Deploy:
Persistent Volume & PVC
MongoDB & Redis
Backend service
Frontend service
Access application via NodePort

### 🛠️ Prerequisites
2 AWS EC2 instances (t2.medium, Ubuntu)
Kubernetes cluster setup using Kubeadm
Docker installed on nodes
kubectl configured

### ⚡ Quick Setup

# Clone repository
git clone -b devops https://github.com/DevMadhup/wanderlust.git

# Create namespace
kubectl create namespace wanderlust
kubectl config set-context --current --namespace wanderlust

# Apply manifests
kubectl apply -f persistentVolume.yaml
kubectl apply -f persistentVolumeClaim.yaml
kubectl apply -f mongodb.yaml
kubectl apply -f redis.yaml
kubectl apply -f backend.yaml
kubectl apply -f frontend.yaml

### 🌐 Access Application
http://<worker-node-public-ip>:31000

### 📊 Key Features
Multi-tier Kubernetes deployment
Persistent storage using PV & PVC
Service-based communication (MongoDB, Redis, Backend)
Scalable architecture using Kubernetes
Dockerized frontend & backend

### 💡 Learnings
Kubernetes resource management (Deployments, Services, PV, PVC)
Multi-service application deployment
Container networking & service discovery
Handling dependencies between services

### 🎯 Conclusion

This project showcases how to deploy a real-world MERN application on Kubernetes using Kubeadm, covering core concepts like containerization, orchestration, and service communication.

20) Navigate to chrome and access your application at 31000 port :
```bash
http://<your-workernode-publicip>:31000/
```
![App](https://github.com/DevMadhup/wanderlust/blob/devops/kubernetes/assets/app.png)

#

