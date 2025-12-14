# Microservices-Task

## Step 1

## Fork the given Repo

<img width="1254" height="691" alt="image" src="https://github.com/user-attachments/assets/9d7b8200-e71e-4496-b4f0-177c8ed7a513" />

<img width="1256" height="707" alt="Forked Repo" src="https://github.com/user-attachments/assets/9a829626-a020-4c4b-90f3-31ce7d3b1638" />

## Step 2

## Starting the docker engine by opening Docker Desktop App

<img width="1278" height="761" alt="Starting Docker Engine" src="https://github.com/user-attachments/assets/8d12c266-7058-4042-afe9-3315348b20e0" />

## Step 3

## Creating Microservices Task Submission Folder and opening it in the VS Code Editor

<img width="828" height="440" alt="Folder Creation" src="https://github.com/user-attachments/assets/dfee82cd-a0d1-420e-ac73-0a16966cd316" />

<img width="1280" height="736" alt="Opening Folder in VS Code" src="https://github.com/user-attachments/assets/26f4f2e7-ff84-4452-b61f-cd6a7e32f0e6" />

## Cloning the forked repository in VS Code Editor

<img width="1278" height="724" alt="Cloning the forked repository" src="https://github.com/user-attachments/assets/136546b8-77b5-45c8-8925-f18270a95c2d" />

## Creating Dockerfile in each folder and adding the script in all the package.json files

<img width="1280" height="770" alt="Dockerfile added in each folder" src="https://github.com/user-attachments/assets/23b54bfd-0acd-4bf5-8685-99345f5d0f66" />

<img width="1145" height="463" alt="Adding script in all package json files" src="https://github.com/user-attachments/assets/4b8f3457-f86e-4c5a-990c-492a19bcb28b" />

## Creating the docker-compose.yml and writing the build for all four services

<img width="1150" height="749" alt="Creation of dockercompose file" src="https://github.com/user-attachments/assets/f7ec3eda-6676-4f9c-9d39-4b5552e3a9a9" />

## Currently, no containers is/are running in the Docker Desktop app

<img width="1277" height="575" alt="No running containers in docker" src="https://github.com/user-attachments/assets/de25550d-3f1a-41d1-a737-331669ad53ab" />

<img width="865" height="464" alt="No running containers in docker powershell" src="https://github.com/user-attachments/assets/32acc726-98c8-4e57-8608-09d28ed99b13" />

## Let's run docker-compose up --build and create the container and check from Docker Desktop app and Powershell that its created or not

<img width="1138" height="723" alt="Docker-compose build" src="https://github.com/user-attachments/assets/123cbd88-2cb5-4a5a-b447-eed2eadd9d59" />

<img width="1280" height="648" alt="Build showing in Docker Desktop" src="https://github.com/user-attachments/assets/44e9dc33-5c66-46f4-bec7-cf4ed2019528" />

<img width="850" height="415" alt="Build showing in Powershell" src="https://github.com/user-attachments/assets/1d808736-1ab9-4be7-8571-e07cba39f45d" />

## Step 4

## Open the respected ports in the browser to see the data

<img width="665" height="382" alt="Port 3000 working" src="https://github.com/user-attachments/assets/e3ed226c-f28e-49d2-be42-e0b6803e06af" />

<img width="692" height="313" alt="Port 3001 working" src="https://github.com/user-attachments/assets/407c41b2-abc1-4f6b-9f31-e0371828a6e9" />

<img width="614" height="251" alt="Port 3002 working" src="https://github.com/user-attachments/assets/a351cdf5-f0af-4082-baae-d99827a54f5d" />

<img width="698" height="311" alt="Port 3003 working 1" src="https://github.com/user-attachments/assets/ab18e48f-609b-4ff7-8381-240fef925e59" />

<img width="674" height="200" alt="Port 3003 working 2" src="https://github.com/user-attachments/assets/f87da60d-3747-47ca-ab6b-6a2ef795d99c" />

## Step 5

## Pushing the code and changes made to GitHub

<img width="742" height="158" alt="Pushing the code to Github" src="https://github.com/user-attachments/assets/b21e2104-3b3d-4fd7-92c5-1ccfc03405e8" />

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Microservices Kubernetes Deployment (Minikube)

This repository contains the **Kubernetes deployment manifests** and setup instructions for deploying a **Node.js-based microservices application** on **Minikube**. The services are containerized and deployed using Kubernetes best practices, including **resource limits**, **liveness/readiness probes**, **secrets**, and **ClusterIP services**.

---

## 📌 Application Overview

The application consists of the following microservices:

| Service Name    | Port | Description                                      |
| --------------- | ---- | ------------------------------------------------ |
| User Service    | 3000 | Manages user-related operations                  |
| Product Service | 3001 | Handles product catalog APIs                     |
| Order Service   | 3002 | Manages order processing                         |
| Gateway Service | 3003 | API Gateway routing requests to backend services |

Each service is deployed as a **Kubernetes Deployment** with a corresponding **ClusterIP Service**.

---

## 🚀 Minikube Setup Steps

Follow the steps below to set up Minikube locally:

```bash
# Verify system supports virtualization
minikube version

# Start Minikube
minikube start

# Verify cluster status
kubectl cluster-info

# Verify nodes
kubectl get nodes
```

Ensure Docker Desktop is running and Kubernetes is enabled (if using Docker Desktop).

