# AWS Identity and Access Management (IAM)

## Overview

AWS Identity and Access Management (IAM) is a service that enables secure access management for AWS resources. It allows administrators to control who can access AWS services and what actions they can perform by using users, groups, roles, and policies.

---

## Learning Objectives

After completing this module, I was able to:

- Understand the purpose of AWS IAM
- Create and manage IAM Users
- Create and manage IAM Groups
- Understand IAM Roles and Service Roles
- Create and attach IAM Policies
- Learn the IAM Policy Structure
- Configure Password Policies
- Enable Multi-Factor Authentication (MFA)
- Understand Access Keys
- Explore IAM Security Tools
- Generate IAM Credentials Report
- Use IAM Access Advisor
- Follow the Principle of Least Privilege

---

## Topics Covered

- IAM Overview
- IAM Users
- IAM Groups
- IAM Roles
- IAM Service Roles
- IAM Policies
- Policy Structure
  - Version
  - Statement
  - Effect
  - Action
  - Resource
  - Condition
  - Principal
- Password Policy
- Multi-Factor Authentication (MFA)
- Access Keys
- IAM Credentials Report
- IAM Access Advisor
- AWS CLI for IAM
- IAM Best Practices

---

## Hands-on Labs Completed

- Created IAM Users
- Created IAM Groups
- Added Users to Groups
- Attached AWS Managed Policies
- Created Custom IAM Policies
- Tested S3 Read-Only Access
- Observed Access Denied Errors
- Enabled MFA
- Explored IAM Credentials Report
- Explored IAM Access Advisor

---

## AWS CLI Commands Practiced

```bash
aws iam list-users

aws iam list-groups

aws iam list-policies

aws iam get-user

aws iam list-roles
```

---

## Key Concepts Learned

- Authentication vs Authorization
- Identity-based Policies
- Resource-based Policies
- Least Privilege Principle
- Temporary Credentials
- IAM Service Roles
- AWS Managed Policies
- Customer Managed Policies
- Inline Policies

---

## Skills Gained

- Identity and Access Management
- User and Group Management
- Permission Management
- Security Best Practices
- IAM Policy Creation
- AWS CLI Basics

---

## Folder Structure

```
IAM/
│
├── README.md
├── Notes/
├── Policies/
├── Hands-On-Labs/
├── CLI-Commands/
└── Screenshots/
```

---

## Screenshots

This folder contains screenshots of:

- IAM Dashboard
- Creating IAM Users
- Creating IAM Groups
- Attaching Policies
- IAM Roles
- MFA Configuration
- Access Denied Example
- Credentials Report
- Access Advisor

---

## Interview Preparation

This module helped me understand:

- How AWS manages identities
- How permissions are granted using policies
- How IAM Roles provide temporary credentials
- How to secure AWS accounts using MFA and Password Policies
- IAM security tools and best practices

---

## Summary

AWS IAM is the foundation of AWS security. It enables secure authentication and authorization by controlling access to AWS resources through users, groups, roles, and policies while following the Principle of Least Privilege.