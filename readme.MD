# 🚀 Kubernetes Microservices Deployment

This project deploys a microservices-based e-commerce platform on a Kubernetes cluster.

---

## 🧱 Microservices Overview

| 🔢 Service       | ⚙️ Description                       | 🗂️ Type       |
|-------------------|--------------------------------------|----------------|
| 🛒 `cart`         | Manages shopping cart                | Microservice  |
| 📚 `catalogue`    | Handles product catalog              | Microservice  |
| 🐞 `debug`        | Debugging/testing purposes           | Utility       |
| 🌐 `frontend`     | Web UI for users                     | Frontend      |
| 🧑‍💻 `user`         | User account management              | Microservice  |
| 💳 `payment`      | Payment gateway integration          | Microservice  |
| 🚚 `shipping`     | Shipping details and tracking        | Microservice  |

---

## 🗄️ Database Services

| 🧩 DB Service     | 💾 Database Type     | 📌 Used By            |
|--------------------|----------------------|--------------------------|
| 🐘 `mongodb`      | NoSQL (MongoDB)      | Catalogue, User        |
| 🐬 `mysql`        | SQL (MySQL)          | Shipping               |
| 🐰 `rabbitmq`     | Message Broker       | Dispatch, Order Flow   |
| 🧠 `redis`        | In-Memory DB/Cache   | Cart, Session Storage  |

---

## 🖥️ Infra & Instance

| 🧰 Component   | 🔍 Purpose                    |
|---------------|---------------------------------|
| ⚙️ `instance` | Backend app instances/pods     |
| 🧪 `debug`    | Debug tool inside the cluster  |

---

## 📦 Deployment Flow

1. 🔹 Create Namespace  
2. 📥 Deploy ConfigMaps & Secrets  
3. 🏗️ Deploy Databases  
4. 🚀 Deploy Microservices  
5. 🌐 Expose via Services  

---

## ✅ Status Check

```bash
kubectl get all -n <namespace>
kubectl logs <pod-name> -n <namespace>
kubectl describe svc <service-name> -n <namespace>

## 🔐 Secrets & Configs
Use base64 for encoding sensitive data in Kubernetes secrets.

    echo -n 'username' | base64

## 🌟 Happy Deploying!
    yaml

