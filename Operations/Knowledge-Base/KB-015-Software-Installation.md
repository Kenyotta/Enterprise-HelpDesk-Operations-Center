\# KB-015 – Software Installation



\---



\# Overview



This Knowledge Base article outlines the standard procedure for installing approved software on company-managed workstations within the Apex Manufacturing enterprise environment.



Software installations must comply with company security policies, licensing agreements, and endpoint management standards. This procedure ensures software is installed consistently, documented appropriately, and verified after deployment.



\---



\# Category



Desktop Support



\---



\# Supported Systems



\- Windows 10 Enterprise

\- Windows 11 Enterprise

\- Microsoft Intune

\- Microsoft Entra ID

\- Microsoft 365

\- Windows Server 2022



\---



\# Supported Roles



\- Tier 1 Service Desk

\- Tier 2 Desktop Support

\- Endpoint Engineering



\---



\# Estimated Resolution Time



\*\*15–45 minutes\*\*



\---



\# Purpose



This procedure ensures:



\- Approved software is installed securely

\- Licensing requirements are met

\- Administrative access is controlled

\- Software functions correctly after installation

\- Enterprise configuration standards are maintained



\---



\# Prerequisites



Before installing software, verify:



\- Approved software request submitted

\- Manager approval received (if required)

\- Software license available

\- User assigned to the workstation

\- Device compliant in Microsoft Intune

\- Installation package approved by IT



\---



\# Required Information



Collect the following:



| Item | Example |

|------|---------|

| User Name | Sarah Johnson |

| Username | sjohnson |

| Computer Name | FIN-WS-032 |

| Asset Tag | WS-2032 |

| Department | Finance |

| Software Requested | Adobe Acrobat Pro |

| Software Version | 2026.1 |



\---



\# Resolution Procedure



\## Step 1 – Verify Request Approval



Confirm:



\- Service request exists

\- Required approvals are documented

\- Software is included on the Approved Software List



Do not install unapproved software.



\---



\## Step 2 – Verify Device Compliance



Confirm the workstation:



\- Is joined to apex.local

\- Appears in Microsoft Intune

\- Meets security compliance requirements

\- Has current Windows Updates installed



\---



\## Step 3 – Verify Available Disk Space



Open:



```text

Settings

System

Storage

```



Confirm sufficient free space exists for installation.



\---



\## Step 4 – Verify Administrative Access



Determine whether installation requires:



\- Local Administrator rights

\- Endpoint management deployment

\- Elevated privileges



Follow company policy for privileged access.



\---



\## Step 5 – Obtain the Installation Package



Retrieve the installer from an approved source, such as:



\- Microsoft Intune

\- Company Software Repository

\- Approved vendor portal

\- Internal deployment share



Verify the installer version matches the approved release.



\---



\## Step 6 – Install the Software



Launch the installer using approved administrative credentials if required.



Follow vendor installation prompts.



If configuration options are presented:



\- Accept enterprise defaults

\- Install only required features

\- Decline optional third-party software



\---



\## Step 7 – Restart if Required



If prompted:



Restart the workstation.



Verify installation completes successfully after restart.



\---



\## Step 8 – Verify Installation



Confirm the software:



\- Appears in the Start Menu

\- Launches successfully

\- Displays the correct version

\- Activates successfully (if licensed)



\---



\## Step 9 – Verify User Functionality



Ask the user to:



\- Open the application

\- Complete a basic task

\- Confirm expected functionality



Resolve any activation or licensing prompts.



\---



\## Step 10 – Update Asset Records



Document:



\- Software name

\- Version installed

\- Installation date

\- Technician

\- License assignment (if applicable)



Update:



\- Asset Inventory

\- CMDB

\- Software inventory records



\---



\# Validation



Verify:



\- Installation completed successfully

\- Software launches without errors

\- License activated (if applicable)

\- User can perform required tasks

\- No installation warnings remain

\- Endpoint remains compliant



\---



\# Common Issues



\## Installation Blocked



Possible causes:



\- Microsoft Intune policy

\- Windows Defender Application Control

\- Insufficient permissions



Resolution:



\- Verify deployment policy

\- Confirm application approval

\- Retry using authorized administrative credentials



\---



\## License Activation Failure



Verify:



\- License assigned

\- Internet connectivity

\- User signed into the correct Microsoft 365 account

\- Product key (if applicable)



Escalate licensing issues to the Microsoft 365 Administration Team.



\---



\## Application Will Not Launch



Possible causes:



\- Corrupted installation

\- Missing prerequisites

\- Endpoint protection interference



Resolution:



\- Repair the installation

\- Reinstall the application

\- Review Windows Event Viewer for application errors



\---



\## Installation Requires Restart



If the application requests a reboot:



\- Save user work

\- Restart the workstation

\- Verify the application functions normally after restart



\---



\# Security Best Practices



\- Install only approved software.

\- Verify software integrity before installation.

\- Use least-privilege administrative access.

\- Keep installed software updated with approved patches.

\- Document all software installations for audit purposes.



\---



\# Escalation Criteria



Escalate to Tier 2 if:



\- Installation repeatedly fails

\- Software conflicts with existing applications

\- Administrative privileges are unavailable

\- Application crashes after installation



Escalate to Endpoint Engineering if:



\- Enterprise deployment packages require modification

\- Microsoft Intune deployment fails

\- Licensing system failures occur

\- Multiple devices experience the same installation issue



\---



\# Ticket Documentation Example



\*\*Issue\*\*



Finance employee requested installation of Adobe Acrobat Pro for document editing.



\*\*Resolution\*\*



Verified manager approval and software license availability, confirmed device compliance, installed Adobe Acrobat Pro using the approved enterprise installer, restarted the workstation, validated successful activation, confirmed application functionality with the user, and updated the software inventory and CMDB.



\*\*Status\*\*



Resolved



\---



\# Related Documentation



\- KB-009-New-Employee-Workstation-Setup.md

\- KB-013-Windows-Update-Failure.md

\- FORM-005-Software-Installation-Request.md

\- RFC-009-Enterprise-Software-Deployment.md

\- Infrastructure/Endpoint-Management/

\- Asset-Inventory.md

\- CMDB.md

\- Security-Policies.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting the standard enterprise software installation procedure. |

