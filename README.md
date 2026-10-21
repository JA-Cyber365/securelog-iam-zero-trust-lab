# SecureLogix IAM Zero Trust Lab

## Objective

This lab simulates an identity lifecycle management environment using Microsoft Entra ID, following the Joiner-Mover-Leaver (JML) framework. The goal was to provision and manage user identities, assign role-based access control (RBAC), and enforce Zero Trust principles — documented using GRC methodology to demonstrate compliance-aligned identity governance.

### Skills Learned

- Identity lifecycle management using the Joiner-Mover-Leaver (JML) framework
- User provisioning and de-provisioning in Microsoft Entra ID
- Role-Based Access Control (RBAC) assignment and principle of least privilege
- Group-based access management and policy scoping
- Multi-Factor Authentication (MFA) enforcement as a Zero Trust control
- GRC documentation of identity and access management controls

### Tools Used

- Microsoft Entra ID (Azure Active Directory) — identity provisioning, RBAC, MFA
- Microsoft Entra Admin Center — user and group management interface

## Steps

### User Provisioning — Joiner Workflow

*Step 1: Create new user (Sarah Mitchell)*

![Create New User](screenshots/user/01-create-user-sarah-mitchell.png)

New user Sarah Mitchell provisioned in Microsoft Entra ID. The Review + create screen confirms the User Principal Name (UPN), display name, account status set to enabled, and user type set to Member — consistent with a standard Joiner workflow onboarding a new employee.

*Step 2: Users list — provisioned identities*

![Users List](screenshots/user/02-users-list.png)

Entra ID users list confirming five active identities: Alex Rivera, David Chen, James Thornton, Jaun Miller, and Sarah Mitchell. This view demonstrates the current identity inventory managed within the SecureLogix tenant.

### Group Management — Access Scoping

*Step 3: [Coming soon]*

### MFA Enforcement — Zero Trust Control

*Step 4: [Coming soon]*

## Findings Summary

| Control Area | Action Taken | Framework Reference |
|---|---|---|
| User Provisioning | New user onboarded via JML Joiner workflow | NIST SP 800-53 AC-2 |
| RBAC | Role assigned based on least privilege | NIST SP 800-53 AC-6 |
| MFA | MFA enforced for all users | NIST SP 800-53 IA-5 |
