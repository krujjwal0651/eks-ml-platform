# Terraform CI/CD with GitHub Actions

## Project Overview

This project demonstrates a production-style workflows for managing AWS infrastructure using:

    - Terraform
    - GitHub Actions
    - AWS OIDC Authentication
    - GitHub Environment Protection Rules

The repository is designed to showcase modern Infrastructure-as-Code (IaC) CI/CD practices used by Platform Engineering, DevOps, and SRE teams.

The current implementation focuses on a **Development Environment (`dev`)** and includes complete Terraform automation workflows for:

    - Terraform Plan
    - Terraform Apply
    - Terraform Destroy

The workflows are designed with:
    - security
    - approval gates
    - concurrency protection
    - artifact handling
    - GitOps workflow patterns

---

# Architecture Overview

```text
Developer
   |
   v
Feature Branch
   |
   v
Terraform Plan Workflow
   |
   v
Pull Request → main
   |
   v
Terraform Plan Validation
   |
   v
Manual Review / Approval
   |
   v
Merge to main
   |
   v
Terraform Apply Workflow
   |
   v
AWS Infrastructure Deployment
   |
   v
Manual Destroy Workflow (Optional)
