# EKS with Rancher Deployment

This repository contains Terraform configurations to deploy an Amazon EKS cluster with Rancher installed, along with GitHub Actions for automated deployment to different environments.

## Prerequisites

- AWS account
- Codespaces or devcontainer to run in

## Repository Structure

- `terraform/`: Contains Terraform configurations
- `environments/`: Contains environment-specific variables
- TODO: `.github/workflows/`: Contains GitHub Actions workflow 


## Setup

1. Fork this repository
2. Set up AWS credentials (`aws configure sso`) for use in codespace
3. Customize the variables in `environments/*.tfvars` files

## Usage

```bash
cd terraform
terraform init
terraform plan --var-file=../environments/dev.tfvars
terraform apply
```

Resources can be cleaned up with `terraform destroy`.

## Customization

- Modify `terraform/main.tf` to change the infrastructure setup
- Adjust `terraform/variables.tf` for different input variables
- Update environment-specific `.tfvars` files in the `environments/` directory