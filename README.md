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
