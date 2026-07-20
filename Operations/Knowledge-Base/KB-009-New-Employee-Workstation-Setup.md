\# KB-009 – New Employee Workstation Setup



\---



\# Overview



This Knowledge Base article outlines the standard procedure for preparing and deploying a new workstation for an employee at Apex Manufacturing.



The objective is to ensure every workstation is configured consistently, securely, and in accordance with company standards before being issued to the employee.



\---



\# Category



Desktop Support



\---



\# Supported Systems



\- Windows 11 Enterprise

\- Active Directory

\- Microsoft Entra ID

\- Microsoft Intune

\- Microsoft 365

\- BitLocker

\- FILE01

\- PRINT01



\---



\# Supported Roles



\- Tier 1 Service Desk

\- Tier 2 Desktop Support



\---



\# Estimated Resolution Time



\*\*30–60 minutes\*\*



\---



\# Purpose



Proper workstation deployment ensures:



\- Consistent configuration

\- Security compliance

\- Successful domain integration

\- Standard software deployment

\- Immediate employee productivity



\---



\# Prerequisites



Before beginning, verify:



\- Approved onboarding request received

\- Computer asset assigned

\- Employee account created

\- Microsoft 365 license assigned

\- Required software identified

\- Department confirmed



\---



\# Required Information



Collect the following:



| Item | Example |

|------|---------|

| Employee Name | Sarah Johnson |

| Username | sjohnson |

| Department | Finance |

| Computer Name | FIN-WS-032 |

| Asset Tag | WS-2032 |

| Manager | Michael Reynolds |

| Office Location | Dallas Headquarters |



\---



\# Deployment Procedure



\## Step 1 – Verify Hardware



Inspect the workstation for:



\- Physical damage

\- Power adapter

\- Docking station (if assigned)

\- Keyboard

\- Mouse

\- Monitor(s)

\- Network cable (if required)



Record the asset tag.



\---



\## Step 2 – Install Windows Updates



Open:



```

Settings

Windows Update

```



Install:



\- Critical updates

\- Security updates

\- Driver updates approved by IT



Restart if required.



\---



\## Step 3 – Join the Domain



Join the workstation to:



```text

apex.local

```



Verify successful domain membership.



Restart the workstation.



\---



\## Step 4 – Verify Microsoft Entra ID Registration



Confirm the device is:



\- Registered

\- Hybrid Joined (if applicable)

\- Visible within Microsoft Entra ID



Document successful registration.



\---



\## Step 5 – Verify Microsoft Intune Enrollment



Confirm the workstation appears within Microsoft Intune.



Verify:



\- Compliance status

\- Assigned device policies

\- Security baselines

\- Configuration profiles



\---



\## Step 6 – Enable BitLocker



Verify:



\- BitLocker enabled

\- Recovery Key successfully escrowed

\- Encryption completed



Document the Recovery Key location according to company policy.



\---



\## Step 7 – Install Standard Applications



Install approved enterprise software including:



\- Microsoft 365 Apps

\- Microsoft Teams

\- Microsoft Edge

\- Adobe Acrobat Reader

\- VPN Client

\- Endpoint Protection

\- Company-approved browser extensions



Install department-specific applications if required.



\---



\## Step 8 – Configure User Access



Verify access to:



\- Active Directory

\- Microsoft 365

\- Outlook

\- Teams

\- OneDrive

\- Department file shares

\- Network printers

\- VPN (if authorized)



\---



\## Step 9 – Verify Group Policy



Open Command Prompt.



Run:



```cmd

gpupdate /force

```



Verify:



\- Drive mappings

\- Printer deployment

\- Security policies

\- Desktop policies



\---



\## Step 10 – Perform Functional Testing



Sign in using the employee account.



Verify:



\- Desktop loads successfully

\- Outlook opens

\- Teams signs in

\- OneDrive syncs

\- File shares accessible

\- Printer available

\- Internet connectivity

\- Windows activation successful



\---



\## Step 11 – Update Documentation



Update:



\- CMDB

\- Asset Inventory

\- Employee Directory

\- Device assignment records



Record:



\- Computer Name

\- Asset Tag

\- Assigned Employee

\- Deployment Date



\---



\# Validation



Confirm the following:



\- Windows fully updated

\- Domain joined

\- Microsoft Entra ID registered

\- Microsoft Intune compliant

\- BitLocker enabled

\- Microsoft 365 functioning

\- Outlook operational

\- Teams operational

\- OneDrive synchronized

\- Network drives mapped

\- Printer installed

\- Endpoint protection active



\---



\# Common Issues



\## Domain Join Failure



Verify:



\- Network connectivity

\- DNS configuration

\- Active Directory availability

\- Computer name uniqueness



Follow:



KB-012 – Domain Join Failure



\---



\## Microsoft 365 Sign-In Failure



Verify:



\- License assignment

\- Password

\- MFA enrollment

\- Internet connectivity



Follow:



KB-001 – Password Reset



KB-002 – MFA Reset



\---



\## Missing Network Drives



Verify:



\- Group Policy applied

\- Security group membership

\- VPN connection (if remote)



Follow:



KB-003 – Map a Network Drive



\---



\## Printer Not Installed



Verify:



\- Group Policy deployment

\- Printer permissions

\- PRINT01 availability



Follow:



KB-006 – Printer Offline



\---



\# Escalation Criteria



Escalate to Tier 2 if:



\- Intune enrollment fails

\- Domain join unsuccessful

\- BitLocker cannot be enabled

\- Hardware defects identified

\- Microsoft 365 licensing issues persist



Escalate to the Infrastructure Team if:



\- Active Directory unavailable

\- Multiple workstation deployments fail

\- Network services unavailable

\- Enterprise imaging issues identified



\---



\# Ticket Documentation Example



\*\*Issue\*\*



Provision and deploy a new workstation for a Finance employee.



\*\*Resolution\*\*



Configured Windows 11 Enterprise, joined the workstation to the apex.local domain, verified Microsoft Entra ID registration and Intune enrollment, enabled BitLocker, installed standard software, validated Microsoft 365 access, mapped department network drives, confirmed printer deployment, and updated the CMDB and Asset Inventory.



\*\*Status\*\*



Completed



\---



\# Related Documentation



\- FORM-002-New-Employee-Onboarding-Request.md

\- FORM-004-Hardware-Request.md

\- RFC-001-New-Employee-Onboarding.md

\- RFC-010-Retire-Legacy-Workstation.md

\- Infrastructure/Active-Directory/

\- Infrastructure/Asset-Management/

\- Infrastructure/Microsoft-365/

\- Asset-Inventory.md

\- CMDB.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting the standard workstation provisioning and deployment procedure for new employees. |

