# SecureLogix Inc — RBAC Matrix
## Identity & Access Management Lab
### Created: September 2026

---

## Company Overview

**Organisation:** SecureLogix Inc  
**Industry:** Financial Services  
**Environment:** Microsoft Entra ID (Azure AD)  
**Administrator:** Jaun Miller — Global Administrator  

---

## Security Principle

All access decisions follow the **Least Privilege** principle — users receive only the minimum access required to perform their job function. No user has access to systems outside their defined role.

---

## User Roles and Departments

| User | Role | Department | Account Type |
|---|---|---|---|
| Sarah Mitchell | HR Analyst | Human Resources | Standard Member |
| James Thornton | Finance Manager | Finance | Standard Member |
| Alex Rivera | Contractor | Operations | External Contractor |
| David Chen | IT Administrator | Information Technology | Privileged Member |
| Jaun Miller | Global Administrator | IT/Executive | Global Admin |

---

## Group Assignments

| Group | Members | Purpose |
|---|---|---|
| GRP-HR-Standard | Sarah Mitchell | Standard HR department access |
| GRP-Finance-Standard | James Thornton | Standard Finance department access |
| GRP-Contractors | Alex Rivera | Limited time-restricted contractor access |
| GRP-IT-Admins | David Chen | Privileged IT administrator access |

---

## RBAC Access Matrix

| Resource | Sarah Mitchell (HR) | James Thornton (Finance) | Alex Rivera (Contractor) | David Chen (IT Admin) | Jaun Miller (Global Admin) |
|---|---|---|---|---|---|
| **Files / SharePoint** | Read Only | Read Only | Limited Read | Full Access | Full Access |
| **HR Systems** | Full Access | No Access | No Access | Read Only | Full Access |
| **Finance Systems** | No Access | Full Access | No Access | Read Only | Full Access |
| **Admin Portal** | No Access | No Access | No Access | Full Access | Full Access |
| **Security Tools** | No Access | No Access | No Access | Full Access | Full Access |
| **Email / M365** | Full Access | Full Access | Limited Access | Full Access | Full Access |

---

## Access Level Definitions

| Level | Description |
|---|---|
| **Full Access** | Read, write, modify and delete permissions |
| **Read Only** | View permissions only — no modifications |
| **Limited Access** | Restricted read access to specific resources only |
| **No Access** | Completely blocked — cannot view or interact |

---

## Privileged Access Process

For IT Admin and Global Admin privileged actions:

1. Submit access request with business justification
2. Manager or admin approves the request
3. Temporary elevated access granted (Just In Time)
4. Task completed within approved window
5. Access automatically revoked when window closes
6. Action logged in Audit logs for review

---

## Least Privilege Justification

| User | Why Access Is Limited |
|---|---|
| Sarah Mitchell | HR Analyst requires HR systems only — no financial data access needed |
| James Thornton | Finance Manager requires Finance systems only — no HR data access needed |
| Alex Rivera | Contractor with limited engagement — minimal access, time-restricted |
| David Chen | IT Admin requires broad technical access — no business data modification rights |
| Jaun Miller | Global Admin — full access required for tenant management only |

---

## Security Controls Applied

| Control | Status | Details |
|---|---|---|
| MFA — All Users | ✅ Enabled | Per-user MFA enabled for all five accounts |
| Security Defaults | ✅ Enabled | Tenant-wide baseline security enforced |
| Group-based Access | ✅ Configured | Four security groups controlling resource access |
| Least Privilege | ✅ Applied | Each role mapped to minimum required permissions |
| Audit Logging | ✅ Active | All sign-in and admin actions logged in Entra ID |

---

## Planned Conditional Access Policies

*Note: These policies were designed as part of the Zero Trust implementation. Full Conditional Access requires Entra ID P1 licensing.*

**Policy 1 — Require MFA Outside Company Network**
- Condition: User signs in from outside named/trusted location
- Control: Require MFA verification
- Applies to: All users
- Zero Trust principle: Verify explicitly

**Policy 2 — Block Contractor Access Outside Business Hours**
- Condition: GRP-Contractors group + sign-in time outside 9AM–5PM EST
- Control: Block access entirely
- Applies to: Alex Rivera
- Zero Trust principle: Least privilege + Just in time

**Policy 3 — Require Compliant Device for Admin Access**
- Condition: IT Admin or Global Admin role + admin portal access
- Control: Require Intune compliant or domain-joined device
- Applies to: David Chen, Jaun Miller
- Zero Trust principle: Verify explicitly

---

## Zero Trust Principles Demonstrated

| Principle | Implementation |
|---|---|
| **Verify Explicitly** | MFA enforced for all users, Security Defaults active |
| **Least Privilege** | RBAC matrix limits access to role requirements only |
| **Assume Breach** | Audit logging active, access reviews planned quarterly |

---

*Document prepared by: Jaun Miller — Global Administrator, SecureLogix Inc*  
*Date: September 2026*  
*Lab environment: Microsoft Entra ID Free Tier*
