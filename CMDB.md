\# Configuration Management Database (CMDB)



\---



\# Apex Manufacturing, Inc.



\## Purpose



The Configuration Management Database (CMDB) serves as the central inventory of Configuration Items (CIs) managed by the Information Technology department.



The CMDB provides a consolidated view of critical IT assets, their relationships, ownership, and business impact. It supports Incident Management, Problem Management, Change Management, Asset Management, Disaster Recovery, and Security Operations.



This document represents a simplified CMDB suitable for documentation and portfolio purposes.



\---



\# What is a Configuration Item (CI)?



A Configuration Item (CI) is any component that must be managed to deliver an IT service.



Examples include:



\- Servers

\- Workstations

\- Applications

\- Network Devices

\- Printers

\- User Accounts

\- File Shares

\- Cloud Services

\- Virtual Machines

\- Security Appliances



\---



\# Configuration Item Categories



| Category | Description |

|-----------|-------------|

| Server | Physical or virtual servers |

| Workstation | Employee desktops and laptops |

| Network Device | Switches, routers, firewalls, wireless access points |

| Application | Business software and internal applications |

| Printer | Network-connected printers |

| Cloud Service | Microsoft 365, Azure, cloud-hosted resources |

| Database | SQL and application databases |

| Security Tool | Security monitoring and endpoint protection platforms |



\---



\# Core Infrastructure Configuration Items



| CI Name | Category | Owner | Status | Business Criticality |

|----------|----------|-------|--------|----------------------|

| DC01 | Server | Systems Administration | Production | Critical |

| FILE01 | Server | Systems Administration | Production | Critical |

| PRINT01 | Server | Systems Administration | Production | High |

| APP01 | Server | Infrastructure Team | Production | High |

| BACKUP01 | Server | Infrastructure Team | Production | Critical |

| MGMT01 | Server | Infrastructure Team | Production | Medium |

| WSUS01 | Server | Systems Administration | Production | Medium |

| MONITOR01 | Server | Infrastructure Team | Production | High |



\---



\# Core Business Applications



| Application | Owner | Department | Criticality |

|-------------|-------|------------|--------------|

| Microsoft 365 | Microsoft 365 Administrator | IT | Critical |

| Outlook | Microsoft 365 Administrator | Company-wide | Critical |

| Microsoft Teams | Microsoft 365 Administrator | Company-wide | High |

| SharePoint Online | Microsoft 365 Administrator | Company-wide | High |

| OneDrive | Microsoft 365 Administrator | Company-wide | High |

| osTicket | Help Desk Supervisor | IT | High |



\---



\# Network Infrastructure



| Device | Category | Owner | Status |

|---------|----------|-------|--------|

| Core Firewall | Security Appliance | Network Administration | Production |

| Core Switch Stack | Network Switch | Network Administration | Production |

| VPN Gateway | Security Appliance | Network Administration | Production |

| Wireless Controller | Network Device | Network Administration | Production |



\---



\# Business Service Dependencies



| Business Service | Depends On |

|------------------|------------|

| Employee Login | DC01, DNS, Active Directory |

| File Access | FILE01, Active Directory |

| Printing | PRINT01, Active Directory |

| Email | Microsoft 365 |

| Help Desk | osTicket |

| Remote Access | VPN Gateway, Microsoft 365, Active Directory |



\---



\# Configuration Item Relationships



```text

Internet

&#x20;       │

Firewall

&#x20;       │

Core Switch

&#x20;       │

──────────────────────────────────────

│          │          │

DC01     FILE01    PRINT01

│          │

│          └─────────────┐

│                        │

Employee PCs         Shared Drives

│

Microsoft 365

│

Outlook

Teams

OneDrive

```



\---



\# Configuration Item Lifecycle



Each Configuration Item follows the lifecycle below.



```text

Requested



↓



Approved



↓



Procured



↓



Configured



↓



Deployed



↓



Maintained



↓



Retired



↓



Disposed

```



\---



\# Business Criticality



| Level | Definition |

|-------|------------|

| Critical | Business operations stop without this service |

| High | Significant business disruption |

| Medium | Reduced productivity |

| Low | Minimal operational impact |



\---



\# Change Management Integration



All production Configuration Items are subject to the organization's Change Management Policy.



Changes involving Configuration Items should include:



\- Approved Change Request

\- Risk Assessment

\- Implementation Plan

\- Rollback Plan

\- Validation

\- CMDB Update



\---



\# Incident Management Integration



During incident response, the CMDB helps identify:



\- Affected systems

\- Service dependencies

\- Asset owners

\- Related infrastructure

\- Potential business impact



\---



\# Security Operations Integration



The CMDB supports Security Operations by providing:



\- Asset ownership

\- Critical system identification

\- Incident scoping

\- Vulnerability prioritization

\- Patch management tracking

\- Risk assessments



\---



\# Maintenance



The CMDB should be reviewed:



\- Monthly

\- Following infrastructure changes

\- After hardware deployments

\- After server decommissioning

\- Following major incidents

\- During annual asset audits



\---



\# Related Documentation



\- Asset-Inventory.md

\- Server-Inventory.md

\- Network-Overview.md

\- IT-Infrastructure.md

\- Security-Policies.md

\- Change-Management-Policy.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | July 2026 | Kenyotta Eave | Initial CMDB overview created. |

