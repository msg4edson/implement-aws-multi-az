# implement-aws-multi-az

## Overview

This repository contains Infrastructure as Code (IaC) to create a highly available and resilient AWS infrastructure using Terraform. The main goal is to set up two Virtual Private Clouds (VPCs) with subnets in two distinct Availability Zones (AZs) to ensure high availability and fault tolerance, following the principles of the AWS Well-Architected Framework.

## Infrastructure Details

- **Two VPCs**: One in the `us-east-1` region and another in the `us-west-1` region.
- **Subnets**: Each VPC will have public subnets spread across two Availability Zones.
- **High Availability**: By distributing resources across multiple AZs, the infrastructure is designed to be resilient to AZ failures.

## Instructions

To initialize the Terraform configuration, plan the deployment, and apply it, follow these steps:

1. Initialize the Terraform configuration:
    ```sh
    terraform init
    ```

2. Plan the Terraform deployment:
    ```sh
    terraform plan -out vpc.tfplan
    ```

3. Apply the deployment:
    ```sh
    terraform apply "vpc.tfplan"
    ```

For further assistance, refer to the Terraform documentation or seek help from the community.