\# RFC-010 – Retire Legacy Workstation



\---



\# Apex Manufacturing, Inc.



\## Request for Change (RFC)



| Field | Value |

|--------|-------|

| RFC Number | RFC-010 |

| Change Type | Standard Change |

| Status | Completed |

| Priority | Medium |

| Requested By | IT Asset Management |

| Change Owner | Desktop Support Team |

| Assigned Technician | Kenyotta Eave |

| Date Submitted | September 12, 2026 |

| Scheduled Implementation | September 13, 2026 |

| Completion Date | September 13, 2026 |



\---



\# Change Summary



Retire a legacy Windows 10 workstation that has reached the end of its approved lifecycle and replace it with a newly provisioned enterprise-managed workstation.



The retired asset will be securely removed from production, sanitized according to company policy, and updated in the Configuration Management Database (CMDB).



\---



\# Business Justification



The existing workstation has exceeded its approved hardware lifecycle and no longer meets Apex Manufacturing's performance, reliability, and security standards.



Replacing the workstation improves:



\- System reliability

\- Security compliance

\- Employee productivity

\- Hardware standardization

\- Lifecycle management



\---



\# Asset Information



| Field | Value |

|--------|-------|

| Asset Tag | WS-1048 |

| Computer Name | FIN-WS-018 |

| Assigned User | Emily Carter |

| Department | Finance |

| Operating System | Windows 10 Enterprise |

| Replacement Device | FIN-WS-032 |

| Replacement OS | Windows 11 Enterprise |



\---



\# Systems Affected



\- Active Directory

\- Microsoft Entra ID

\- Microsoft Intune

\- Microsoft 365

\- BitLocker Recovery

\- Endpoint Protection

\- CMDB

\- Asset Inventory



\---



\# Scope



This change includes:



\- Verify replacement workstation

\- Backup user data

\- Migrate user profile

\- Remove workstation from Active Directory

\- Remove device from Microsoft Entra ID

\- Remove Intune enrollment

\- Verify BitLocker recovery information

\- Securely sanitize storage

\- Update Asset Inventory

\- Update CMDB



\---



\# Risk Assessment



\## Overall Risk



\*\*Low\*\*



\### Risks



\- Data migration failure

\- User profile corruption

\- Asset inventory inaccuracies

\- Device not properly removed from management platforms



\### Mitigation



\- Verify successful backup before migration

\- Validate user profile after migration

\- Confirm device removal from all management systems

\- Follow approved media sanitization procedures



\---



\# Impact Assessment



Business Impact



Low



User Impact



The assigned employee will receive a replacement workstation with minimal interruption to daily operations.



Expected Downtime



Approximately 30 minutes



Customer Impact



None



\---



\# Pre-Implementation Checklist



\- \[x] Replacement workstation prepared

\- \[x] Windows updates installed

\- \[x] BitLocker enabled

\- \[x] Microsoft Intune enrollment verified

\- \[x] User data backup completed

\- \[x] Department manager notified



\---



\# Implementation Plan



1\. Verify replacement workstation configuration.

2\. Perform full user data backup.

3\. Migrate user profile and documents.

4\. Join replacement workstation to the domain.

5\. Verify Microsoft Entra ID registration.

6\. Verify Intune compliance.

7\. Test Microsoft 365 applications.

8\. Remove legacy workstation from Active Directory.

9\. Remove device from Microsoft Entra ID.

10\. Remove Intune enrollment.

11\. Perform secure disk sanitization.

12\. Update Asset Inventory.

13\. Update CMDB.

14\. Prepare retired asset for recycling.

15\. Close change request.



\---



\# Validation Plan



The following validation activities were completed successfully.



\- User successfully logged into replacement workstation

\- Domain authentication verified

\- Microsoft 365 applications functioning normally

\- Network drives accessible

\- Finance department applications tested

\- Printer access verified

\- Legacy workstation removed from management platforms

\- Asset inventory updated

\- CMDB updated



Result:



\*\*Successful\*\*



\---



\# Rollback Plan



If implementation failed:



1\. Restore user profile to original workstation.

2\. Rejoin legacy workstation to the domain if required.

3\. Re-enroll device in Microsoft Intune.

4\. Restore Microsoft Entra ID registration.

5\. Verify user access.

6\. Escalate to Desktop Support Manager.



\---



\# Communication Plan



\## Before Implementation



\- Notify assigned employee

\- Notify Finance Manager

\- Notify Help Desk

\- Confirm replacement schedule



\## After Implementation



\- Confirm successful migration

\- Verify employee access

\- Provide new asset information

\- Archive retirement documentation



\---



\# Approval History



| Approver | Department | Status |

|----------|------------|--------|

| Michael Reynolds | Finance | Approved |

| Rachel Adams | IT Asset Management | Approved |

| David Brooks | IT Operations | Approved |



\---



\# Implementation Results



The workstation retirement completed successfully.



\- Replacement workstation deployed

\- User profile migrated

\- Microsoft 365 validated

\- Active Directory updated

\- Microsoft Entra ID updated

\- Intune enrollment verified

\- Legacy workstation securely sanitized

\- Asset inventory updated

\- CMDB updated



No issues were encountered during implementation.



\---



\# Post-Implementation Review



\## Objectives Met



\- Legacy workstation retired

\- Replacement workstation deployed

\- User productivity maintained

\- Asset records updated

\- Security standards maintained

\- No rollback required



\### Lessons Learned



Completing user profile validation before removing the legacy workstation from production ensured a seamless transition and prevented unnecessary downtime. Coordinating asset updates across Active Directory, Microsoft Entra ID, Intune, and the CMDB kept inventory records accurate and reduced administrative follow-up.



\---



\# Related Documentation



\- FORM-004-Hardware-Request.md

\- Infrastructure/Asset-Management/

\- Infrastructure/Active-Directory/

\- Infrastructure/Microsoft-365/

\- Asset-Inventory.md

\- Server-Inventory.md

\- CMDB.md

\- Change-Management-Policy.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial completed Request for Change documenting the retirement of a legacy enterprise workstation and deployment of its replacement. |

