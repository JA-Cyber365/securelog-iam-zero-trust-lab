# SecureLogix Inc — JML Workflow
## Joiner-Mover-Leaver Identity Lifecycle Management
### Created: September 2026

---

## 1. JOINER — New Employee Onboarding

**Scenario:** Sarah Mitchell joins as HR Analyst  
**Trigger:** Signed offer letter received by HR

| Step | Action | Responsible | Timing |
|---|---|---|---|
| 1 | Create user account in Entra ID | IT Admin | Before start date |
| 2 | Assign to GRP-HR-Standard security group | IT Admin | Before start date |
| 3 | Enable per-user MFA | IT Admin | Before start date |
| 4 | Send temporary credentials to user | IT Admin / HR | Day of start |
| 5 | Confirm user can sign in successfully | IT Admin | Day of start |
| 6 | Document account creation in audit log | IT Admin | Day of start |

---

## 2. MOVER — Role Change

**Scenario:** James Thornton promoted from Finance Analyst to Finance Manager  
**Trigger:** HR confirms role change effective date

| Step | Action | Responsible |
|---|---|---|
| 1 | Review current access against new role requirements | IT Admin |
| 2 | Remove any access no longer required | IT Admin |
| 3 | Update job title and department in Entra ID | IT Admin |
| 4 | Assign additional permissions required for new role | IT Admin |
| 5 | Update group membership if required | IT Admin |
| 6 | Notify user of access changes | IT Admin / HR |
| 7 | Document changes in audit log | IT Admin |
| 8 | Schedule 30-day access review | IT Admin |

**Key principle:** Never accumulate permissions — remove old access before granting new access.

---

## 3. LEAVER — Offboarding

**Scenario:** Alex Rivera's contractor engagement ends  
**Trigger:** Contract end date reached or early termination notice

| Step | Action | Responsible | Timing |
|---|---|---|---|
| 1 | Disable sign-in immediately | IT Admin | Same day |
| 2 | Revoke all active sessions | IT Admin | Same day |
| 3 | Remove from all groups | IT Admin | Same day |
| 4 | Reset account password | IT Admin | Same day |
| 5 | Review and export audit logs | IT Admin | Within 24 hours |
| 6 | Transfer any owned files to manager | IT Admin | Within 48 hours |
| 7 | Delete account after retention period | IT Admin | 30 days |
| 8 | Document offboarding completion | IT Admin | Within 48 hours |

**Critical:** Disable account BEFORE or AT the moment of notification — never after.

---

## 4. Access Review Checklist

Conducted quarterly for all accounts:

| Question | Action if No |
|---|---|
| Does this user still work here? | Offboard immediately |
| Does this user still need this access? | Remove unnecessary access |
| Is this access appropriate for their role? | Adjust to match current role |
| Are there any risk flags on this account? | Investigate and document |
| Is access documented and approved? | Update documentation |

---

## 5. Privileged Access Review

For IT Admin and Global Admin accounts — reviewed monthly:

| Check | Details |
|---|---|
| Admin actions reviewed | Review audit logs for all privileged actions |
| Unnecessary privileges removed | Remove any access beyond current requirements |
| JIT access verified | Confirm temporary access was revoked after use |
| MFA compliance verified | Confirm MFA active on all privileged accounts |

---

## Summary

| Event | Key Action | Timing |
|---|---|---|
| Joiner | Create account, assign group, enable MFA | Before start date |
| Mover | Remove old access, assign new access | Effective date of change |
| Leaver | Disable account, revoke sessions, remove groups | Same day as departure |

---

*Document prepared by: Jaun Miller — Global Administrator, SecureLogix Inc*  
*Date: September 2026*  
*Framework reference: NIST SP 800-53 AC-2 Account Management*
