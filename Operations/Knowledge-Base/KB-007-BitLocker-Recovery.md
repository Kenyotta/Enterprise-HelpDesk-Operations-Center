\# KB-007 – BitLocker Recovery



\---



\# Overview



This Knowledge Base article outlines the standard procedure for assisting users who are prompted to enter a BitLocker Recovery Key on a company-managed Windows device.



BitLocker is used throughout the Apex Manufacturing environment to protect data on endpoint devices through full-disk encryption. Recovery should only be performed after the user's identity and device ownership have been verified.



\---



\# Category



Endpoint Security



\---



\# Supported Systems



\- Windows 10 Enterprise

\- Windows 11 Enterprise

\- Microsoft Intune

\- Microsoft Entra ID

\- Active Directory

\- BitLocker Drive Encryption



\---



\# Supported Roles



\- Tier 1 Service Desk (Verification Only)

\- Tier 2 Desktop Support



\---



\# Estimated Resolution Time



\*\*10–20 minutes\*\*



\---



\# Symptoms



Users may report one or more of the following:



\- BitLocker Recovery screen appears during startup

\- Device requests a 48-digit recovery key

\- Windows will not boot normally

\- Recovery screen appears after BIOS or firmware updates

\- Recovery requested after hardware changes

\- Recovery requested after TPM changes



\---



\# Possible Causes



\- TPM validation failure

\- BIOS or UEFI update

\- Motherboard replacement

\- Secure Boot configuration changes

\- Drive moved to another computer

\- Multiple failed boot attempts

\- BitLocker policy changes



\---



\# Required Verification



Before retrieving a recovery key, verify:



\- User identity

\- Device asset tag

\- Computer name

\- Serial number (if available)

\- Device assignment within Asset Inventory

\- Department ownership



> \*\*Important:\*\* Recovery keys must never be provided without verifying the identity of the requester.



\---



\# Resolution Procedure



\## Step 1 – Record Recovery Information



At the BitLocker Recovery screen, ask the user to provide:



\- Recovery Key ID

\- Computer Name (if known)

\- Asset Tag



Do \*\*not\*\* ask the user to read the entire recovery key unless it has already been retrieved by an authorized technician.



\---



\## Step 2 – Locate the Recovery Key



Attempt to retrieve the BitLocker Recovery Key from one of the approved management systems:



Priority order:



1\. Microsoft Intune

2\. Microsoft Entra ID

3\. Active Directory (if stored)

4\. Approved enterprise recovery repository



Confirm the Recovery Key ID matches the device before providing the key.



\---



\## Step 3 – Verify Device Ownership



Confirm the device belongs to:



\- The requesting employee

\- Their assigned department

\- The organization's asset inventory



If ownership cannot be verified, stop the process and escalate.



\---



\## Step 4 – Provide the Recovery Key



Read the 48-digit recovery key carefully to the user.



Advise the user to:



\- Enter each group of digits exactly as provided

\- Verify each section before continuing



Do not send recovery keys through unsecured communication methods unless permitted by company policy.



\---



\## Step 5 – Verify Successful Startup



After entering the recovery key, confirm:



\- Windows loads successfully

\- User signs in

\- Desktop appears normally



\---



\## Step 6 – Determine Why Recovery Occurred



Review recent changes such as:



\- BIOS updates

\- Firmware updates

\- Hardware replacement

\- TPM configuration

\- Windows feature updates

\- Security policy changes



Document the probable cause.



\---



\## Step 7 – Verify BitLocker Protection



After Windows starts:



Open an elevated Command Prompt.



Run:



```cmd

manage-bde -status

```



Confirm:



\- Protection Status: On

\- Drive fully encrypted

\- No recovery actions pending



\---



\# Validation



Verify the following:



\- Recovery key accepted

\- Windows boots normally

\- User successfully signs in

\- BitLocker protection remains enabled

\- No additional recovery prompts appear

\- Device functions normally



\---



\# Common Issues



\## Recovery Key Does Not Match



Possible causes:



\- Wrong device

\- Incorrect Recovery Key ID

\- Outdated recovery information



Resolution:



\- Verify Recovery Key ID

\- Confirm computer name

\- Retrieve the correct recovery key



\---



\## Recovery Key Not Found



Verify:



\- Device enrolled in Microsoft Intune

\- Recovery key escrowed to Microsoft Entra ID

\- Active Directory BitLocker recovery objects exist



Escalate if no recovery key can be located.



\---



\## Recovery Screen Appears Repeatedly



Possible causes:



\- TPM malfunction

\- BIOS configuration changes

\- Secure Boot issues

\- Firmware problems



Escalate for hardware investigation.



\---



\## Windows Boots into Recovery Again



Verify:



\- BitLocker status

\- TPM health

\- Recent BIOS updates

\- Firmware version

\- Device hardware integrity



\---



\# Security Best Practices



\- Verify user identity before releasing recovery information.

\- Never disclose recovery keys to unauthorized individuals.

\- Store recovery keys only in approved enterprise systems.

\- Document every recovery event.

\- Investigate repeated BitLocker recovery requests for potential security concerns.



\---



\# Escalation Criteria



Escalate to Tier 2 if:



\- Recovery key cannot be located

\- Device ownership cannot be verified

\- BitLocker repeatedly enters recovery mode

\- TPM errors are identified

\- Hardware replacement is suspected



Escalate to the Infrastructure or Endpoint Engineering Team if:



\- Multiple devices experience BitLocker recovery simultaneously

\- BitLocker policies require modification

\- Recovery key escrow failures are identified

\- Enterprise-wide encryption issues occur



\---



\# Ticket Documentation Example



\*\*Issue\*\*



User reported their company laptop displayed a BitLocker Recovery screen after a firmware update.



\*\*Resolution\*\*



Verified user identity and device ownership, retrieved the matching recovery key from Microsoft Entra ID, guided the user through entering the recovery key, confirmed successful Windows startup, and verified BitLocker protection remained enabled.



\*\*Status\*\*



Resolved



\---



\# Related Documentation



\- RFC-010-Retire-Legacy-Workstation.md

\- Infrastructure/Asset-Management/

\- Infrastructure/Microsoft-365/

\- Security/Security-Baselines/

\- Asset-Inventory.md

\- CMDB.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting the standard BitLocker recovery procedure for company-managed Windows devices. |

