# Microservice App Deployment into Kubernetes

## Introduction

**Microservices in Kubernetes** refer to independently deployable units of an application, each focusing on a specific function or business capability. These microservices typically communicate with one another via APIs, Container Network Interfaces (CNIs), and other mechanisms to work together as a larger application. Kubernetes serves as a powerful orchestration platform for managing these microservices.

This project is based on the official **microservice-demo** project from Google Cloud: [GoogleCloudPlatform/microservices-demo](https://github.com/GoogleCloudPlatform/microservices-demo). It represents a web-based e-commerce application, where various components such as email services, checkout, shipping, payment, and others are decoupled and managed as separate microservices.

![image](https://github.com/user-attachments/assets/6545d60a-d1f9-4473-9e7a-8c7a4911284d)


## Scope

- Understand the microservices being deployed, including image names, build languages, listening ports, and environment variables.
- Identify how the microservices connect to each other and their dependencies.
- Determine third-party services or databases required.
- Identify the entry-point service.
- Deploy the Microservice App into Kubernetes.

## Steps: Create Deployments for Each Microservice

Follow these steps to deploy the microservices:

1. **Namespace**  
   Deploy all microservices in the same namespace (Default in this project).

2. **Labels**  
   Ensure that all deployments have matching labels.

3. **Image**  
   Pull the microservice images from Google Artifactory.

4. **Ports & Environment Variables**  
   Configure the listening ports and pass necessary environment variables.

5. **Dependencies**  
   Pass any microservice dependencies as environment variables.

6. **Service**  
   Create a Kubernetes service for each microservice, including a pod selector and target ports.

7. **Frontend Service**  
   Set the frontend service as a NodePort for external access.

8. **Deployment**  
   Deploy the services and microservices into Kubernetes.

9. **Access**  
   Access the web application through the frontend service NodePort.
