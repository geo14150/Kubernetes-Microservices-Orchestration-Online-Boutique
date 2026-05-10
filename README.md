# Kubernetes-Microservices-Orchestration-Online-Boutique
This repository demonstrates the deployment and management of a cloud-native microservices application using Kubernetes. The project focuses on showcasing core orchestration features such as self-healing, dynamic scaling, and rolling updates.


🚀 Project Overview
The application used is the Online Boutique, a web-based e-commerce demo consisting of 12 tiered microservices. The services communicate via gRPC and handle various tasks like product catalog management, currency conversion, and payment processing.

Key Features Demonstrated:
Self-Healing: Automatic recovery of failed Pods to maintain the desired state.

Dynamic Scaling: Scaling microservices (e.g., emailservice) based on workload requirements.

Rolling Updates: Zero-downtime deployments with the ability to rollback in case of failure.

Service Discovery: Automated networking between distributed components.

In-Memory Caching: High-performance session management using Redis (redis-cart).

🛠️ Tech Stack
Orchestrator: Kubernetes (Minikube)

Container Engine: Docker Desktop

Environment: WSL 2 (Ubuntu 22.04 LTS)

CLI Tool: kubectl

💻 Local Setup & Installation
1. Prerequisites
Ensure you have the following installed on your local machine:

-Docker Desktop with WSL 2 backend enabled.

-Minikube.

-kubectl.

2. Starting the Cluster
Open your Ubuntu terminal and start Minikube (do not run as root):

minikube start --driver=docker

3. Deploying the Application
Navigate to the project root and apply the Kubernetes manifests:

kubectl apply -f ./release/kubernetes-manifests.yaml

# Kubernetes Pods Status
<img width="854" height="381" alt="getpods" src="https://github.com/user-attachments/assets/f2581107-b5d3-4c7d-a5e6-ab9f336595f5" />


4. Running the Application
To access the web frontend, run the following command to create a tunnel:

minikube service frontend

# SITE ONLINE BOUTIQUE
<img width="1684" height="893" alt="kubernetes" src="https://github.com/user-attachments/assets/4abe6848-ffcd-4eef-9fd7-d68465c5c258" />


This following diagram visualizes the communication flow within the Online Boutique cloud-native application. 
Understanding this architecture is crucial to grasping how Kubernetes coordinates these 12 distinct service tiers.

<img width="662" height="308" alt="image" src="https://github.com/user-attachments/assets/27fa52e6-0f4b-4f41-a873-d4f86410e03e" />


