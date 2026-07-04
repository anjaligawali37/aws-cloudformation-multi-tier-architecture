# AWS CloudFormation Multi-Tier Architecture
![AWS](https://img.shields.io/badge/AWS-CloudFormation-orange?logo=amazonaws)
![YAML](https://img.shields.io/badge/Language-YAML-red)
![IaC](https://img.shields.io/badge/Infrastructure-as-Code-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## Project Overview

This project demonstrates how to provision a production-inspired AWS Multi-Tier Architecture entirely using AWS CloudFormation.

Instead of manually creating AWS resources through the AWS Management Console, the complete infrastructure is deployed as Infrastructure as Code (IaC) using a single CloudFormation YAML template.

The architecture consists of a highly available network with public and private subnets, a Bastion Host for secure administration, Application Load Balancer for traffic distribution, NAT Gateway for outbound internet access from private instances, and EC2 instances running Apache Web Server.

## Architecture

<p align="center">
<img src="architecture/multi-tier-architecture.png" width="100%">
</p>

## AWS Services Used

- Amazon VPC
- Public & Private Subnets
- Internet Gateway
- NAT Gateway
- Route Tables
- Security Groups
- IAM Role
- IAM Instance Profile
- Amazon EC2
- Application Load Balancer
- Target Group
- Listener
- Elastic IP
- AWS CloudFormation

## Architecture Components

✔ Custom VPC

✔ Two Public Subnets

✔ Two Private Subnets

✔ Internet Gateway

✔ NAT Gateway

✔ Public Route Table

✔ Private Route Table

✔ Bastion Host

✔ Two Private EC2 Instances

✔ Application Load Balancer

✔ Target Group

✔ Listener

✔ IAM Role

✔ Security Groups

## Folder Structure
aws-cloudformation-multi-tier-architecture/
│
├── templates/
│   └── infrastructure.yaml
│
├── architecture/
│   ├── multi-tier-architecture.png
│   └── README.md
│
├── screenshots/
│
├── docs/
│
├── LICENSE
├── README.md
└── .gitignore

## Features

- Infrastructure as Code (IaC)
- Fully Automated CloudFormation Deployment
- Highly Available Multi-AZ Architecture
- Public and Private Subnet Design
- Secure Bastion Host Access
- Private EC2 Administration via SSH
- Apache Web Server Deployment
- Application Load Balancer Integration
- Security Group Isolation
- NAT Gateway for Internet Access
- IAM Role-Based EC2 Permissions

## Deployment

1. Open AWS CloudFormation
2. Create Stack
3. Upload the CloudFormation YAML Template
4. Provide Stack Name
5. Select Existing Key Pair
6. Review Parameters
7. Acknowledge IAM Resources
8. Create Stack
9. Wait for CREATE_COMPLETE

## Secure SSH Workflow

Local Machine

↓

Bastion Host

↓

Private EC2 Instance

↓

Apache Web Server


## Validation

✔ Successfully created CloudFormation Stack

✔ Successfully created VPC

✔ Successfully created Public Subnets

✔ Successfully created Private Subnets

✔ Successfully created NAT Gateway

✔ Successfully created Bastion Host

✔ Successfully connected to Bastion Host

✔ Successfully connected to Private EC2 via SSH

✔ Successfully installed Apache Web Server

✔ Successfully configured Application Load Balancer

✔ Successfully served web pages through ALB

## Project Screenshots

All implementation screenshots are available in the **screenshots** folder.

- CloudFormation Stack Creation
- VPC Configuration
- Public & Private Subnets
- Security Groups
- Bastion Host
- Private EC2 Instances
- SSH to Private EC2
- Application Load Balancer
- Target Group
- Web Server Output

📂 See: [screenshots/README.md](screenshots/README.md)

## Learning Outcomes

This project provided practical experience with:

- AWS CloudFormation
- Infrastructure as Code (IaC)
- Amazon VPC Networking
- Multi-Tier Architecture Design
- Bastion Host Implementation
- NAT Gateway Configuration
- Application Load Balancer
- Security Group Design
- IAM Role Management
- EC2 Administration
- Linux Server Management

## Author

**Anjali Gawali**

LinkedIn:
https://www.linkedin.com/in/anjali-gawali-248b2a399/

GitHub:
https://github.com/anjaligawali37