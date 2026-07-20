\# RFC-002 – Windows Monthly Patching



\---



\# Apex Manufacturing, Inc.



\## Request for Change (RFC)



| Field | Value |

|--------|-------|

| RFC Number | RFC-002 |

| Change Type | Normal Change |

| Status | Completed |

| Priority | High |

| Requested By | IT Operations |

| Change Owner | Infrastructure Team |

| Assigned Technician | Kenyotta Eave |

| Date Submitted | July 21, 2026 |

| Scheduled Maintenance Window | July 24, 2026 (10:00 PM – 12:00 AM CST) |

| Completion Date | July 24, 2026 |



\---



\# Change Summary



Deploy Microsoft's monthly cumulative security updates to all supported Windows Server and Windows 11 endpoints within the Apex Manufacturing environment.



The purpose of this maintenance window is to remediate newly disclosed security vulnerabilities, maintain compliance with organizational security policies, and improve system stability.



\---



\# Business Justification



Monthly operating system patching is required to:



\- Maintain cybersecurity posture

\- Address critical and high-severity vulnerabilities

\- Meet organizational compliance requirements

\- Improve system reliability

\- Reduce exposure to ransomware and known exploits



\---



\# Systems Affected



\### Servers



\- DC01 (Domain Controller)

\- FILE01 (File Server)

\- PRINT01 (Print Server)



\### Workstations



\- Windows 11 Enterprise endpoints

\- Department laptops

\- Executive workstations



\---



\# Scope



This change includes:



\- Windows Security Updates

\- Cumulative Updates

\- .NET Framework Updates

\- Microsoft Defender Security Intelligence Updates

\- Microsoft Defender Platform Updates



\---



\# Risk Assessment



\### Overall Risk



\*\*Medium\*\*



\### Risks



\- Unexpected reboot failures

\- Driver compatibility issues

\- Application compatibility problems

\- Temporary service interruption



\### Mitigation



\- Perform full VM snapshots before maintenance

\- Verify recent backups

\- Test updates in lab environment

\- Schedule after business hours

\- Notify all departments in advance



\---



\# Impact Assessment



Business Impact



Low



Expected Downtime



15–30 minutes per server



User Impact



Users may be unable to access internal resources while servers reboot.



Customer Impact



None expected.



\---



\# Pre-Implementation Checklist



\- \[x] Recent backups verified

\- \[x] VM snapshots created

\- \[x] Maintenance window approved

\- \[x] Department managers notified

\- \[x] Patch testing completed in lab

\- \[x] Change Advisory Board approval received



\---



\# Implementation Plan



1\. Verify backup completion.

2\. Create Hyper-V/VM snapshots.

3\. Download approved Windows Updates.

4\. Install updates on non-production systems.

5\. Validate successful installation.

6\. Install updates on production servers.

7\. Restart affected servers.

8\. Verify Active Directory services.

9\. Verify DNS functionality.

10\. Verify DHCP services.

11\. Verify File Server availability.

12\. Verify Print Server availability.

13\. Verify workstation connectivity.

14\. Document installation results.

15\. Close change record.



\---



\# Validation Plan



The following validation tests were completed successfully.



\- Domain authentication verified

\- DNS resolution successful

\- Group Policy processing confirmed

\- File shares accessible

\- Network printers operational

\- Windows Update history confirmed

\- Microsoft Defender operational

\- Event Viewer reviewed

\- No critical system errors detected



Result:



\*\*Successful\*\*



\---



\# Rollback Plan



If the implementation failed:



1\. Restore affected virtual machine snapshot.

2\. Uninstall failed Windows updates.

3\. Restore latest verified backup if required.

4\. Notify Change Manager.

5\. Escalate to Infrastructure Team.

6\. Schedule emergency maintenance if necessary.



\---



\# Communication Plan



\### Before Maintenance



\- Notify all employees 72 hours in advance.

\- Send maintenance reminder 24 hours before implementation.

\- Notify Help Desk staff.



\### After Maintenance



\- Send maintenance completion notification.

\- Confirm all production services operational.

\- Update change record.



\---



\# Approval History



| Approver | Department | Status |

|----------|------------|--------|

| David Brooks | IT Operations Manager | Approved |

| Rachel Adams | Infrastructure Manager | Approved |

| Information Security Team | Security | Approved |



\---



\# Implementation Results



Implementation completed successfully.



\- All servers patched successfully.

\- All workstations received approved updates.

\- No failed installations observed.

\- No service interruptions outside the approved maintenance window.



\---



\# Post-Implementation Review



\### Objectives Met



\- Security vulnerabilities remediated

\- Systems remained stable

\- Compliance maintained

\- Downtime remained within approved limits

\- No rollback required



\### Lessons Learned



Pre-deployment testing in the lab environment identified a printer driver compatibility issue before production deployment, allowing it to be resolved without impacting end users.



\---



\# Related Documentation



\- Change-Management-Policy.md

\- Security-Policies.md

\- Security-Baselines.md

\- CMDB.md

\- Server-Inventory.md

\- Infrastructure/Servers/

\- SOP-010 Windows Server Patching \*(planned)\*



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | July 2026 | Kenyotta Eave | Initial completed Request for Change documenting monthly Windows patch deployment. |