<img width="734" height="392" alt="minikube setup" src="https://github.com/user-attachments/assets/83525940-4fa4-40e8-ae23-fec1fcce2e97" />

<img width="414" height="787" alt="image" src="https://github.com/user-attachments/assets/69959d32-a235-4044-a3ec-24f8ad1e735d" />

---

## 📦 Deployment Process (kubectl apply -f)

All Kubernetes manifests are stored under the `K8s/` directory.

### Step 1: Navigate to K8s directory

```bash
cd K8s
```

### Step 2: Apply Deployment and Service manifests

```bash
kubectl apply -f userservice-deployment.yml
kubectl apply -f productservice-deployment.yml
kubectl apply -f orderservice-deployment.yml
kubectl apply -f gatewayservice-deployment.yml
```

### Step 3: Verify resources

```bash
kubectl get deployments
kubectl get pods
kubectl get svc
```

All pods should be in **Running** state and services should be of type **ClusterIP**.

<img width="655" height="80" alt="image" src="https://github.com/user-attachments/assets/10443551-4771-40e7-bd53-9f5b9e8a6e22" />

---

## 🔍 Service Testing Instructions

### Option 1: Using kubectl port-forward (Recommended for testing)

#### User Service

```bash
kubectl port-forward svc/user-service 3000:3000
```

Access:

```
http://localhost:3000/users
```

#### Product Service

```bash
kubectl port-forward svc/product-service 3001:3001
```

Access:

```
http://localhost:3001/products
```

#### Order Service

```bash
kubectl port-forward svc/order-service 3002:3002
```

Access:

```
http://localhost:3002/orders
```

#### Gateway Service

```bash
kubectl port-forward svc/gateway-service 3003:3003
```

Access:

```
http://localhost:3003/health
```

Access:

```
http://localhost:3003/api/users
```

Access:

```
http://localhost:3003/api/products
```

Access:

```
http://localhost:3003/api/orders
```

### Option 2: Service-to-Service Communication (ClusterIP)

Inside the cluster, services communicate using **DNS-based service discovery**:

```text
http://user-service:3000
http://product-service:3001
http://order-service:3002
```

These URLs are injected via environment variables using Kubernetes **Secrets**.

---

## 🧪 Health Checks (Probes)

Each deployment includes:

* **Liveness Probe** – Restarts container if app becomes unhealthy
* **Readiness Probe** – Controls traffic routing to the pod

Example:

```yaml
livenessProbe:
  httpGet:
    path: /products
    port: 3001
  initialDelaySeconds: 30
  periodSeconds: 10

readinessProbe:
  httpGet:
    path: /products
    port: 3001
  initialDelaySeconds: 10
  periodSeconds: 5
```

---

## ⚙️ Resource Requests and Limits

Each container defines CPU and memory constraints:

```yaml
resources:
  requests:
    cpu: "100m"
    memory: "128Mi"
  limits:
    cpu: "250m"
    memory: "256Mi"
```

This ensures:

* Fair scheduling
* Protection against resource exhaustion

---

## 🛠 Troubleshooting Tips

### 1. Pod stuck in ImagePullBackOff

```bash
kubectl describe pod <pod-name>
```

✔ Ensure image exists in Docker Hub
✔ Verify image name and tag

---

### 2. Pod Running but NOT Ready

```bash
kubectl describe pod <pod-name>
```

✔ Check readiness probe path
✔ Ensure API endpoint returns HTTP 200

---

### 3. Probe failures (404 / 500)

✔ Confirm correct API path (`/users`, `/products`, `/gateway`)
✔ Test endpoint locally using port-forward

---

### 4. View container logs

```bash
kubectl logs <pod-name>
```

✨ **Status:** Kubernetes Microservices Deployment successfully completed and validated on Minikube.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Overview
This document provides details on testing various services after running the `docker-compose` file. These services include User, Product, Order, and Gateway Services. Each service has its own endpoints for testing purposes.

---

## Services and Endpoints

### **User Service**
- **Base URL:** `http://localhost:3000`
- **Endpoints:**
  - **List Users:**  
    ```
    curl http://localhost:3000/users
    ```
    Or open in your browser: [http://localhost:3000/users](http://localhost:3000/users)

---

### **Product Service**
- **Base URL:** `http://localhost:3001`
- **Endpoints:**
  - **List Products:**  
    ```
    curl http://localhost:3001/products
    ```
    Or open in your browser: [http://localhost:3001/products](http://localhost:3001/products)

---

### **Order Service**
- **Base URL:** `http://localhost:3002`
- **Endpoints:**
  - **List Orders:**  
    ```
    curl http://localhost:3002/orders
    ```
    Or open in your browser: [http://localhost:3002/orders](http://localhost:3002/orders)

---

### **Gateway Service**
- **Base URL:** `http://localhost:3003/api`
- **Endpoints:**
  - **Users:**  
    ```
    curl http://localhost:3003/api/users
    ```
  - **Products:**  
    ```
    curl http://localhost:3003/api/products
    ```
  - **Orders:**  
    ```
    curl http://localhost:3003/api/orders
    ```

---

## Instructions
1. Start all services using the `docker-compose` file:
   ```
   docker-compose up
   ```
2. Once the services are running, use the above endpoints to verify the functionality.

Happy testing!
