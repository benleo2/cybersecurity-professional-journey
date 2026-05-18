# Docker Security

## What I Learned

Containers are not automatically secure.

Security depends on:
- image security
- container configuration
- user permissions
- secret management

---

## Important Concepts

### Non-Root Containers

Containers should avoid running as root.

Example:
```dockerfile
RUN useradd -m appuser
USER appuser
```

Benefit:
Limits attacker privileges if container is compromised.

---

### Slim Images

Using slim images reduces:
- unnecessary packages
- vulnerabilities
- attack surface

Example:
```dockerfile
FROM python:3.11-slim
```

---

### Vulnerability Scanning

Used Trivy to scan Docker images.

Example:
```
trivy image secure-app
```

---

### Secrets Management

Avoid hardcoding credentials in source code.

Bad:
```
password = "admin123"
```

Better:
```python
os.getenv("DB_PASSWORD")
```

---

## Security Improvements Implemented

- Added non-root container execution
- Used slim base image
- Performed Trivy vulnerability scanning
- Reduced attack surface

---

## Security Relevance

Docker security is important for:
- DevSecOps
- Kubernetes security
- cloud infrastructure security
- containerized applications
