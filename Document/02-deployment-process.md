# Deployment Process

## Implementation Summary

This project was implemented using an AWS Management Account to simulate the cloud infrastructure of Latency IT Solutions. The objective was to establish centralized identity and access management using AWS Organizations and AWS IAM Identity Center.

---

## Step 1: Created the AWS Organization

An AWS Organization was created using the existing AWS Management Account.

Organization Name:

Latency IT Solutions

The management account serves as the central administration account responsible for managing member accounts, identity services, and organization level governance.

---

## Step 2: Created Member Accounts

Two member accounts were created inside the AWS Organization.

• Development Team Account

• Support Team Account

These accounts represent separate business environments and demonstrate how enterprise organizations isolate workloads between different departments.

---

## Step 3: Configured AWS IAM Identity Center

AWS IAM Identity Center was configured as the centralized identity management service for the organization.

This provides a single location for managing users, groups, and permissions across multiple AWS accounts.

---

## Step 4: Created Permission Sets

The following permission sets were created.

• Operators Access

Purpose:
Provides administrative access for cloud operations engineers responsible for managing AWS resources.

---

• Financial Access

Purpose:
Provides billing related permissions for the finance department while limiting access to infrastructure resources.

---

• Junior Engineer

Purpose:
Provides limited operational permissions appropriate for junior cloud engineers and DevOps trainees.

---

• Intern Engineer

Purpose:
Provides read only access for interns and trainees to safely explore the AWS environment without making infrastructure changes.

---

## Step 5: Created an Administrator Group

An Administrators group was created within AWS IAM Identity Center.

This group is intended for senior cloud engineers who require administrative permissions across multiple AWS accounts.

Using groups instead of assigning permissions directly to individual users simplifies long term user management.

---

## Step 6: Created an Identity Center User

A demonstration user named:

SammieLatency

was created within AWS IAM Identity Center.

The user represents an employee of Latency IT Solutions who can later be assigned to groups and permission sets.

---

## Step 7: Engineering Decision

The invitation email sent to the demonstration user was intentionally not accepted.

This decision preserves the associated email address for future AWS Free Tier and laboratory environments while still demonstrating the complete identity management workflow within the organization.

This approach reflects a practical engineering decision made during the implementation of this project.
