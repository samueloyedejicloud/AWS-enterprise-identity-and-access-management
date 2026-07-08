# Engineering Decisions

## Overview

Throughout the implementation of this project, several technical and operational decisions were made to balance security, scalability, and practical resource management.

The following decisions reflect both AWS best practices and the constraints of a personal learning environment.

---

## Decision 1: Centralized Identity Management

AWS IAM Identity Center was selected as the primary identity management service instead of managing permissions individually with IAM users across multiple accounts.

### Reason

Centralized identity management simplifies user administration and reduces the operational overhead of maintaining separate identities for each AWS account.

This approach also prepares the environment for future organizational growth.

---

## Decision 2: Permission Sets Instead of Direct User Permissions

Permission Sets were created before assigning permissions to users.

### Reason

Assigning permissions through Permission Sets provides consistency across multiple AWS accounts and reduces configuration errors.

This follows enterprise access management practices and supports future scalability.

---

## Decision 3: Group Based Access Control

Administrative permissions were assigned to groups rather than directly to users.

### Reason

Managing permissions through groups makes user onboarding and offboarding significantly easier.

As employees join or leave the organization, administrators only need to update group membership instead of modifying individual permissions.

This follows the Principle of Least Privilege and simplifies long term administration.

---

## Decision 4: Preserving AWS Free Tier Resources

The invitation sent to the demonstration user was intentionally left unaccepted.

### Reason

Additional email addresses were preserved for future AWS Free Tier environments and laboratory exercises.

This decision demonstrates responsible cloud resource planning while still allowing the identity management workflow to be documented.

---

## Decision 5: Multi Account Architecture

Separate Development and Support accounts were created within AWS Organizations.

### Reason

Separating workloads into different AWS accounts improves security boundaries, simplifies permission management, and aligns with AWS multi account best practices.

This design also prepares the environment for future expansion into additional business units such as Production, Security, and Shared Services.

---

## Conclusion

These engineering decisions were made to demonstrate practical enterprise cloud administration rather than simply completing a laboratory exercise.

The overall design emphasizes security, maintainability, scalability, and operational efficiency while remaining appropriate for a learning environment.
