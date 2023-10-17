# Terraform Bastion Infrastructure

![Terraform Bastion Infrastructure](https://your-image-url.com/your-image.png)

## Introduction

The **terraform-bastion-infra** project is a Terraform configuration that creates a secure and flexible infrastructure setup for deploying projects that require a bastion host. This infrastructure is designed to mimic the bastion host topology, offering a secure environment for project deployment.

If you need to use this Terraform configuration, please make necessary adjustments to the resources to fit your specific requirements.

## Resources Included

This Terraform infrastructure includes the following AWS resources:

- **VPC (Virtual Private Cloud)**: A logically isolated section of AWS Cloud where you can launch AWS resources.

- **Internet Gateway (IG)**: A horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet.

- **Public Subnet**: A subnet with a route to the internet via the Internet Gateway, suitable for hosting public-facing resources.

- **Private Subnet**: A subnet without direct internet access, ideal for hosting internal resources.

- **Route Table**: Associating route tables with subnets to control the traffic flow.

- **2 EC2 Instances**: Virtual machines used as bastion hosts for secure access to other resources in the private subnet.

- **Elastic IP**: A static, public IPv4 address for use with the EC2 instances.

- **NAT Gateway**: Enables instances in a private subnet to initiate outbound traffic to the internet while preventing unsolicited inbound traffic from the internet.

- **Security Group**: Includes ingress and egress rules to control incoming and outgoing traffic for your EC2 instances.

## Usage

Follow these steps to create the infrastructure using Terraform:

### Prerequisites

Before you start, make sure you have the following prerequisites:

- **Terraform**: If you haven't already, install Terraform by following the official [Terraform installation guide](https://learn.hashicorp.com/tutorials/terraform/install-cli).

- **AWS CLI**: Configure your AWS credentials using the AWS CLI with `aws configure`.

### Deployment

1. Clone the repository:

   ```shell
   git clone https://github.com/czlazlo/terraform-bastion-infra.git
2. Initialize Terraform:
  terraform init
3. Apply the Terraform configuration to create the infrastructure:
  terraform apply


Security Considerations
This infrastructure is designed with security in mind, but it's important to review and enhance security measures based on your project's requirements and AWS best practices.

Cleanup
When you are done using the infrastructure, you can tear down the resources created by Terraform:
  terraform destroy


