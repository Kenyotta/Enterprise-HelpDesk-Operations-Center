\# RFC-007 – Server Maintenance Window



\---



\# Apex Manufacturing, Inc.



\## Request for Change (RFC)



| Field | Value |

|--------|-------|

| RFC Number | RFC-007 |

| Change Type | Normal Change |

| Status | Completed |

| Priority | High |

| Requested By | Infrastructure Team |

| Change Owner | Systems Administration Team |

| Assigned Technician | Kenyotta Eave |

| Date Submitted | August 22, 2026 |

| Scheduled Maintenance Window | August 24, 2026 (10:00 PM – 2:00 AM CST) |

| Completion Date | August 24, 2026 |



\---



\# Change Summary



Perform scheduled maintenance on critical infrastructure servers to ensure continued reliability, security, and performance.



Maintenance includes operating system updates, storage verification, Active Directory health checks, DNS validation, log review, backup verification, and service testing.



\---



\# Business Justification



Routine server maintenance is required to maintain system availability, reduce the likelihood of unexpected outages, improve performance, and ensure compliance with organizational security and operational standards.



\---



\# Systems Affected



\## Domain Services



\- DC01 (Domain Controller)



\## File Services



\- FILE01



\## Print Services



\- PRINT01



\## Supporting Services



\- Active Directory Domain Services

\- DNS

\- Group Policy

\- Windows Event Logging

\- Windows Backup

\- Microsoft Defender



\---



\# Scope



This maintenance includes:



\- Install approved Windows updates

\- Review system health

\- Verify Active Directory replication

\- Verify DNS functionality

\- Review storage utilization

\- Verify backup completion

\- Review system event logs

\- Restart required services

\- Validate production services

\- Update maintenance documentation



\---



\# Risk Assessment



\## Overall Risk



\*\*Medium\*\*



\### Risks



\- Unexpected reboot failure

\- Service startup issues

\- Delayed Active Directory replication

\- Hardware failure during reboot



\### Mitigation



\- Verify backups before maintenance

\- Create virtual machine snapshots

\- Perform maintenance after business hours

\- Validate each service before proceeding to the next system

\- Maintain rollback procedures



\---



\# Impact Assessment



Business Impact



Medium



User Impact



Employees may temporarily lose access to authentication, file shares, printers, and internal resources while maintenance is in progress.



Expected Downtime



Approximately 45 minutes



Customer Impact



None expected.



\---



\# Pre-Implementation Checklist



\- \[x] Recent backups verified

\- \[x] Virtual machine snapshots created

\- \[x] Maintenance window approved

\- \[x] Department managers notified

\- \[x] Help Desk notified

\- \[x] Monitoring dashboards operational



\---



\# Implementation Plan



1\. Verify backup completion.

2\. Create virtual machine snapshots.

3\. Notify stakeholders that maintenance is beginning.

4\. Install approved Windows updates.

5\. Restart DC01.

6\. Verify Active Directory services.

7\. Verify DNS resolution.

8\. Restart FILE01.

9\. Verify shared folders.

10\. Restart PRINT01.

11\. Verify printer queues.

12\. Review Windows Event Viewer.

13\. Confirm Microsoft Defender status.

14\. Verify server performance.

15\. Update CMDB.

16\. Close maintenance window.



\---



\# Validation Plan



The following validation activities were completed successfully.



\- Active Directory operational

\- DNS resolution verified

\- Group Policy processing successful

\- File shares accessible

\- Network printers available

\- Windows Event Logs reviewed

\- Backup status verified

\- Microsoft Defender operational

\- CPU and memory utilization within normal limits



Result:



\*\*Successful\*\*



\---



\# Rollback Plan



If maintenance failed:



1\. Restore affected virtual machine snapshot.

2\. Recover from verified backup if required.

3\. Restart failed services.

4\. Notify Infrastructure Manager.

5\. Escalate to Microsoft Support if necessary.

6\. Schedule emergency maintenance window.



\---



\# Communication Plan



\## Before Maintenance



\- Notify all employees

\- Notify department managers

\- Notify Help Desk

\- Publish maintenance advisory



\## During Maintenance



\- Provide hourly status updates

\- Report any unexpected issues



\## After Maintenance



\- Confirm all services operational

\- Notify stakeholders of completion

\- Update change documentation



\---



\# Approval History



| Approver | Department | Status |

|----------|------------|--------|

| Rachel Adams | Infrastructure | Approved |

| David Brooks | IT Operations | Approved |

| Information Security Team | Security | Approved |



\---



\# Implementation Results



Maintenance completed successfully.



\- All servers restarted successfully.

\- Windows updates installed.

\- Active Directory healthy.

\- DNS functioning normally.

\- File services restored.

\- Print services verified.

\- No unexpected outages occurred.



\---



\# Post-Implementation Review



\## Objectives Met



\- Infrastructure successfully maintained

\- Security updates applied

\- System health verified

\- Backup validation completed

\- Documentation updated



\### Lessons Learned



Completing health checks immediately after each server reboot allowed issues to be identified quickly before proceeding to the next maintenance task, reducing operational risk.



\---



\# Related Documentation



\- RFC-002-Windows-Monthly-Patching.md

\- Infrastructure/Servers/

\- Infrastructure/Active-Directory/

\- Server-Inventory.md

\- CMDB.md

\- Security-Baselines.md

\- Change-Management-Policy.md

\- SOP-010 Windows Server Maintenance \*(planned)\*



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | August 2026 | Kenyotta Eave | Initial completed Request for Change documenting scheduled enterprise server maintenance. |

