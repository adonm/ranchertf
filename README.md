# EKS with Rancher Deployment

This repository contains Terraform configurations to deploy an Amazon EKS cluster with Rancher installed, along with GitHub Actions for automated deployment to different environments.

## Prerequisites

- AWS account
- GitHub account
- Terraform installed locally for testing

## Repository Structure

- `.github/workflows/`: Contains GitHub Actions workflow
- `terraform/`: Contains Terraform configurations
- `environments/`: Contains environment-specific variables

## Setup

1. Fork this repository
2. Set up AWS credentials in GitHub secrets:
   - AWS_ACCESS_KEY_ID
   - AWS_SECRET_ACCESS_KEY
3. Customize the variables in `environments/*.tfvars` files
4. Push changes to trigger the GitHub Actions workflow

## Usage

- Push to `main` branch to trigger deployments
- The workflow will run `terraform plan` for all environments
- It will only apply changes to the `main` branch

## Customization

- Modify `terraform/main.tf` to change the infrastructure setup
- Adjust `terraform/variables.tf` for different input variables
- Update environment-specific `.tfvars` files in the `environments/` directory

## Notes

- This is a basic setup and should be enhanced for production use
- Ensure to implement proper security measures and follow AWS best practices