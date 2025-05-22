# 🚀 MERN Stack Application Deployment with Kubernetes

![Docker](https://img.shields.io/badge/Docker-blue?logo=docker)
![Docker Engine](https://img.shields.io/badge/Docker%20Engine-blue?logo=docker)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326ce5?logo=kubernetes)
![Minikube](https://img.shields.io/badge/Minikube-lightblue?logo=kubernetes)
![MongoDB](https://img.shields.io/badge/MongoDB-brightgreen?logo=mongodb)
![Express](https://img.shields.io/badge/Express.js-lightgrey?logo=express)
![React](https://img.shields.io/badge/React-blue?logo=react)
![Node.js](https://img.shields.io/badge/Node.js-green?logo=node.js)
![YAML](https://img.shields.io/badge/Config-YAML-yellow)
![License](https://img.shields.io/badge/license-MIT-blue)
![Status](https://img.shields.io/badge/status-Active-brightgreen)

This repository showcases the deployment of a full-stack MERN (MongoDB, Express, React, Node.js) application on a Kubernetes cluster using Minikube. The project demonstrates containerization, orchestration, and service exposure best practices aligned with industry standards.

---


## ⚙️ Tech Stack

| Layer        | Technology                     |
|-------------|---------------------------------|
| Frontend     | React (Vite)                    |
| Backend      | Node.js, Express                |
| Database     | MongoDB                         |
| Containerization | Docker                      |
| Orchestration   | Kubernetes (Minikube)        |
| Platform      | Ubuntu VM                      |
| Repository    | GitHub                         |

---

## 🛠️ Features

- Add new employees with details
- View a list of employees
- Fully containerized frontend and backend
- Frontend connects to backend via service discovery (`backend` service)
- MongoDB used for persistent storage

---

## 📁 Project Structure

```bash
mern-kubernetes-deployment/
│
├── backend/             # Node.js + Express backend
│   └── Dockerfile
│
├── frontend/            # React frontend
│   └── Dockerfile
│
└── k8s/                 # Kubernetes manifests
```

---

### ⚙️ Prerequisites

- Docker needs to be installed and configured
- Minikube running on a virtual machine
- kubectl CLI configured to interact with Minikube
- Docker Hub account for image hosting

---

### 🚀 Getting Started

1. Clone the Repository
   ```bash
   git clone https://github.com/yourusername/mern-kubernetes-deployment.git
   cd mern-kubernetes-deployment
   ```
2. Build and Push Docker Images
     Ensure Docker is logged in and run:
   ```bash
   # Backend
    cd backend
    docker build -t yourdockerhubusername/mern-backend:1.0 .
    docker push yourdockerhubusername/mern-backend:1.0

   # Frontend
   cd ../frontend
   docker build -t yourdockerhubusername/mern-frontend:1.0 .
   docker push yourdockerhubusername/mern-frontend:1.0
   ```
3. Apply Kubernetes Manifests
   ```bash
   cd ../k8s
   kubectl apply -f .
   ```
4. Access the Application
   Start Minikube service tunnel:
   ```bash
   minikube service frontend
   ```
   Use the provided URL to access the frontend in a browser.

---

### 🎯 Goals and Highlights

- Demonstrates real-world cloud-native deployment of a full-stack app.
- Provides a working Kubernetes architecture with services, deployments, and pods.
- Builds experience in CI/CD readiness and container workflows.
   
---

### 📌 Future Improvements

- Automate deployment via GitHub Actions
- Add Ingress Controller
- Implement persistent storage for MongoDB
- Add monitoring tools like Prometheus and Grafana

---

### 🔍 Known Issues
  ⚠️ Both Frontend & Backend are deployed successfully, but Frontend and Backend communication is currently not working properly due to pending API integration updates. Will be fixed within the next bug fix. 
   
---




   

