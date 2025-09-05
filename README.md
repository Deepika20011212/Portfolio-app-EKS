# 🚀 Portfolio App on AWS EKS with GitOps (ArgoCD)

This project demonstrates end-to-end **DevOps practices** by containerizing a Flask-based Portfolio application and deploying it on **AWS EKS** with **ArgoCD** for GitOps-driven Continuous Delivery.  
It leverages **GitHub Actions** for CI/CD, **Docker** for containerization, **ECR** for image storage, and **Helm** for managing Kubernetes manifests with dynamic values.

---

## 📌 Architecture

1. **Application**  
   - Flask-based Portfolio web application.  
   - Dockerized and versioned for consistent deployment.

2. **Infrastructure**  
   - AWS EKS cluster for hosting the application.  
   - Amazon ECR for storing container images.  

3. **CI/CD Pipeline**  
   - **GitHub Actions** for:  
     - Building Docker images  
     - Running code quality & image scans (optional with SonarQube/Trivy)  
     - Pushing images to ECR  
     - Updating Helm values (dynamic image tags)  

4. **Continuous Delivery with ArgoCD**  
   - ArgoCD monitors Git repository.  
   - Syncs updated Helm charts to EKS automatically.

5. **Helm**  
   - Helm charts manage deployment, service, and values dynamically (image tags, replicas, etc.).

---

## 🛠️ Tech Stack

- **Language/Framework**: Python, Flask  
- **Containerization**: Docker  
- **CI/CD**: GitHub Actions, ArgoCD  
- **Orchestration**: Kubernetes (EKS)  
- **Image Registry**: Amazon ECR  
- **IaC : eksctl for EKS setup  
- **Helm**: For Kubernetes deployment automation  

---

## ⚙️ Setup & Deployment

### 1. Clone Repository
```bash
git clone https://github.com/Deepika20011212/Portfolio-app-EKS.git
cd Portfolio-app-EKS
```
### EKS Cluster creation
```bash
eksctl create cluster --name demo-cluster --region us-east-1
```
