# 👨‍💻 **PROJECT BY: SAMEER-INFRA**

# 🚀 **FLASK + DOCKER + KUBERNETES PLATFORM**

### ⚡ Production-style containerized application with Kubernetes orchestration, Ingress routing, PV/PVC storage, and HPA autoscaling.

---

## ✨ **KEY HIGHLIGHTS**

- ⚡ **Lightweight Flask Application**
- 🐳 **Docker Containerized Setup**
- ☸️ **Kubernetes Deployment (Manifests Based)**
- 🌐 **Ingress for External Traffic Routing**
- 💾 **Persistent Volume (PV) + PVC Storage**
- 📈 **Horizontal Pod Autoscaler (HPA)**
- 📦 **Cloud-Native Architecture Design**

---

## 🏗️ **SYSTEM ARCHITECTURE**

### **Client Request**
⬇️  
### **Ingress Controller**
⬇️  
### **Kubernetes Service**
⬇️  
### **Flask Application Pods**
⬇️  
### **PV / PVC Storage Layer**

📈 **HPA automatically scales pods based on CPU usage**

---

## 🛠️ **TECH STACK**

| Layer         | Technology |
|---------------|------------|
| Application   | **Flask (Python)** |
| Container     | **Docker** |
| Orchestration | **Kubernetes** |
| Networking    | **Ingress Controller** |
| Storage       | **PV & PVC** |
| Scaling       | **Horizontal Pod Autoscaler** |

---

## 📂 **PROJECT STRUCTURE**
Flask-Docker-K8s-project/
│
├── app.py
├── requirements.txt
├── Dockerfile
│
├── k8s/
│ ├── deployment.yaml
│ ├── service.yaml
│ ├── ingress.yaml
│ ├── hpa.yaml
│ ├── pv.yaml
│ ├── pvc.yaml
│
├── templates/
├── static/
└── README.md

----

## 🐳 **DOCKER RUN**

```bash
docker build -t flask-app .
docker run -p 5000:5000 flask-app
👉 Access: http://localhost:5000

☸️ KUBERNETES DEPLOYMENT

kubectl apply -f k8s/

Check status:
kubectl get pods
kubectl get svc
kubectl get ingress
kubectl get hpa

🌐 INGRESS

External traffic is routed into the cluster using Ingress Controller for controlled access to services.

💾 STORAGE (PV + PVC)
* PV (Persistent Volume): Cluster-level storage
* PVC (Persistent Volume Claim): Application-bound storage
* Ensures data persistence across pod restarts

📈 AUTOSCALING (HPA)

Automatically scales application pods based on CPU usage and load demand.

📌 DESIGN PRINCIPLES
* Modular Kubernetes architecture
* Separation of compute, networking, and storage
* Production-style deployment workflow

🔥 WHAT THIS PROJECT SHOWS
* Docker containerization workflow
* Kubernetes orchestration system
* Ingress-based routing
* Persistent storage handling
* Auto-scaling system design
