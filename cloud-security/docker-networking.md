# Docker Networking

## What I Learned

Docker Compose automatically creates internal networks between containers.

Containers communicate using service names as hostnames.

Example:
```
redis.Redis(host='redis', port=6379)
```

---

## Important Concepts

### Bridge Network
Default Docker network type used for communication between containers.

### Internal DNS
Docker automatically resolves container names to IP addresses.

### Multi-Container Communication
Containers can securely communicate inside isolated Docker networks.

---

## Commands Practiced

### List Networks
```
docker network ls
```

### Inspect Network
```
docker network inspect <network-name>
```

---

## Troubleshooting Experience

Problem:
Flask container exited before Redis was fully ready.

Solution:
Implemented retry logic using Python and time.sleep().

---

## Security Relevance

Container networking affects:
- segmentation
- isolation
- attack surface reduction
- lateral movement prevention

Misconfigured networking can expose internal services publicly.
