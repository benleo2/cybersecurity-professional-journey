# Container Networking

## What I Learned

Containers communicate using internal Docker networks.

Docker Compose automatically creates private networks for services.

---

## Example Architecture

Flask App <-> Redis Container

The Flask container communicates with Redis using:
```
host='redis'
```

Docker resolves the service name internally.

---

## Important Concepts

### Internal DNS
Docker automatically maps service names to container IP addresses.

### Isolation
Containers communicate inside isolated networks.

### Port Mapping
Example:
```
ports:
  - "5000:5000"
```

Format:
```
host_port:container_port
```

---

## Commands Practiced

### View Networks
```
docker network ls
```

### Inspect Networks
```
docker network inspect <network>
```

---

## Security Relevance

Networking affects:
- segmentation
- service exposure
- lateral movement
- attack surfaces

Proper isolation improves container security.
