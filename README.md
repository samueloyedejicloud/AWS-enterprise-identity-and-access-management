# AWS-enterprise-identity-and-access-management
Designed and implemented an enterprise identity and access management solution using AWS Organizations, IAM Identity Center, IAM users, groups, permission sets, and AWS Organizations to demonstrate secure access management in a multi-account cloud environment.
# AWS Enterprise Identity and Access Management

## Project Overview

This project demonstrates the design and implementation of an enterprise Identity and Access Management (IAM) solution using Amazon Web Services (AWS).

The objective was to simulate how a growing technology company can securely manage cloud identities, user permissions, and account access across multiple AWS accounts using AWS Organizations and AWS IAM Identity Center.

Rather than treating AWS as a collection of individual services, this project focuses on designing an access management strategy that follows enterprise security best practices, including centralized identity management, role based access control, and least privilege access.



## Solution Architecture

The diagram below illustrates the enterprise identity and access management architecture implemented for **Latency IT Solutions**. The design demonstrates centralized governance using AWS Organizations, AWS IAM Identity Center, permission sets, user groups, and role based access control across multiple AWS accounts.

```text
                                   AWS Organization
                              Latency IT Solutions
                                        │
                         Management Account (Root)
                                        │
                  ┌─────────────────────┴─────────────────────┐
                  │                                           │
        AWS IAM Identity Center                    AWS Organizations
                  │                                           │
         ┌────────┴────────┐                    ┌─────────────┴───────────────┐
         │                 │                    │                             │
 Permission Sets      Identity Store      Development Account         Support Account
         │                 │                    │                             │
         │                 │                    │                             │
         │           Sammie Latency             │                             │
         │                 │                    │                             │
         └────────────┬────┘                    │                             │
                      │                         │                             │
               Administrators Group             │                             │
                      │                         │                             │
                      └──────────────Assigned Across AWS Accounts─────────────┘

Permission Sets
---------------
• Operations Access
• Financial Access
• Junior Engineer
• Intern Engineer
```

> **Note:** A graphical architecture diagram will be added in a future update. This text-based architecture is included to clearly document the implementation and relationships between AWS Organizations, IAM Identity Center, permission sets, groups, users, and member accounts.

## Solution Architecture

The diagram below illustrates the enterprise identity and access management architecture implemented for Latency IT Solutions.

![AWS IAM Architecture](diagram/aws-iam-architecture.png)
