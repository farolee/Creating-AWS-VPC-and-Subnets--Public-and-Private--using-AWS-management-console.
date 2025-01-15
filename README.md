![Alt Screenshot(6).png]Screenshot(6).png

---
# AWS VPC Project - Ronny Global Services

## Project Overview
This project involved the creation of a secure and scalable Virtual Private Cloud (VPC) for **Ronny Global Services** using AWS resources. The VPC includes both **public** and **private subnets** distributed across two Availability Zones (AZs) to ensure **high availability** and **fault tolerance**. An **Internet Gateway** was attached to the VPC to enable Internet connectivity for the resources in the public subnet. Proper tagging was applied to all deployed resources for better organization and management.

---

## Architecture Diagram

*(Please refer to the attached reference diagram for the complete architecture layout.)*
---

## Resources Deployed

### 1. **VPC Creation**

- Created a new **VPC** using the AWS Management Console.
- **IPv4 CIDR Block**: `10.0.0.0/16`
- **Name Tag**: `RonnyGlobalVPC`

### 2. **Subnets Deployment**

- Deployed **two subnets**:
  - **Public Subnet** in **us-east-1a**
  - **Private Subnet** in **us-east-1b**
- Subnets were distributed across two Availability Zones for higher availability and fault tolerance.

#### Public Subnet:

- **CIDR Block**: `10.0.1.0/24`
- **Name Tag**: `PublicSubnet-AZ1`

#### Private Subnet:

- **CIDR Block**: `10.0.2.0/24`
- **Name Tag**: `PrivateSubnet-AZ2`

### 3. **Internet Gateway Attachment**

- An **Internet Gateway (IGW)** was created and attached to the VPC to enable internet connectivity for resources in the public subnet.
- **Name Tag**: Ronny GlobalITE

### 4. **Route Tables Configuration**

- Configured **Route Tables** to direct traffic appropriately:
  - **Public Route Table** with a route to the Internet Gateway for public subnet resources.
  - **Private Route Table** configured for internal communication.

### 5. **Tagging**

- Applied **proper tagging** to all deployed resources for easy identification and management.
  - **VPC**: `Name: RonnyGlobalVPC`
  - **Public Subnet**: `Name: RonnyGlobal_PublicSubnet-AZ1`
  - **Private Subnet**: `Name: RonnyGlobal_PrivateSubnet-AZ2`
  - **Internet Gateway**: `Name: RonnyGlobalIGW`

---

## High Availability and Fault Tolerance

- The use of two subnets across different **Availability Zones (AZs)** ensures that the infrastructure is highly available and resilient to failures.
- The public subnet is accessible from the internet, while the private subnet is isolated for sensitive workloads.

---

## Summary

This project successfully set up a **VPC** for **Ronny Global Services** with both public and private subnets, providing **internet connectivity** through an **Internet Gateway** and ensuring **high availability** by deploying resources across two Availability Zones. Proper resource tagging was applied to improve the management and visibility of AWS resources.

