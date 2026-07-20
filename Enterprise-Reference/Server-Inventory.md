\# Server Inventory



\---



\# Apex Manufacturing, Inc.



\## Server Inventory



\### Purpose



This document serves as the official server inventory for Apex Manufacturing, Inc.



It provides a centralized record of all production and infrastructure servers maintained by the Information Technology department. The inventory supports system administration, asset management, disaster recovery planning, change management, and cybersecurity operations.



All server-related documentation throughout this repository should reference this inventory to ensure consistency.



\---



\# Server Naming Standard



Servers follow the naming convention below.



```text

SRV-<FUNCTION>-##



Examples



SRV-DC-01

SRV-FILE-01

SRV-PRINT-01

SRV-APP-01

SRV-BACKUP-01

```



\---



\# Server Status



The following status values are used.



\- Production

\- Testing

\- Maintenance

\- Offline

\- Retired



\---



\# Infrastructure Servers



\## Domain Controller



| Property | Value |

|-----------|-------|

| Server Name | SRV-DC-01 |

| Hostname | DC01 |

| Role | Primary Domain Controller |

| Operating System | Windows Server 2022 Standard |

| Environment | Production |

| Location | Dallas Headquarters |

| Department | Information Technology |

| Status | Production |

| Backup Schedule | Nightly |

| Owner | Systems Administration Team |



\---



\## File Server



| Property | Value |

|-----------|-------|

| Server Name | SRV-FILE-01 |

| Hostname | FILE01 |

| Role | Enterprise File Server |

| Operating System | Windows Server 2022 Standard |

| Environment | Production |

| Location | Dallas Headquarters |

| Status | Production |

| Backup Schedule | Nightly |

| Owner | Systems Administration Team |



\---



\## Print Server



| Property | Value |

|-----------|-------|

| Server Name | SRV-PRINT-01 |

| Hostname | PRINT01 |

| Role | Network Print Services |

| Operating System | Windows Server 2022 Standard |

| Environment | Production |

| Location | Dallas Headquarters |

| Status | Production |

| Backup Schedule | Nightly |

| Owner | Systems Administration Team |



\---



\## Application Server



| Property | Value |

|-----------|-------|

| Server Name | SRV-APP-01 |

| Hostname | APP01 |

| Role | Internal Business Applications |

| Operating System | Windows Server 2022 Standard |

| Environment | Production |

| Location | Dallas Headquarters |

| Status | Production |

| Backup Schedule | Nightly |

| Owner | Infrastructure Team |



\---



\## Backup Server



| Property | Value |

|-----------|-------|

| Server Name | SRV-BACKUP-01 |

| Hostname | BACKUP01 |

| Role | Backup \& Recovery Services |

| Operating System | Windows Server 2022 Standard |

| Environment | Production |

| Location | Dallas Headquarters |

| Status | Production |

| Backup Schedule | Continuous |

| Owner | Infrastructure Team |



\---



\## Management Server



| Property | Value |

|-----------|-------|

| Server Name | SRV-MGMT-01 |

| Hostname | MGMT01 |

| Role | Systems Management |

| Operating System | Windows Server 2022 Standard |

| Environment | Production |

| Status | Production |

| Owner | Infrastructure Team |



\---



\## WSUS Server



| Property | Value |

|-----------|-------|

| Server Name | SRV-WSUS-01 |

| Hostname | WSUS01 |

| Role | Windows Update Services |

| Operating System | Windows Server 2022 Standard |

| Environment | Production |

| Status | Production |

| Owner | Systems Administration Team |



\---



\## Monitoring Server



| Property | Value |

|-----------|-------|

| Server Name | SRV-MON-01 |

| Hostname | MONITOR01 |

| Role | Infrastructure Monitoring |

| Operating System | Windows Server 2022 Standard |

| Environment | Production |

| Status | Production |

| Owner | Infrastructure Team |



\---



\# Planned Future Servers



The following servers will be introduced as additional projects are completed.



| Hostname | Purpose |

|-----------|----------|

| M365SYNC01 | Microsoft 365 Hybrid Sync |

| INTUNE01 | Microsoft Intune Management |

| AZCONNECT01 | Azure AD Connect |

| SPLUNK01 | SIEM Platform |

| WAZUH01 | Security Monitoring |

| PKI01 | Certificate Services |

| MDT01 | Windows Deployment Services |

| SQL01 | SQL Database Server |



\---



\# Server Roles



| Role | Primary Responsibility |

|------|------------------------|

| Domain Controller | Authentication and Active Directory |

| File Server | Department file shares |

| Print Server | Centralized printing |

| Application Server | Internal applications |

| Backup Server | Backup and disaster recovery |

| Management Server | Administrative tools |

| WSUS Server | Windows Updates |

| Monitoring Server | Infrastructure monitoring |



\---



\# Maintenance Window



Routine server maintenance is performed during the following maintenance window.



\*\*Day\*\*



Saturday



\*\*Time\*\*



10:00 PM – 2:00 AM Central Time



Maintenance activities include:



\- Windows Updates

\- Security patches

\- Firmware updates

\- Backup verification

\- Log review

\- Service validation



\---



\# Backup Policy



Infrastructure servers are protected according to the following schedule.



| Backup Type | Frequency |

|-------------|-----------|

| System State | Daily |

| Full Backup | Weekly |

| Incremental Backup | Nightly |

| Configuration Backup | Before Changes |



\---



\# Disaster Recovery Priority



| Priority | Server |

|-----------|--------|

| Critical | DC01 |

| Critical | FILE01 |

| High | BACKUP01 |

| High | APP01 |

| Medium | PRINT01 |

| Medium | WSUS01 |

| Medium | MGMT01 |



\---



\# Monitoring



The following items should be monitored continuously.



\- CPU utilization

\- Memory utilization

\- Disk usage

\- Windows Event Logs

\- Active Directory replication

\- Backup status

\- Network connectivity

\- Service availability

\- Failed logon attempts

\- Storage capacity



\---



\# Change Management



All server modifications require:



\- Approved Change Request

\- Maintenance Window

\- Rollback Plan

\- Backup Verification

\- Change Documentation

\- Post-Implementation Validation



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | July 2026 | Kenyotta Eave | Initial server inventory created. |

