# Terraform Basics

## What is Terraform?

Terraform is an Infrastructure as Code (IaC) tool used to automate infrastructure creation and management.

Terraform allows infrastructure to be defined using code.

---

## Important Concepts

### Infrastructure as Code (IaC)

Infrastructure is managed through code instead of manual configuration.

Benefits:
- automation
- consistency
- version control
- repeatability

---

### Terraform Configuration

Terraform uses `.tf` files.

Example:
```
resource "local_file" "example" {
  content  = "Hello Terraform"
  filename = "example.txt"
}
```

---

## Commands Practiced

### Initialize Terraform
```
terraform init
```

### Preview Changes
```
terraform plan
```

### Apply Changes
```
terraform apply
```

### Destroy Resources
```
terraform destroy
```

---

## Security Relevance

Terraform helps:
- standardize infrastructure
- reduce manual mistakes
- improve auditing
- automate cloud deployments

Misconfigured IaC can create security risks if permissions are too broad.
