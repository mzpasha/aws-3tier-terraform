# AWS 3-Tier Architecture using Terraform

## 🔧 Tools Used
* Terraform: To provision and manage AWS infrastructure declaratively.

* AWS: Cloud provider where the infrastructure is deployed.

* AWS CLI: For managing AWS resources and verifying deployments.

* Visual Studio Code / Any Code Editor: For writing Terraform code.

* Git: For version control of the Terraform code.

* Terraform Cloud or Local Backend: For state management.

* Optional: Postman / Browser to test the deployed application.

## 💡 Project Goal
To design and deploy a scalable, secure, and highly available 3-tier web application architecture on AWS using Infrastructure as Code (IaC) with Terraform.

## 🔍 Features
Infrastructure split into three tiers:

Web Tier: Public-facing Elastic Load Balancer (ELB) and EC2 instances running web servers.

Application Tier: EC2 instances or Auto Scaling Group running backend services.

Database Tier: Managed RDS instance for persistent storage.

Use of VPC, Subnets (public/private), Route Tables, and Security Groups to enforce network segmentation and security.

Auto Scaling setup for web and app tiers for scalability.

Use of IAM Roles for secure resource access.

Outputs like public DNS or ELB endpoint for testing.

Parameterization via Terraform variables.

Remote state management for collaboration.

## 📦 Folder Structure
aws-3tier-terraform/
│
├── modules/
│   ├── vpc/
│   │   └── main.tf, variables.tf, outputs.tf
│   ├── web-tier/
│   │   └── main.tf, variables.tf, outputs.tf
│   ├── app-tier/
│   │   └── main.tf, variables.tf, outputs.tf
│   ├── db-tier/
│   │   └── main.tf, variables.tf, outputs.tf
│
├── env/
│   ├── dev.tfvars
│   └── prod.tfvars
│
├── main.tf
├── variables.tf
├── outputs.tf
├── provider.tf
├── terraform.tfvars (optional)
├── README.md


## 🚀 How to Run
1 Install Terraform: Make sure Terraform is installed on your machine.

2 Configure AWS CLI with your AWS credentials.

3 Clone the repo (or create your own project folder).

4 Initialize Terraform to download required providers and modules:
terraform init

5 Plan the deployment to preview infrastructure changes:
terraform plan -var-file="env/dev.tfvars"

6 Apply the deployment to create infrastructure:
terraform apply -var-file="env/dev.tfvars"

7 Verify deployment by accessing the output ELB DNS or public IP.

8 Destroy the environment when done:
terraform destroy -var-file="env/dev.tfvars"


## 🧠 Learning Outcome
Understand how to architect a secure and scalable 3-tier architecture on AWS.

Gain hands-on experience writing reusable Terraform modules.

Learn network segmentation using VPC, subnets, and routing.

Implement security best practices with security groups and IAM roles.

Automate infrastructure provisioning using Terraform.

Practice state management and environment parameterization in Terraform.

Understand integration of different AWS services (EC2, ELB, RDS) in a single infrastructure.

Learn to use Terraform CLI commands effectively for deployment lifecycle.

