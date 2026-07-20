\# Naming Conventions



\---



\# Apex Manufacturing, Inc.



\## Purpose



This document defines the official naming standards used throughout the Apex Manufacturing enterprise environment.



Consistent naming conventions improve administration, troubleshooting, automation, reporting, and documentation. All newly created IT resources should follow the standards outlined in this document.



\---



\# General Guidelines



All IT resource names should:



\- Be descriptive and meaningful.

\- Use approved abbreviations.

\- Avoid spaces and special characters unless required.

\- Remain consistent across all environments.

\- Be unique within their respective systems.



\---



\# Active Directory Domain



| Resource | Standard |

|----------|----------|

| Domain Name | apex.local |

| NetBIOS Name | APEX |



\---



\# User Accounts



\## Standard User Accounts



\*\*Format\*\*



```text

First Initial + Last Name

```



\*\*Examples\*\*



```text

keave

dmiller

ajohnson

smitchell

```



\---



\## Administrative Accounts



Administrative accounts use a dedicated prefix.



\*\*Format\*\*



```text

adm-username

```



\*\*Examples\*\*



```text

adm-dmiller

adm-ajohnson

adm-smartinez

```



Administrative accounts should only be used for privileged tasks and must not be used for daily activities.



\---



\# Computer Names



\## Laptops



\*\*Format\*\*



```text

LT-<DEPARTMENT>-###

```



Examples:



```text

LT-IT-001

LT-HR-004

LT-FIN-012

LT-SLS-008

```



\---



\## Desktop Workstations



\*\*Format\*\*



```text

DT-<DEPARTMENT>-###

```



Examples:



```text

DT-OPS-001

DT-MFG-010

DT-ENG-007

```



\---



\## Shared Kiosks



\*\*Format\*\*



```text

KSK-###

```



Examples:



```text

KSK-001

KSK-002

```



\---



\# Servers



\*\*Format\*\*



```text

SRV-<FUNCTION>-##

```



Examples:



```text

SRV-DC-01

SRV-FILE-01

SRV-PRINT-01

SRV-APP-01

SRV-BACKUP-01

SRV-WSUS-01

SRV-MGMT-01

SRV-MON-01

```



Hostnames may use shorter names where appropriate:



```text

DC01

FILE01

PRINT01

APP01

BACKUP01

```



\---



\# Organizational Units (OUs)



```text

Corporate

├── Users

├── Computers

├── Servers

├── Groups

├── Service Accounts

└── Departments

```



Department OUs include:



\- Executive

\- IT

\- HR

\- Finance

\- Sales

\- Marketing

\- Engineering

\- Operations

\- Customer Support



\---



\# Security Groups



\*\*Format\*\*



```text

SG-Department-Permission

```



Examples:



```text

SG-IT-Admins

SG-HR-Users

SG-FIN-Modify

SG-SALES-Read

```



\---



\# Distribution Groups



\*\*Format\*\*



```text

DL-Department

```



Examples:



```text

DL-IT

DL-HR

DL-Finance

DL-AllEmployees

```



\---



\# Shared Folders



\*\*Format\*\*



```text

\\\\FILE01\\Department

```



Examples:



```text

\\\\FILE01\\IT

\\\\FILE01\\Finance

\\\\FILE01\\HR

\\\\FILE01\\Engineering

```



\---



\# Network Printers



\*\*Format\*\*



```text

PRN-Location-##

```



Examples:



```text

PRN-HQ-01

PRN-HR-01

PRN-FIN-01

PRN-OPS-01

```



\---



\# Asset Tags



Asset tags follow the format:



```text

AST-#####

```



Examples:



```text

AST-10001

AST-10542

AST-11237

```



\---



\# Ticket Numbers



The Help Desk system uses the following prefixes.



| Ticket Type | Prefix |

|-------------|--------|

| Incident | INC-YYYY-0001 |

| Service Request | SR-YYYY-0001 |

| Change Request | CHG-YYYY-0001 |

| Problem | PRB-YYYY-0001 |



Examples:



```text

INC-2026-0042

SR-2026-0187

CHG-2026-0015

PRB-2026-0003

```



\---



\# Knowledge Base Articles



\*\*Format\*\*



```text

KB-###

```



Examples:



```text

KB-001 Password Reset Procedure

KB-002 Account Unlock

KB-003 Outlook Troubleshooting

```



\---



\# Standard Operating Procedures (SOPs)



\*\*Format\*\*



```text

SOP-###

```



Examples:



```text

SOP-001 User Onboarding

SOP-002 Password Reset

SOP-003 New Computer Deployment

```



\---



\# Scripts



Automation scripts should use lowercase with underscores.



Examples:



```text

create\_user.ps1

disable\_user.ps1

backup\_report.py

ticket\_report.py

```



\---



\# Documentation Files



Documentation should use Title Case with hyphens.



Examples:



```text

Company-Profile.md

Employee-Directory.md

Server-Inventory.md

Security-Policies.md

```



\---



\# Version Control



Documentation revisions follow semantic versioning.



| Version | Meaning |

|----------|----------|

| 1.0 | Initial release |

| 1.1 | Minor updates |

| 1.2 | Documentation improvements |

| 2.0 | Major revisions |



\---



\# Exceptions



Exceptions to these naming conventions require approval from the Information Technology Manager and must be documented.



\---



\# Related Documentation



\- Company-Profile.md

\- Employee-Directory.md

\- Asset-Inventory.md

\- Server-Inventory.md

\- IT-Infrastructure.md

\- Change-Management-Policy.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | July 2026 | Kenyotta Eave | Initial naming convention standards established. |

