# 🚀 Deployement Project – Helm Chart (Frontend)

## 📌 Overview

Ce projet contient un **Helm Chart Kubernetes** pour déployer une application frontend.

Il automatise le déploiement, la scalabilité et la configuration de l’application via Kubernetes.

---

## 📁 Project Structure

```
Deployement-Project/
│
├── frontend/
│   ├── templates/
│   │   ├── NOTES.txt
│   │   ├── _helpers.tpl
│   │   ├── deployment.yaml
│   │   ├── service.yaml
│   │   ├── ingress.yaml
│   │   ├── hpa.yaml
│   │   ├── serviceaccount.yaml
│   │   └── tests/
│   │
│   ├── Chart.yaml
│   ├── values.yaml
│   └── .helmignore
│
├── mon-chart/
│   ├── templates/
│   │   ├── NOTES.txt
│   │   ├── _helpers.tpl
│   │   └── ...
│   ├── Chart.yaml
│   ├── values.yaml
│   └── .helmignore
│
└── README.md
```

---

## ⚙️ What This Helm Chart Does

### 🧩 1. Deployment

* Déploie le frontend sur Kubernetes
* Définit les replicas
* Configure les containers (image, ports, env variables)

---

### 🌐 2. Service

* Expose l’application en interne (ClusterIP / NodePort / LoadBalancer)
* Permet la communication entre pods

---

### 🚪 3. Ingress

* Expose l’application à l’extérieur
* Gestion des routes HTTP/HTTPS
* Support domaine personnalisé

---

### 📈 4. HPA (Horizontal Pod Autoscaler)

* Auto-scale les pods selon :

  * CPU usage
  * Memory usage
* Améliore la performance et la stabilité

---

### 🔐 5. ServiceAccount

* Gestion des permissions Kubernetes
* Sécurité des pods

---

### 🧪 6. Tests Helm

* Validation des templates
* Vérification du rendu YAML

---

## 📦 Configuration (values.yaml)

Le fichier `values.yaml` permet de configurer :

* image Docker
* replicas
* ressources CPU / RAM
* ingress domain
* autoscaling rules

Exemple :

```yaml
replicaCount: 2

image:
  repository: my-frontend
  tag: latest

service:
  type: ClusterIP
  port: 80
```

---

## 🚀 Installation

### 1. Installer le chart

```bash
helm install frontend ./frontend
```

---

### 2. Mettre à jour le chart

```bash
helm upgrade frontend ./frontend
```

---

### 3. Supprimer le déploiement

```bash
helm uninstall frontend
```

---

## 🔍 Check status

```bash
kubectl get pods
kubectl get services
kubectl get ingress
```

---

## 📊 DevOps Value

Ce projet permet :

* ⚡ Déploiement automatisé
* 🔄 CI/CD ready
* 📈 Scalabilité automatique
* 🔐 Sécurité Kubernetes
* 🌍 Production-ready architecture

---

## 🎯 Goal

Transformer le frontend en application **cloud-native**, scalable et automatisée avec Kubernetes + Helm.

---

## 👨‍💻 Tech Stack

* Kubernetes ☸️
* Helm 📦
* Docker 🐳
* Nginx / Frontend React (ou autre)
* HPA + Ingress Controller

---

 
