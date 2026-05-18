# CI/CD Security

## What is CI/CD?

CI/CD stands for:
- Continuous Integration
- Continuous Deployment/Delivery

Used to automate:
- testing
- building
- security scanning
- deployments

---

## GitHub Actions

GitHub Actions automates workflows inside GitHub repositories.

Example workflow:
- build Docker image
- run Trivy vulnerability scan
- automate security checks

---

## Important Concepts

### Shift-Left Security

Security checks happen earlier during development.

Benefits:
- detect vulnerabilities early
- reduce deployment risks
- automate security validation

---

### GitHub Secrets

Sensitive data should be stored securely using GitHub Secrets.

Example:
```
env:
  API_KEY: ${{ secrets.API_KEY }}
```

---

### Supply Chain Security

Third-party GitHub Actions can introduce risks.

Better practice:
```
uses: aquasecurity/trivy-action@v0.28.0
```

instead of:
```
@master
```

---

## Security Pipeline Built

Implemented:
- Docker image build
- Trivy vulnerability scanning
- automated CI/CD security workflow

---

## Security Relevance

CI/CD systems are high-value targets because they may contain:
- cloud credentials
- deployment secrets
- production access

Pipeline security is an important DevSecOps area.
