\# RFC-003 – Deploy New Department Printer



\---



\# Apex Manufacturing, Inc.



\## Request for Change (RFC)



| Field | Value |

|--------|-------|

| RFC Number | RFC-003 |

| Change Type | Standard Change |

| Status | Completed |

| Priority | Medium |

| Requested By | Finance Department |

| Change Owner | Infrastructure Team |

| Assigned Technician | Kenyotta Eave |

| Date Submitted | July 26, 2026 |

| Scheduled Implementation | July 28, 2026 |

| Completion Date | July 28, 2026 |



\---



\# Change Summary



Deploy a new network multifunction printer for the Finance Department to replace an aging device that had reached end-of-life and experienced repeated hardware failures.



The deployment includes printer installation, network configuration, Active Directory printer deployment, driver installation, and user validation.



\---



\# Business Justification



The existing Finance Department printer experienced frequent paper jams, toner sensor failures, and intermittent network connectivity issues.



Replacing the device improves employee productivity, reduces Help Desk tickets, and provides improved scanning and secure printing capabilities.



\---



\# Systems Affected



\- PRINT01 Print Server

\- Active Directory

\- Finance Department Windows 11 Workstations

\- Corporate LAN

\- Asset Inventory (CMDB)



\---



\# Scope



This change includes:



\- Install new multifunction printer

\- Assign static IP address

\- Configure print server

\- Publish printer in Active Directory

\- Install printer drivers

\- Deploy printer to Finance users

\- Configure secure printing

\- Update CMDB



\---



\# Risk Assessment



\## Overall Risk



\*\*Low\*\*



\### Risks



\- Incorrect printer driver installation

\- Network connectivity issues

\- Incorrect security permissions

\- Print queue configuration errors



\### Mitigation



\- Verify firmware before deployment

\- Test printer in IT lab

\- Backup existing print queue configuration

\- Validate network connectivity before production deployment



\---



\# Impact Assessment



Business Impact



Low



User Impact



Finance users may briefly lose printing services during printer replacement.



Expected Downtime



Approximately 30 minutes



Customer Impact



None



\---



\# Pre-Implementation Checklist



\- \[x] New printer received and inspected

\- \[x] Firmware updated

\- \[x] Static IP reserved

\- \[x] Print drivers downloaded

\- \[x] Maintenance window approved

\- \[x] Department manager notified



\---



\# Implementation Plan



1\. Remove old printer from service.

2\. Install new multifunction printer.

3\. Connect printer to corporate network.

4\. Configure static IP address.

5\. Update printer firmware.

6\. Install printer on PRINT01.

7\. Share printer from print server.

8\. Publish printer in Active Directory.

9\. Configure security permissions.

10\. Install printer on Finance workstations.

11\. Print test pages.

12\. Verify scanning functionality.

13\. Verify secure printing.

14\. Update asset inventory.

15\. Close Help Desk ticket.



\---



\# Validation Plan



The following validation steps were completed successfully.



\- Printer reachable on network

\- Print queue operational

\- Test page printed successfully

\- Color printing verified

\- Duplex printing verified

\- Scanner functionality verified

\- Secure print release verified

\- Finance users successfully connected



Result:



\*\*Successful\*\*



\---



\# Rollback Plan



If deployment failed:



1\. Disconnect new printer.

2\. Restore previous printer configuration.

3\. Restore previous print queue.

4\. Reconnect legacy printer.

5\. Notify Finance Department.

6\. Escalate hardware issue to vendor.



\---



\# Communication Plan



\## Before Implementation



\- Notify Finance Department

\- Notify Help Desk

\- Schedule deployment after business hours



\## After Implementation



\- Notify Finance Manager

\- Confirm successful printing

\- Update change documentation

\- Close change request



\---



\# Approval History



| Approver | Department | Status |

|----------|------------|--------|

| Michael Reynolds | Finance | Approved |

| David Brooks | IT Operations | Approved |

| Rachel Adams | Infrastructure | Approved |



\---



\# Implementation Results



Deployment completed successfully.



\- Printer installed successfully

\- Network connectivity verified

\- Active Directory publication successful

\- Print queue operational

\- No unexpected issues encountered



\---



\# Post-Implementation Review



\## Objectives Met



\- New printer deployed successfully

\- Finance users restored to full printing capability

\- Asset inventory updated

\- No unplanned downtime

\- No rollback required



\### Lessons Learned



Preloading printer drivers on the print server before workstation deployment reduced installation time and minimized user disruption.



\---



\# Related Documentation



\- FORM-009-Printer-Access-Request.md

\- Asset-Inventory.md

\- CMDB.md

\- Server-Inventory.md

\- Infrastructure/Servers/

\- Infrastructure/Networking/

\- Change-Management-Policy.md

\- SOP-008 Printer Management \*(planned)\*



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | July 2026 | Kenyotta Eave | Initial completed Request for Change documenting deployment of a new Finance Department network printer. |

