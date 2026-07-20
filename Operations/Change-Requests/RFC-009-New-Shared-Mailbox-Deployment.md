\# RFC-009 – New Shared Mailbox Deployment



\---



\# Apex Manufacturing, Inc.



\## Request for Change (RFC)



| Field | Value |

|--------|-------|

| RFC Number | RFC-009 |

| Change Type | Standard Change |

| Status | Completed |

| Priority | Medium |

| Requested By | Customer Support Department |

| Change Owner | Microsoft 365 Administration Team |

| Assigned Technician | Kenyotta Eave |

| Date Submitted | September 5, 2026 |

| Scheduled Implementation | September 6, 2026 |

| Completion Date | September 6, 2026 |



\---



\# Change Summary



Create a new Microsoft 365 Shared Mailbox for the Customer Support Department to centralize customer email communications.



The mailbox will provide multiple support representatives with access to incoming customer requests while maintaining centralized ownership and auditing.



\---



\# Business Justification



The Customer Support Department currently manages customer inquiries through individual employee mailboxes, making collaboration difficult and creating a risk of delayed responses.



Deploying a shared mailbox will improve:



\- Team collaboration

\- Customer response times

\- Workload distribution

\- Mailbox continuity during employee absences

\- Auditability of customer communications



\---



\# Shared Mailbox Information



| Field | Value |

|--------|-------|

| Display Name | Customer Support |

| Email Address | support@apexmanufacturing.com |

| Department | Customer Support |

| Owner | Lisa Martinez |

| Initial Members | 8 |



\---



\# Systems Affected



\- Microsoft 365 Admin Center

\- Exchange Online

\- Microsoft Outlook

\- Outlook on the Web

\- Microsoft Entra ID

\- CMDB



\---



\# Scope



This change includes:



\- Create Shared Mailbox

\- Configure Exchange Online

\- Assign Full Access permissions

\- Assign Send As permissions

\- Configure Outlook Auto Mapping

\- Validate Outlook Web Access

\- Update documentation

\- Update CMDB



\---



\# Risk Assessment



\## Overall Risk



\*\*Low\*\*



\### Risks



\- Incorrect mailbox permissions

\- Incorrect email address assignment

\- Mailbox synchronization delay

\- Outlook Auto Mapping delay



\### Mitigation



\- Verify mailbox naming conventions

\- Review permission assignments

\- Test mailbox using pilot account

\- Validate Outlook synchronization before closing change



\---



\# Impact Assessment



Business Impact



Low



User Impact



Customer Support staff may need to restart Outlook to receive the new mailbox.



Expected Downtime



None



Customer Impact



None



\---



\# Pre-Implementation Checklist



\- \[x] Department manager approval received

\- \[x] Shared mailbox name verified

\- \[x] Email address confirmed

\- \[x] Microsoft 365 service health verified

\- \[x] Members identified

\- \[x] Documentation prepared



\---



\# Implementation Plan



1\. Verify approved request.

2\. Create Shared Mailbox in Microsoft 365.

3\. Assign display name.

4\. Configure email address.

5\. Assign mailbox owner.

6\. Assign Full Access permissions.

7\. Assign Send As permissions.

8\. Verify Outlook Auto Mapping.

9\. Test Outlook Web Access.

10\. Validate email delivery.

11\. Update CMDB.

12\. Close Help Desk ticket.



\---



\# Validation Plan



The following validation activities were completed successfully.



\- Shared mailbox created

\- Email address verified

\- Outlook desktop access verified

\- Outlook Web Access verified

\- Send As permissions confirmed

\- Incoming email received successfully

\- Outgoing email delivered successfully



Result:



\*\*Successful\*\*



\---



\# Rollback Plan



If implementation failed:



1\. Remove mailbox permissions.

2\. Delete Shared Mailbox.

3\. Restore previous email workflow.

4\. Notify department manager.

5\. Escalate to Microsoft 365 Administration Team.



\---



\# Communication Plan



\## Before Implementation



\- Notify Customer Support Manager

\- Notify Help Desk

\- Notify mailbox users



\## After Implementation



\- Confirm mailbox availability

\- Provide mailbox usage instructions

\- Update Help Desk documentation

\- Close change request



\---



\# Approval History



| Approver | Department | Status |

|----------|------------|--------|

| Lisa Martinez | Customer Support | Approved |

| David Brooks | IT Operations | Approved |

| Rachel Adams | Microsoft 365 Administration | Approved |



\---



\# Implementation Results



The shared mailbox deployment completed successfully.



\- Mailbox created

\- Permissions assigned

\- Outlook synchronization verified

\- Email flow validated

\- Documentation updated

\- No issues encountered



\---



\# Post-Implementation Review



\## Objectives Met



\- Shared mailbox deployed successfully

\- Customer Support collaboration improved

\- Microsoft 365 configuration documented

\- No service interruption

\- No rollback required



\### Lessons Learned



Testing mailbox access using a pilot account before granting access to all team members helped identify and resolve a minor permission inheritance issue prior to production rollout.



\---



\# Related Documentation



\- FORM-007-Shared-Mailbox-Request.md

\- Infrastructure/Microsoft-365/

\- Employee-Directory.md

\- Naming-Conventions.md

\- CMDB.md

\- Change-Management-Policy.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial completed Request for Change documenting deployment of a Microsoft 365 Shared Mailbox. |

