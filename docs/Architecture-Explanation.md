# Architecture Explanation

## Overview

This project provisions a complete production-inspired AWS Multi-Tier Architecture using AWS CloudFormation.

The infrastructure is deployed as Infrastructure as Code (IaC), eliminating the need to manually create AWS resources.

---

## Architecture Components

### Amazon VPC

Creates an isolated network with CIDR block:

10.0.0.0/16

---

### Public Subnets

- Public Subnet 1
- Public Subnet 2

Resources inside public subnets receive public IP addresses.

---

### Private Subnets

- Private Subnet 1
- Private Subnet 2

Private instances are not directly accessible from the internet.

---

### Internet Gateway

Provides internet connectivity for resources in public subnets.

---

### NAT Gateway

Allows private EC2 instances to access the internet for updates without exposing them publicly.

---

### Route Tables

Public Route Table

0.0.0.0/0 → Internet Gateway

Private Route Table

0.0.0.0/0 → NAT Gateway

---

### Bastion Host

A secure EC2 instance deployed in a public subnet.

It acts as a jump server for securely accessing private EC2 instances through SSH.

---

### Security Groups

Bastion Security Group

- SSH (22) from Internet

Load Balancer Security Group

- HTTP (80) from Internet

Private EC2 Security Group

- SSH only from Bastion Host
- HTTP only from Load Balancer

---

### Application Load Balancer

Distributes incoming HTTP requests across private EC2 instances.

---

### Target Group

Registers both private EC2 instances as application targets.

---

### IAM Role

Provides AWS permissions to EC2 instances.

---

## Request Flow

User

↓

Application Load Balancer

↓

Private EC2 Instances

↓

Apache Web Server

---

## SSH Flow

Local Machine

↓

Bastion Host

↓

Private EC2 Instance