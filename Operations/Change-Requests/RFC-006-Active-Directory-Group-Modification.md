\# RFC-006 – Active Directory Group Modification



\---



\# Apex Manufacturing, Inc.



\## Request for Change (RFC)



| Field | Value |

|--------|-------|

| RFC Number | RFC-006 |

| Change Type | Normal Change |

| Status | Completed |

| Priority | Medium |

| Requested By | Human Resources |

| Change Owner | Identity \& Access Management Team |

| Assigned Technician | Kenyotta Eave |

| Date Submitted | August 15, 2026 |

| Scheduled Implementation | August 16, 2026 |

| Completion Date | August 16, 2026 |



\---



\# Change Summary



Modify Active Directory security group memberships for an employee transferring from the Human Resources department to the Finance department.



The change includes removing legacy permissions, assigning new department security groups, validating access, and updating enterprise documentation.



\---



\# Business Justification



The employee has accepted a new role within the Finance Department.



To maintain the Principle of Least Privilege, all Human Resources permissions must be removed and replaced with Finance-specific access.



\---



\# Employee Information



| Field | Value |

|--------|-------|

| Employee Name | Emily Carter |

| Employee ID | EMP-10381 |

| Username | ecarter |

| Previous Department | Human Resources |

| New Department | Finance |

| Manager | Michael Reynolds |



\---



\# Systems Affected



\- DC01 Domain Controller

\- Active Directory

\- Group Policy

\- FILE01 File Server

\- Microsoft Entra ID

\- Microsoft 365

\- CMDB



\---



\# Scope



This change includes:



\- Remove HR security groups

\- Add Finance security groups

\- Verify Group Policy processing

\- Validate shared drive permissions

\- Verify Microsoft 365 access

\- Update Employee Directory

\- Update CMDB



\---



\# Existing Group Memberships



\- HR\_Users

\- HR\_FileShare\_RW

\- HR\_Printers

\- All\_Employees



\---



\# New Group Memberships



\- Finance\_Users

\- Finance\_FileShare\_RW

\- Finance\_Printers

\- Finance\_Teams

\- All\_Employees



\---



\# Risk Assessment



\## Overall Risk



\*\*Low\*\*



\### Risks



\- Incorrect security group assignment

\- Delayed Active Directory replication

\- Temporary access interruption

\- Incorrect file permissions



\### Mitigation



\- Review requested permissions with department manager

\- Verify replication after changes

\- Validate access before closing change

\- Maintain audit log of all modifications



\---



\# Impact Assessment



Business Impact



Low



User Impact



The employee may briefly lose access to department resources while group memberships replicate.



Expected Downtime



Less than 10 minutes



Customer Impact



None



\---



\# Pre-Implementation Checklist



\- \[x] HR approval received

\- \[x] Finance manager approval received

\- \[x] Group memberships reviewed

\- \[x] Current memberships documented

\- \[x] Backup of user group assignments completed



\---



\# Implementation Plan



1\. Verify employee identity.

2\. Review approved access request.

3\. Record current group memberships.

4\. Remove Human Resources security groups.

5\. Add Finance security groups.

6\. Force Active Directory replication.

7\. Verify Group Policy update.

8\. Validate Finance shared drive access.

9\. Validate Microsoft Teams access.

10\. Update Employee Directory.

11\. Update CMDB.

12\. Close Help Desk ticket.



\---



\# Validation Plan



The following validation activities were completed successfully.



\- Active Directory updated

\- Group memberships verified

\- Group Policy processed successfully

\- Finance file shares accessible

\- HR resources no longer accessible

\- Teams access verified

\- Microsoft 365 login successful



Result:



\*\*Successful\*\*



\---



\# Rollback Plan



If implementation failed:



1\. Remove Finance security groups.

2\. Restore original HR group memberships.

3\. Force Active Directory replication.

4\. Verify previous access restored.

5\. Notify department managers.

6\. Escalate to Identity \& Access Management.



\---



\# Communication Plan



\## Before Implementation



\- Notify Human Resources

\- Notify Finance Manager

\- Notify employee



\## After Implementation



\- Confirm successful access

\- Update Help Desk ticket

\- Notify department managers

\- Archive change documentation



\---



\# Approval History



| Approver | Department | Status |

|----------|------------|--------|

| Emily Carter | Human Resources | Approved |

| Michael Reynolds | Finance | Approved |

| David Brooks | IT Operations | Approved |



\---



\# Implementation Results



The Active Directory modification was completed successfully.



\- Legacy permissions removed

\- Finance access granted

\- Group Policy updated successfully

\- File server permissions validated

\- No service interruptions observed



\---



\# Post-Implementation Review



\## Objectives Met



\- Department transfer completed

\- Principle of Least Privilege maintained

\- Active Directory updated

\- Enterprise documentation updated

\- No rollback required



\### Lessons Learned



Documenting existing group memberships before making changes simplified validation and would have allowed rapid recovery if a rollback had been required.



\---



\# Related Documentation



\- FORM-001-User-Access-Request.md

\- FORM-002-New-Employee-Onboarding-Request.md

\- Infrastructure/Active-Directory/

\- Infrastructure/Servers/

\- Employee-Directory.md

\- CMDB.md

\- Security-Policies.md

\- Change-Management-Policy.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | August 2026 | Kenyotta Eave | Initial completed Request for Change documenting Active Directory group membership modification following an employee department transfer. |

