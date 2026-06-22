# Minikube-CI-CD-DevOps-Pipeline

## Project Overview

This project demonstrates a complete CI/CD pipeline for deploying a Python Flask application on Kubernetes using Jenkins, Docker, Docker Hub, and Minikube.

The pipeline automatically:

* Pulls source code from GitHub
* Runs Python validation checks
* Builds a Docker image
* Pushes the image to Docker Hub
* Deploys the application to Kubernetes (Minikube)
* Verifies deployment rollout

## Tech Stack

* Python Flask
* Jenkins
* Docker
* Docker Hub
* Kubernetes
* Minikube
* GitHub

## CI/CD Workflow

GitHub -> Jenkins -> Docker Build -> Docker Hub -> Kubernetes (Minikube)

## Pipeline Stages

### 1. Checkout Code

Jenkins pulls the latest source code from GitHub.

### 2. Test Application

* Installs Python dependencies
* Validates application syntax using py_compile

### 3. Build Docker Image

Creates a Docker image of the Flask application.

### 4. Push Docker Image

Pushes the image to Docker Hub using Jenkins Credentials and Docker Hub Personal Access Token.

### 5. Deploy to Kubernetes

Deploys the application using Kubernetes manifests.

### 6. Verify Deployment

Waits for rollout completion and validates successful deployment.

## Screenshots

### Jenkins Pipeline Success

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/8b852537-07c7-407d-a118-a76f99fd984d" />


### Docker Hub Repository

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/b14a66b4-3abd-48e1-b577-9701df70279e" />


### Kubernetes Deployment and Running Pods

<img width="1056" height="184" alt="image" src="https://github.com/user-attachments/assets/79479f06-3ef4-4cef-9324-9f1857bd7479" />

<img width="829" height="182" alt="image" src="https://github.com/user-attachments/assets/f744f8e9-3485-4b32-b741-f75680cea4c0" />


### Flask Application

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/931dd1be-a318-4b43-8621-b78a0e1cccb5" />


## Commands Used

### Check Pods

```bash
kubectl get pods
```

### Check Deployments

```bash
kubectl get deployments
```

### Check Services

```bash
kubectl get svc
```

### Verify Rollout

```bash
kubectl rollout status deployment/flask-app
```

## Docker Hub Image

Docker Image:

```text
nikita311/flask-app:latest
```

## Results

* Automated CI/CD pipeline implemented successfully.
* Docker image pushed automatically to Docker Hub.
* Application deployed on Kubernetes using Minikube.
* Jenkins integrated with GitHub and Docker Hub.
* End-to-end deployment automation achieved.

