\# IT Infrastructure



\---



\# Apex Manufacturing, Inc.



\## Purpose



This document provides a high-level overview of the Information Technology infrastructure supporting Apex Manufacturing, Inc.



It serves as the primary technical reference for enterprise systems, infrastructure services, endpoint management, networking, identity management, security controls, and operational support.



All infrastructure documentation within this repository should align with the standards defined in this document.



\---



\# Infrastructure Overview



The Apex Manufacturing enterprise environment supports approximately \*\*850 employees\*\* across three corporate locations.



The environment follows a hybrid infrastructure model consisting of:



\- On-premises Active Directory

\- Windows Server infrastructure

\- Microsoft 365 cloud services

\- Azure cloud resources

\- Enterprise networking

\- Centralized Help Desk operations

\- Security monitoring and logging

\- Automated administrative workflows



\---



\# Corporate Locations



| Location | Primary Departments |

|-----------|---------------------|

| Dallas Headquarters | Executive, IT, HR, Finance, Engineering, Marketing |

| Phoenix Distribution Center | Operations, Manufacturing, Warehouse |

| Atlanta Sales Office | Sales, Customer Support |



\---



\# Identity Services



Identity management is centralized through Microsoft Active Directory.



\## Active Directory Domain



```text

apex.local

```



Core services include:



\- Active Directory Domain Services (AD DS)

\- DNS

\- DHCP

\- Organizational Units (OUs)

\- Group Policy Objects (GPOs)

\- Security Groups

\- User and Computer Accounts



\---



\# Core Infrastructure Servers



| Hostname | Function |

|-----------|----------|

| DC01 | Domain Controller |

| FILE01 | File Server |

| PRINT01 | Print Server |

| APP01 | Application Server |

| BACKUP01 | Backup Server |

| MGMT01 | Systems Management |

| WSUS01 | Windows Update Services |

| MONITOR01 | Infrastructure Monitoring |



\---



\# Endpoint Environment



Supported endpoint devices include:



\- Windows 11 Enterprise desktops

\- Windows 11 Enterprise laptops

\- Shared workstations

\- Conference room systems

\- Network printers



Endpoints are joined to the Active Directory domain and managed according to company security standards.



\---



\# Microsoft 365 Services



The organization uses Microsoft 365 to provide collaboration and productivity services.



Primary workloads include:



\- Outlook

\- Exchange Online

\- Microsoft Teams

\- SharePoint Online

\- OneDrive for Business



Future projects will include:



\- Microsoft Intune

\- Microsoft Entra ID

\- Conditional Access

\- Microsoft Defender



\---



\# Azure Services



Azure resources are used to extend the on-premises environment.



Planned services include:



\- Azure Virtual Machines

\- Azure Backup

\- Azure Monitor

\- Azure Storage

\- Azure Networking

\- Azure Update Management

\- Azure Site Recovery



\---



\# Help Desk Platform



The IT department utilizes osTicket as the centralized Help Desk platform.



Core functions include:



\- Incident Management

\- Service Requests

\- Knowledge Base

\- SLA Management

\- Department Routing

\- Ticket Escalation

\- Email Integration

\- Active Directory Authentication



\---



\# Enterprise Networking



Core network services include:



\- Managed switches

\- Enterprise firewall

\- VPN gateway

\- Wireless infrastructure

\- VLAN segmentation

\- DHCP

\- DNS

\- Internet redundancy



\---



\# File Services



Departmental file shares are hosted on FILE01.



Example shared folders include:



\- Human Resources

\- Finance

\- IT

\- Engineering

\- Marketing

\- Operations

\- Public



Access is controlled using Active Directory security groups and NTFS permissions.



\---



\# Print Services



Network printers are centrally managed through PRINT01.



Standard features include:



\- Department printer mapping

\- Driver management

\- Secure printing

\- Printer deployment using Group Policy



\---



\# Backup and Disaster Recovery



Enterprise backup strategy includes:



\- Nightly incremental backups

\- Weekly full backups

\- Monthly archive backups

\- System State backups

\- Virtual machine snapshots

\- Backup verification testing



Recovery priorities are based on business impact.



\---



\# Security Infrastructure



Security technologies include:



\- Microsoft Defender

\- Windows Firewall

\- Multi-Factor Authentication (MFA)

\- BitLocker Drive Encryption

\- Active Directory auditing

\- Event logging

\- Endpoint protection

\- Security awareness training



Planned additions include:



\- Microsoft Sentinel

\- Splunk Enterprise

\- Wazuh

\- Endpoint Detection and Response (EDR)



\---



\# Monitoring and Logging



Infrastructure monitoring includes:



\- Server health

\- Network availability

\- Disk utilization

\- Backup status

\- Windows Event Logs

\- Authentication events

\- Service availability

\- Performance metrics



Monitoring data supports proactive maintenance and incident response.



\---



\# Automation



The environment incorporates automation to improve operational efficiency.



Examples include:



\- PowerShell administration

\- Python automation

\- Automated ticket creation

\- User provisioning

\- Scheduled maintenance scripts

\- Reporting automation



Future repositories will expand automation capabilities across multiple IT disciplines.



\---



\# Documentation Standards



All infrastructure documentation should include:



\- Purpose

\- Scope

\- Prerequisites

\- Implementation steps

\- Validation procedures

\- Rollback procedures

\- Troubleshooting guidance

\- Revision history



\---



\# Related Documentation



This document should be used alongside:



\- Company-Profile.md

\- Organizational-Chart.md

\- Department-Directory.md

\- Employee-Directory.md

\- Asset-Inventory.md

\- Server-Inventory.md

\- Network-Overview.md

\- Naming-Conventions.md

\- Security-Policies.md

\- Change-Management-Policy.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | July 2026 | Kenyotta Eave | Initial IT infrastructure overview created. |

