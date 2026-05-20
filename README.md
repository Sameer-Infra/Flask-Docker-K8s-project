 # 👨‍💻 Author

 # Sameer | 👨‍💻☸️ DevOps & Ai Engineer 🤖☁️ (Aspiring)

 # GitHub: Sameer-Infra

 # Project: Flask CI/CD Pipeline using Jenkins, Docker & Kubernetes.


# 📌 Project Overview
This project demonstrates a real-world DevOps CI/CD pipeline that automates deployment of a Flask application using:


# . Jenkins (Automation Server)

# . Docker (Containerization)

# . Kubernetes (Orchestration)

# . Docker Hub (Image Registry)


# 👉 Goal:
Every code push automatically builds, packages, and deploys the application to a Kubernetes cluster without manual 
intervention.

# # Project Structure

```text id="m5k8v2"
Flask-Docker-K8s-project/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── Jenkinsfile
├── README.md
│
├── k8s/
│   ├── namespace.yaml
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── ingress.yaml
│   ├── configmap.yaml
│   ├── secret.yaml
│   ├── hpa.yaml
│   └── pvc.yaml
│
└── docker-compose.yml




# ⚙️ CI/CD Pipeline Workflow
1️⃣ Code Push (GitHub)
Developer code push karta hai GitHub repository me.

2️⃣ Jenkins Trigger
Jenkins automatically pipeline start karta hai.

3️⃣ Docker Image Build
Flask application ka Docker image build hota hai:
docker build -t techwithsameer/sameer-flask-app:latest .

4️⃣ Docker Hub Login & Push
Jenkins securely login karta hai aur image push karta hai:
docker logindocker push techwithsameer/sameer-flask-app:latest

5️⃣ Kubernetes Deployment
Latest image Kubernetes cluster me deploy hoti hai:
kubectl apply -f k8s-Deployment.yamlkubectl apply -f K8s-Service.yaml

6️⃣ Service Exposure
Application Service ke through expose hoti hai (LoadBalancer/NodePort).

7️⃣ Auto Scaling (HPA)
Kubernetes automatically traffic ke hisaab se pods scale karta hai.


# # Jenkins Shared Library

This project uses a centralized Jenkins Shared Library for reusable CI/CD pipeline functions.

## Shared Library Repository

 # https://github.com/Sameer-Infra/jenkins-shared-libraries.git #

## Shared Library Import

@Library('Shared') _

## Shared Library Structure

Shared/
│
├── vars/
│   ├── hello.groovy
│   ├── Clone.groovy
│   ├── docker_build.groovy
│   ├── docker_push.groovy
│   └── docker_compose.groovy
│
├── src/
└── resources/
```

The shared library contains reusable Jenkins pipeline functions for:

* GitHub Repository Cloning
* Docker Image Build
* DockerHub Push
* Docker Compose Deployment
* Common CI/CD Utilities




## 🛠️ Tech Stack

| Tool       | Purpose                       |
| ---------- | ----------------------------- |
| Flask      | Web Application               |
| Jenkins    | CI/CD Automation              |
| Docker     | Containerization              |
| Kubernetes | Container Orchestration       |
| Docker Hub | Image Registry                |
| GitHub     | Version Control               |
| kubectl    | Kubernetes Cluster Management |





# ☸️ Kubernetes Components

Deployment (App lifecycle management)

Service (Networking & exposure)

Pods (Application runtime)

Ingress (External access routing)

HPA (Auto scaling)


# 📂 Project Structure
Flask-Docker-K8s-project/│├── app.py├── requirements.txt├── Dockerfile├── Jenkinsfile│├── k8s-Deployment.yaml├── K8s-Service.yaml│└── README.md

# ⚡ Jenkins Pipeline Stages

. Clone GitHub Repository

. Build Docker Image

. Login to Docker Hub

. Push Image to Registry

. Deploy to Kubernetes

. Verify Deployment


# 🚨 Real-World Challenges Solved

. Jenkins ↔ Kubernetes authentication setup

. Docker image versioning issues

. Kubernetes networking & service debugging

. CI/CD pipeline failure handling

. Cluster deployment troubleshooting


# 📚 Key Learnings

. Designing CI/CD pipelines using Jenkins

. Docker image lifecycle management

. Kubernetes deployment architecture

. Debugging production deployment issues

. Secure credential handling in CI/CD

. Cloud-native DevOps workflow understanding


# 📈 Business Impact

⚡ Faster software delivery

🧠 Reduced manual deployment errors

📦 Fully automated release pipeline

📊 Scalable cloud-native architecture

🚀 Production-grade DevOps workflow


# 🚀 Future Enhancements

. Helm Chart deployment

. ArgoCD GitOps integration

. Prometheus + Grafana monitoring

. Terraform infrastructure automation

. Blue-Green / Canary deployment

. Multi-environment CI/CD pipeline



# 🏁 Conclusion
This project demonstrates a real-world DevOps CI/CD pipeline using Jenkins, Docker, and Kubernetes. It showcases automation, scalability, and production-grade deployment practices used in modern cloud-native environments.
