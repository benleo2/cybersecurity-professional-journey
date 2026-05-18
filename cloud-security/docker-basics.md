# Docker Basics

## What is Docker?

Docker is a containerization platform used to package applications and their dependencies into isolated environments called containers.

Containers help applications run consistently across different systems.

---

## Important Concepts

### Image
A blueprint/template used to create containers.

Example:
```
docker pull python:3.11-slim
```

---

### Container
A running instance of an image.

Example:
```
docker run hello-world
```

---

### Dockerfile
A file containing instructions to build a Docker image.

Example:
```
FROM python:3.11-slim
COPY . .
RUN pip install -r requirements.txt
```

---

## Commands Practiced

### Check Docker Version
```
docker --version
```

### List Running Containers
```
docker ps
```

### List All Containers
```
docker ps -a
```

### Build Docker Image
```
docker build -t myapp .
```

### Run Container
```
docker run myapp
```

### Stop Container
```
docker stop <container_id>
```

---

## Security Relevance

Docker containers can become attack surfaces if:
- containers run as root
- vulnerable images are used
- secrets are exposed
- unnecessary ports are open

Understanding Docker is important for cloud security and DevSecOps.
