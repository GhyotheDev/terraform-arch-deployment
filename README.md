# Terraform AWS Infrastructure Practice

Practicing AWS infrastructure deployment using Terraform with CI/CD automation.

## What I'm Learning

- **Terraform Modules**: Modular infrastructure code organization
- **S3 Backend**: Remote state management with versioning and encryption
- **State Locking**: DynamoDB table for concurrent access protection
- **VPC Architecture**: Multi-AZ networking with public/private subnets
- **GitHub Actions**: Automated CI/CD pipeline for infrastructure deployment

## Project Structure

```
src/
├── main.tf              # Root configuration with S3 backend
├── locals.tf            # Local variables
└── modules/
    ├── tf-state/        # S3 bucket and DynamoDB table
    └── vpc/             # VPC, subnets, and networking
```

## Deployment Process

1. Comment out S3 backend in `main.tf`
2. Run `terraform init && terraform apply` (creates S3/DynamoDB)
3. Uncomment S3 backend
4. Run `terraform init && terraform apply` (migrates to remote state)

## Skills Practiced

- Infrastructure as Code (IaC)
- Remote state management
- Terraform best practices
- AWS networking fundamentals
- CI/CD automation