# Deployment Guide

## Prerequisites

- AWS Account
- Existing EC2 Key Pair
- IAM permissions for CloudFormation

---

## Step 1

Open AWS CloudFormation.

---

## Step 2

Choose **Create Stack**.

---

## Step 3

Upload the CloudFormation YAML template.

---

## Step 4

Enter a Stack Name.

---

## Step 5

Select your EC2 Key Pair.

---

## Step 6

Review parameters.

---

## Step 7

Acknowledge IAM resource creation.

---

## Step 8

Click **Create Stack**.

---

## Step 9

Wait until the stack reaches **CREATE_COMPLETE**.

---

## Step 10

Connect to the Bastion Host using SSH.

---

## Step 11

Connect from the Bastion Host to the private EC2 instances.

---

## Step 12

Install and configure Apache on both private instances.

---

## Step 13

Create an Application Load Balancer.

---

## Step 14

Register the private EC2 instances in the target group.

---

## Step 15

Access the Application Load Balancer DNS to verify successful load balancing.