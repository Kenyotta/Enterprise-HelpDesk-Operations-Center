\# RFC-005 – VPN Configuration Change



\---



\# Apex Manufacturing, Inc.



\## Request for Change (RFC)



| Field | Value |

|--------|-------|

| RFC Number | RFC-005 |

| Change Type | Normal Change |

| Status | Completed |

| Priority | High |

| Requested By | Information Security |

| Change Owner | Network Infrastructure Team |

| Assigned Technician | Kenyotta Eave |

| Date Submitted | August 8, 2026 |

| Scheduled Maintenance | August 10, 2026 (8:00 PM – 9:00 PM CST) |

| Completion Date | August 10, 2026 |



\---



\# Change Summary



Update the corporate VPN configuration to enforce Multi-Factor Authentication (MFA) for all remote users and migrate legacy authentication policies to Microsoft Entra ID Conditional Access.



The change improves remote access security and aligns VPN authentication with Apex Manufacturing's Security Baselines.



\---



\# Business Justification



Recent security assessments identified that several legacy VPN authentication policies did not enforce Multi-Factor Authentication.



Implementing MFA for all VPN users significantly reduces the risk of unauthorized access resulting from compromised credentials.



\---



\# Systems Affected



\- VPN Gateway

\- Microsoft Entra ID

\- Active Directory (DC01)

\- Microsoft Authenticator

\- Conditional Access Policies

\- Remote User Workstations



\---



\# Scope



This change includes:



\- Enable MFA requirement

\- Update VPN authentication policy

\- Integrate Microsoft Entra ID

\- Remove legacy authentication policy

\- Verify remote connectivity

\- Update VPN documentation

\- Update CMDB



\---



\# Risk Assessment



\## Overall Risk



\*\*Medium\*\*



\### Risks



\- Users unable to authenticate

\- Incorrect Conditional Access configuration

\- VPN client compatibility issues

\- Increased Help Desk call volume



\### Mitigation



\- Test policy in pilot group

\- Maintain previous authentication policy until validation completes

\- Notify users in advance

\- Schedule implementation after business hours

\- Prepare rollback procedure



\---



\# Impact Assessment



Business Impact



Medium



User Impact



Remote users will be prompted to register or verify Multi-Factor Authentication during their next VPN login.



Expected Downtime



Less than 15 minutes



Customer Impact



None



\---



\# Pre-Implementation Checklist



\- \[x] VPN configuration backed up

\- \[x] Conditional Access policy tested

\- \[x] Pilot user testing completed

\- \[x] Microsoft Authenticator verified

\- \[x] Change approved

\- \[x] Users notified



\---



\# Implementation Plan



1\. Export existing VPN configuration.

2\. Verify Microsoft Entra ID connectivity.

3\. Create new Conditional Access policy.

4\. Enable MFA enforcement.

5\. Disable legacy authentication policy.

6\. Synchronize policy changes.

7\. Test VPN connection using pilot account.

8\. Validate remote desktop connectivity.

9\. Monitor authentication logs.

10\. Update documentation.

11\. Close change request.



\---



\# Validation Plan



The following validation steps were completed successfully.



\- VPN authentication successful

\- MFA challenge received

\- Microsoft Authenticator approval successful

\- Active Directory authentication verified

\- Internal network resources accessible

\- File shares accessible

\- Remote Desktop connectivity verified

\- Security logs reviewed



Result:



\*\*Successful\*\*



\---



\# Rollback Plan



If implementation failed:



1\. Disable new Conditional Access policy.

2\. Restore previous VPN configuration.

3\. Re-enable legacy authentication.

4\. Verify VPN connectivity.

5\. Notify affected users.

6\. Escalate to Network Infrastructure Team.



\---



\# Communication Plan



\## Before Implementation



\- Notify all remote employees

\- Notify Help Desk

\- Notify Department Managers



\## After Implementation



\- Confirm VPN availability

\- Publish user guidance for MFA enrollment

\- Monitor Help Desk tickets

\- Close change record



\---



\# Approval History



| Approver | Department | Status |

|----------|------------|--------|

| Rachel Adams | Network Infrastructure | Approved |

| David Brooks | IT Operations | Approved |

| Information Security Team | Security | Approved |



\---



\# Implementation Results



The VPN authentication update completed successfully.



\- MFA enforcement enabled

\- Legacy authentication retired

\- Microsoft Entra ID integration verified

\- Remote access validated

\- No critical issues identified



\---



\# Post-Implementation Review



\## Objectives Met



\- Multi-Factor Authentication enforced

\- Remote access security strengthened

\- Legacy authentication removed

\- Documentation updated

\- No rollback required



\### Lessons Learned



Deploying the updated VPN policy to a pilot group before enterprise-wide implementation reduced risk and allowed minor configuration issues to be resolved before affecting production users.



\---



\# Related Documentation



\- FORM-006-VPN-Access-Request.md

\- FORM-010-MFA-Reset-Request.md

\- Infrastructure/Networking/

\- Infrastructure/Microsoft-365/

\- Security-Baselines.md

\- Security-Policies.md

\- CMDB.md

\- Change-Management-Policy.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | August 2026 | Kenyotta Eave | Initial completed Request for Change documenting enterprise VPN authentication modernization. |

