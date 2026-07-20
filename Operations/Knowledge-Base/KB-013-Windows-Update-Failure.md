\# KB-013 – Windows Update Failure



\---



\# Overview



This Knowledge Base article provides the standard procedure for diagnosing and resolving Windows Update failures within the Apex Manufacturing enterprise environment.



Windows Updates are essential for maintaining security, stability, and compliance. This guide helps technicians identify whether update failures are caused by connectivity issues, insufficient disk space, corrupted system files, Windows Update services, or enterprise update policies.



\---



\# Category



Windows Operating System



\---



\# Supported Systems



\- Windows 10 Enterprise

\- Windows 11 Enterprise

\- Windows Server 2022

\- Microsoft Intune

\- Windows Update for Business

\- Microsoft Entra ID



\---



\# Supported Roles



\- Tier 1 Service Desk

\- Tier 2 Desktop Support

\- Infrastructure Team



\---



\# Estimated Resolution Time



\*\*20–45 minutes\*\*



\---



\# Symptoms



Users may report:



\- Windows Update stuck at 0%

\- Update download never completes

\- Installation repeatedly fails

\- Update error codes displayed

\- Computer continually requests a restart

\- Feature update will not install

\- Device reports it is not up to date



\---



\# Possible Causes



\- Insufficient disk space

\- Corrupted system files

\- Windows Update service stopped

\- Internet connectivity issues

\- Group Policy restrictions

\- Corrupted SoftwareDistribution folder

\- Enterprise update deployment issues



\---



\# Required Verification



Before troubleshooting, verify:



\- User identity

\- Computer name

\- Asset tag

\- Windows version

\- Internet or corporate network connectivity

\- Available disk space



\---



\# Resolution Procedure



\## Step 1 – Verify Internet Connectivity



Open Command Prompt.



Run:



```cmd

ping 8.8.8.8

```



Then verify Microsoft services are reachable by opening a web browser.



If internet connectivity fails:



\- Resolve the network issue before continuing.



\---



\## Step 2 – Verify Available Disk Space



Open:



```text

Settings

System

Storage

```



Confirm:



\- At least 20 GB of free disk space is available for major feature updates.

\- Temporary files are removed if space is limited.



\---



\## Step 3 – Verify Windows Update Services



Open:



```text

Services

```



Confirm these services are running:



\- Windows Update (wuauserv)

\- Background Intelligent Transfer Service (BITS)

\- Cryptographic Services



Restart any stopped services.



\---



\## Step 4 – Check for Updates



Open:



```text

Settings

Windows Update

```



Select:



```text

Check for updates

```



Document any error code displayed.



\---



\## Step 5 – Repair System Files



Open an elevated Command Prompt.



Run:



```cmd

sfc /scannow

```



Restart the computer if repairs are completed.



\---



\## Step 6 – Repair the Windows Image



Run:



```cmd

DISM /Online /Cleanup-Image /RestoreHealth

```



Allow the repair to complete.



Restart the workstation.



\---



\## Step 7 – Clear the Windows Update Cache



Open an elevated Command Prompt.



Stop Windows Update services:



```cmd

net stop wuauserv

net stop bits

```



Rename the update cache:



```cmd

ren C:\\Windows\\SoftwareDistribution SoftwareDistribution.old

```



Restart the services:



```cmd

net start wuauserv

net start bits

```



Retry Windows Update.



\---



\## Step 8 – Verify Group Policy



Run:



```cmd

gpupdate /force

```



Confirm:



\- Windows Update policies apply successfully.

\- No policy conflicts are present.



\---



\## Step 9 – Restart the Workstation



Restart the computer.



Attempt Windows Update again.



\---



\# Validation



Verify:



\- Updates download successfully

\- Updates install successfully

\- Restart completes normally

\- Windows reports "You're up to date"

\- No update error codes remain



\---



\# Common Issues



\## Update Stuck Downloading



Possible causes:



\- Network interruption

\- Windows Update service issue

\- Corrupted update cache



Resolution:



\- Restart Windows Update services.

\- Clear the SoftwareDistribution folder.

\- Retry the update.



\---



\## Insufficient Disk Space



Resolution:



\- Run Disk Cleanup.

\- Remove temporary files.

\- Delete unnecessary applications or files.

\- Retry the update.



\---



\## Error After Restart



Possible causes:



\- Corrupt system files

\- Driver incompatibility

\- Failed feature update



Resolution:



\- Run SFC and DISM.

\- Review Windows Update history.

\- Roll back the failed update if approved.



\---



\## Enterprise Update Policy Prevents Installation



Verify:



\- Device is receiving the correct Group Policy or Intune update policy.

\- Update deployment has been approved for the device.



Escalate if policy changes are required.



\---



\# Security Best Practices



\- Keep devices fully patched with approved updates.

\- Do not disable Windows Update services permanently.

\- Verify update approval before manually installing feature updates.

\- Document update failures and corrective actions.

\- Confirm endpoint protection remains operational after updates.



\---



\# Escalation Criteria



Escalate to Tier 2 if:



\- Windows Update repeatedly fails after repair procedures

\- SFC or DISM cannot repair the operating system

\- Windows Update services continue stopping unexpectedly

\- Disk corruption is suspected



Escalate to the Infrastructure Team if:



\- Enterprise-wide update failures occur

\- Windows Update for Business policies require modification

\- WSUS or update management infrastructure is unavailable

\- Multiple systems report identical update failures



\---



\# Ticket Documentation Example



\*\*Issue\*\*



User reported Windows Update repeatedly failed during installation with error code 0x80070002.



\*\*Resolution\*\*



Verified internet connectivity and available disk space, restarted Windows Update services, repaired system files using SFC and DISM, cleared the SoftwareDistribution cache, successfully installed pending updates, and confirmed the workstation reported it was fully up to date.



\*\*Status\*\*



Resolved



\---



\# Related Documentation



\- KB-008-Blue-Screen-Troubleshooting.md

\- KB-009-New-Employee-Workstation-Setup.md

\- KB-015-Software-Installation.md

\- RFC-002-Windows-Monthly-Patching.md

\- Infrastructure/Endpoint-Management/

\- Security-Policies.md

\- CMDB.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting the standard Windows Update troubleshooting procedure. |

