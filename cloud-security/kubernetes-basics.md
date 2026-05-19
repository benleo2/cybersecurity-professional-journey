# Kubernetes Basics

## What is Kubernetes?

Kubernetes is a container orchestration platform used to deploy, manage, scale, and recover containerized applications automatically.

Docker creates containers.

Kubernetes manages containers at scale.

---

## Important Concepts

### Pod

The smallest deployable unit in Kubernetes.

Pods usually contain one or more containers.

---

### Node

A machine (virtual or physical) that runs workloads.

---

### Cluster

A group of nodes managed together.

---

### Deployment

Manages pods automatically.

Provides:
- scaling
- updates
- self-healing

---

### Service

Provides stable networking access to pods.

---

## Commands Practiced

### Start Minikube
```
minikube start
```

### Check Nodes
```
kubectl get nodes
```

### Check Pods
```
kubectl get pods
```

### Check Deployments
```
kubectl get deployments
```

### Check Services
```
kubectl get services
```

---

## What I Built

- Deployed Flask application into Kubernetes
- Created Deployment with 2 replicas
- Created Service for external access
- Tested Kubernetes self-healing

---

## Security Relevance

Kubernetes security is important because clusters may expose:
- APIs
- containers
- secrets
- networking
- IAM/RBAC configurations

Misconfigured Kubernetes environments are common cloud attack surfaces.
