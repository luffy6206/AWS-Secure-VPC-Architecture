# Secure AWS VPC Architecture with EC2

## Project Overview
This project demonstrates the design and implementation of a secure AWS Virtual Private Cloud (VPC)
with public and private subnets. The architecture follows AWS best practices for network isolation,
secure access, and controlled routing.

The setup includes EC2 instances deployed across different subnets, secure SSH access using key pairs,
and outbound-only internet access for private resources.

## Architecture Design
![Architecture Diagram](architecture-diagram.png)



## Key Components
- Amazon VPC with custom CIDR block
- Public and Private Subnets
- Internet Gateway
- NAT Gateway
- EC2 Instances
- Bastion Host
- Security Groups
- Network ACLs
- Route Tables
- IAM Roles and Policies

## Network Configuration
- Public subnets allow inbound internet traffic via Internet Gateway.
- Private subnets have no direct internet access and use NAT Gateway for outbound connectivity.
- Route tables are configured and associated with respective subnets to control traffic flow.

## Security Implementation
- Security Groups restrict inbound and outbound traffic at the instance level.
- Network ACLs provide subnet-level traffic control.
- Private EC2 instances do not have public IP addresses.
- SSH access to private EC2 instances is allowed only through a Bastion Host using PEM-based authentication.
- IAM roles are attached to EC2 instances to enforce least-privilege access to AWS services.

## Access Control
- SSH key pairs are generated and securely stored.
- SSH access is restricted to authorized sources only.
- IAM policies control access to AWS resources.

## Testing and Validation
- Verified SSH connectivity to public and private EC2 instances.
- Tested network communication between subnets.
- Validated routing, security group rules, and NACL configurations.

## Learning Outcomes
- Hands-on experience with AWS VPC design and networking
- Understanding of public vs private subnet isolation
- Secure access management using Bastion Host and IAM
- Practical knowledge of AWS routing and security mechanisms

## Author
Ashish Raj

