# Kubernetes Spring Boot Application

This project demonstrates deployment of a Spring Boot application on Kubernetes using Docker and Minikube.

## Objective

To containerize a Spring Boot application and deploy it on a Kubernetes cluster with scalability and service exposure.

---

## Technologies Used

- Java 17
- Spring Boot
- Maven
- Docker
- Kubernetes
- Minikube
- kubectl

---

## Project Structure

```text
k8sapp/
│── src/
│── target/
│── Dockerfile
│── deployment.yaml
│── service.yaml
│── pom.xml
│── README.md


Build the Application
mvn clean package

Generates JAR file inside target/

Build Docker Image
docker build -t aarya/k8sapp .
Run Docker Container
docker run -p 8080:8080 aarya/k8sapp

Access:

http://localhost:8080
Start Kubernetes Cluster
minikube start
Load Docker Image into Minikube
minikube image load aarya/k8sapp:latest
Deploy Application
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
Verify Resources
kubectl get pods
kubectl get deployments
kubectl get svc
Access Application
minikube service k8sapp-service
Features
Containerized Spring Boot Application
Kubernetes Deployment with Replicas
NodePort Service Exposure
Scalable Architecture
Easy Management using kubectl
Sample Output
2 Pods Running
Service Created
Application Accessible in Browser
Author

Aarya


---

# Small Tip

Before upload remove `target/` folder from GitHub using `.gitignore`

```gitignore
target/
