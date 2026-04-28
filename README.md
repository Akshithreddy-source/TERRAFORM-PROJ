# Terraform AWS Infrastructure Setup

## Overview

This project demonstrates the creation of AWS infrastructure using Terraform. The setup includes networking components, storage backend, and resource configuration required for a scalable cloud environment.

---

## Resources Created

The following AWS resources were created:

* Virtual Private Cloud (VPC)
* Public and Private Subnets (across multiple Availability Zones)
* Internet Gateway
* NAT Gateway
* Route Tables (Public and Private)
* S3 Bucket (for Terraform remote backend)
* DynamoDB Table (for state locking)

---

## VPC Configuration

* VPC CIDR: `10.0.0.0/16`
* 2 Public Subnets:

  * `10.0.1.0/24` (ap-south-1a)
  * `10.0.2.0/24` (ap-south-1b)
* 2 Private Subnets:

  * `10.0.3.0/24` (ap-south-1a)
  * `10.0.4.0/24` (ap-south-1b)

This setup ensures high availability by distributing resources across multiple availability zones.

---

## Backend Configuration

### S3 Bucket

An S3 bucket is used to store Terraform state remotely. This helps in maintaining consistency and collaboration.

### DynamoDB Table

A DynamoDB table is used for state locking to prevent multiple users from making simultaneous changes.

---

## Screenshots

The following screenshots are included in this repository:

* VPC Configuration
* Subnets (Public and Private)
* S3 Bucket
* DynamoDB Table

  1.<img width="1902" height="803" alt="image" src="https://github.com/user-attachments/assets/5861f394-2372-4a68-947f-5e7137e7cce1" />
2.<img width="1912" height="820" alt="image" src="https://github.com/user-attachments/assets/53fe6c8a-3f0c-47ec-8c11-b6975db04e9c" />
3. <img width="1919" height="820" alt="image" src="https://github.com/user-attachments/assets/cd876a0f-e833-4df9-9106-91e75408d036" />
4. <img width="1919" height="769" alt="image" src="https://github.com/user-attachments/assets/81d61d2a-955f-48e4-af0c-a3eb26c65198" />


---

## Terraform Usage

Terraform was used to define and provision the infrastructure using Infrastructure as Code (IaC) principles.

All resources were created using Terraform configuration files and executed using:

* `terraform init`
* `terraform plan`
* `terraform apply`

---

## Reference

The resource configurations and structure were implemented by referring to the official Terraform Registry documentation:

https://registry.terraform.io/providers/hashicorp/aws/latest/docs

---

## Conclusion

This project demonstrates the use of Terraform to automate AWS infrastructure setup, including networking, backend configuration, and resource management. It highlights best practices such as modular design, use of variables, and remote state management.
