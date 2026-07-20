\# RFC-008 – Firewall Rule Change



\---



\# Apex Manufacturing, Inc.



\## Request for Change (RFC)



| Field | Value |

|--------|-------|

| RFC Number | RFC-008 |

| Change Type | Normal Change |

| Status | Completed |

| Priority | High |

| Requested By | Information Security |

| Change Owner | Network Security Team |

| Assigned Technician | Kenyotta Eave |

| Date Submitted | August 29, 2026 |

| Scheduled Maintenance Window | August 31, 2026 (9:00 PM – 10:00 PM CST) |

| Completion Date | August 31, 2026 |



\---



\# Change Summary



Implement a new inbound firewall rule allowing secure HTTPS (TCP 443) communication from the corporate VPN network to the internal Help Desk application server while removing an obsolete legacy rule permitting unnecessary HTTP (TCP 80) access.



The change supports secure remote access while reducing the organization's attack surface.



\---



\# Business Justification



Apex Manufacturing recently migrated internal web applications to HTTPS.



The legacy HTTP firewall rule is no longer required and presents an unnecessary security risk.



Implementing this change ensures:



\- Secure encrypted communications

\- Compliance with Security Baselines

\- Reduced attack surface

\- Alignment with organizational security policies



\---



\# Systems Affected



\- Corporate Firewall

\- VPN Gateway

\- Help Desk Application Server

\- Internal Network

\- Network Monitoring Platform



\---



\# Scope



This change includes:



\- Create new HTTPS firewall rule

\- Remove legacy HTTP rule

\- Verify VPN network access

\- Validate application connectivity

\- Review firewall logging

\- Update firewall documentation

\- Update CMDB



\---



\# Firewall Rule Details



\### New Rule



| Setting | Value |

|---------|-------|

| Action | Allow |

| Protocol | TCP |

| Port | 443 |

| Source | Corporate VPN Network |

| Destination | Help Desk Application Server |

| Logging | Enabled |



\---



\### Removed Rule



| Setting | Value |

|---------|-------|

| Action | Allow |

| Protocol | TCP |

| Port | 80 |

| Source | VPN Network |

| Destination | Help Desk Application Server |



\---



\# Risk Assessment



\## Overall Risk



\*\*Medium\*\*



\### Risks



\- Incorrect firewall configuration

\- Accidental service interruption

\- VPN connectivity failure

\- Application access issues



\### Mitigation



\- Export firewall configuration before changes

\- Validate rules in staging environment

\- Schedule maintenance after business hours

\- Monitor firewall logs during implementation

\- Prepare rollback procedure



\---



\# Impact Assessment



Business Impact



Medium



User Impact



Remote users may briefly lose access to the Help Desk application while firewall policies are updated.



Expected Downtime



Less than 10 minutes



Customer Impact



None



\---



\# Pre-Implementation Checklist



\- \[x] Firewall configuration backed up

\- \[x] Existing rules documented

\- \[x] Maintenance approved

\- \[x] Help Desk notified

\- \[x] Information Security approval received

\- \[x] Monitoring tools operational



\---



\# Implementation Plan



1\. Export current firewall configuration.

2\. Verify maintenance window has begun.

3\. Create new HTTPS allow rule.

4\. Enable logging for the new rule.

5\. Remove obsolete HTTP rule.

6\. Apply firewall policy.

7\. Verify rule synchronization.

8\. Test VPN connectivity.

9\. Verify Help Desk application access.

10\. Review firewall logs.

11\. Update firewall documentation.

12\. Update CMDB.

13\. Close change request.



\---



\# Validation Plan



The following validation activities were completed successfully.



\- HTTPS connectivity verified

\- VPN users authenticated successfully

\- Help Desk application accessible

\- Firewall logging operational

\- No unexpected denied connections

\- Legacy HTTP access blocked

\- Network monitoring reported normal traffic



Result:



\*\*Successful\*\*



\---



\# Rollback Plan



If implementation failed:



1\. Restore exported firewall configuration.

2\. Re-enable previous HTTP rule.

3\. Remove newly created HTTPS rule if required.

4\. Apply previous firewall policy.

5\. Verify application connectivity.

6\. Notify Information Security and Infrastructure teams.



\---



\# Communication Plan



\## Before Maintenance



\- Notify Help Desk

\- Notify Infrastructure Team

\- Notify Information Security

\- Notify remote users



\## During Maintenance



\- Monitor firewall logs

\- Provide implementation status updates



\## After Maintenance



\- Confirm secure application access

\- Notify stakeholders

\- Archive implementation documentation



\---



\# Approval History



| Approver | Department | Status |

|----------|------------|--------|

| Information Security Manager | Security | Approved |

| Rachel Adams | Infrastructure | Approved |

| David Brooks | IT Operations | Approved |



\---



\# Implementation Results



Implementation completed successfully.



\- HTTPS rule deployed

\- Legacy HTTP rule removed

\- VPN connectivity validated

\- Firewall logging confirmed

\- No service interruptions observed

\- No rollback required



\---



\# Post-Implementation Review



\## Objectives Met



\- Secure communications enforced

\- Legacy firewall rule removed

\- Security posture improved

\- Documentation updated

\- Change completed within approved maintenance window



\### Lessons Learned



Reviewing firewall logs immediately after implementation confirmed legitimate traffic was permitted while unauthorized HTTP requests were successfully blocked, providing immediate validation of the new policy.



\---



\# Related Documentation



\- RFC-005-VPN-Configuration-Change.md

\- Infrastructure/Networking/

\- Security/Security-Baselines/

\- Security/Security-Policies.md

\- CMDB.md

\- Change-Management-Policy.md

\- SOP-011 Firewall Rule Management \*(planned)\*



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | August 2026 | Kenyotta Eave | Initial completed Request for Change documenting enterprise firewall rule modification. |

