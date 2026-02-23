# 🚀 Terraform AWS ECS Infrastructure with CI

This project provisions a complete AWS containerized application
infrastructure using Terraform and implements Continuous Integration
using GitHub Actions.

------------------------------------------------------------------------

# 🏗 Architecture Overview

Internet\
↓\
Application Load Balancer (Public Subnet)\
↓\
ECS Fargate Service (Private Subnet)\
↓\
ECS Cluster\
↓\
IAM Task Role

------------------------------------------------------------------------

# 📦 What This Project Provisions

-   VPC with Public & Private Subnets
-   Security Groups (ALB & ECS)
-   IAM Roles (Execution + Task Role)
-   Application Load Balancer
-   ECS Cluster (Fargate)
-   ECS Service (NGINX container)
-   GitHub Actions CI Pipeline

------------------------------------------------------------------------

# 📁 Project Structure

. ├── main.tf\
├── variables.tf\
├── outputs.tf\
├── modules/\
│ ├── vpc/\
│ ├── security-groups/\
│ ├── iam/\
│ ├── alb/\
│ └── ecs/\
└── .github/workflows/terraform-ci.yml

------------------------------------------------------------------------

# 🛠 Prerequisites

-   Terraform \>= 1.6
-   AWS CLI configured (`aws configure`)
-   Git installed
-   GitHub repository created

------------------------------------------------------------------------

# 🚀 Implementation Process (Step-by-Step)

## 1️⃣ Clone Repository

git clone `<your-repo-url>`{=html}\
cd terraform-ecs-app

------------------------------------------------------------------------

## 2️⃣ Initialize Terraform

terraform init

------------------------------------------------------------------------

## 3️⃣ Validate Configuration

terraform validate

------------------------------------------------------------------------

## 4️⃣ Preview Infrastructure Changes

terraform plan

------------------------------------------------------------------------

## 5️⃣ Apply Infrastructure

terraform apply

After successful apply, Terraform will output:

alb_dns_name

Open it in your browser to see the NGINX welcome page.

------------------------------------------------------------------------

# 🔄 Continuous Integration (CI)

GitHub Actions workflow automatically runs on:

-   Push to main branch
-   Pull requests

Pipeline executes:

-   terraform fmt -check
-   terraform init
-   terraform validate
-   terraform plan

Workflow file:

.github/workflows/terraform-ci.yml

------------------------------------------------------------------------

# 🔐 Adding AWS Credentials to GitHub

1.  Go to GitHub → Repository → Settings → Secrets and variables →
    Actions\
2.  Add:
    -   AWS_ACCESS_KEY_ID\
    -   AWS_SECRET_ACCESS_KEY

------------------------------------------------------------------------

# 🧹 Destroy Infrastructure

To avoid AWS charges:

terraform destroy

------------------------------------------------------------------------

# 🎯 Learning Outcomes

This project demonstrates:

-   Infrastructure as Code (IaC)
-   Terraform modular architecture
-   AWS ECS with Fargate
-   Load balancing with ALB
-   IAM role management
-   CI with GitHub Actions
-   DevOps best practices

------------------------------------------------------------------------

# 👨‍💻 Author

Mayank Pandey\
DevOps & Cloud Engineering Journey
