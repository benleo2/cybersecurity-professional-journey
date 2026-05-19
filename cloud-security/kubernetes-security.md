# Kubernetes Security Fundamentals

## Why Kubernetes Security Matters

Kubernetes manages containers at scale.

Misconfigured Kubernetes environments can expose:
- applications
- APIs
- secrets
- internal services
- cloud infrastructure

Kubernetes security is a major area in cloud security and DevSecOps.

---

# Important Security Areas

## Namespaces

Namespaces isolate workloads inside a cluster.

Example:
- development
- testing
- production

Benefits:
- segmentation
- reduced blast radius
- access separation

### Commands Practiced

```
kubectl create namespace dev
kubectl get namespaces
```

---

## RBAC (Role-Based Access Control)

RBAC controls:
- who can access resources
- what actions they can perform

### Principle of Least Privilege

Users and services should only receive minimum required permissions.

---

## Example Role

```
apiVersion: rbac.authorization.k8s.io/v1
kind: Role

metadata:
  namespace: dev
  name: pod-reader

rules:
- apiGroups: [""]
  resources: ["pods"]
  verbs: ["get", "watch", "list"]
```

This role only allows viewing pods.

---

## Kubernetes Secrets

Secrets are used for:
- passwords
- API keys
- tokens
- credentials

### Example

```
kubectl create secret generic db-secret \
  --from-literal=password=mysecurepassword
```

---

## Important Note

Kubernetes secrets are base64 encoded by default.

Additional protection methods:
- encryption at rest
- HashiCorp Vault
- cloud secret managers

---

## Pod Security

Pods should avoid running as root.

### Example

```
securityContext:
  runAsNonRoot: true
```

Benefits:
- limits privilege escalation
- reduces impact of compromise

---

## Image Security

Container images should:
- come from trusted registries
- use slim/minimal images
- be scanned regularly

### Trivy Scanning

```
trivy image secure-app
```

Purpose:
- identify vulnerabilities
- reduce attack surface
- improve container security

---

## Service Exposure Risks

Improperly exposed services may:
- leak internal applications
- expose admin panels publicly
- increase attack surface

Example risky configuration:

```
type: LoadBalancer
```

for internal-only services.

---

## Key Security Concepts Learned

- least privilege
- segmentation
- container hardening
- vulnerability management
- secret management
- RBAC
- image scanning

---

## Security Relevance

Kubernetes security is important for:
- cloud security engineering
- DevSecOps
- platform engineering
- container security
- production infrastructure protection
