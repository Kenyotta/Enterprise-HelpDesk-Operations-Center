\# KB-011 – Account Lockout Troubleshooting



\---



\# Overview



This Knowledge Base article outlines the standard procedure for diagnosing and resolving Active Directory account lockouts within the Apex Manufacturing enterprise environment.



Account lockouts commonly occur due to repeated failed authentication attempts from outdated passwords, cached credentials, mobile devices, mapped network drives, scheduled tasks, or applications using stored credentials.



The objective is to restore user access while identifying and correcting the underlying cause to prevent recurring lockouts.



\---



\# Category



Identity and Access Management



\---



\# Supported Systems



\- Windows 10 Enterprise

\- Windows 11 Enterprise

\- Windows Server 2022

\- Active Directory

\- Microsoft Entra ID

\- Microsoft 365

\- VPN Client



\---



\# Supported Roles



\- Tier 1 Service Desk

\- Tier 2 Desktop Support

\- Identity Management Team



\---



\# Estimated Resolution Time



\*\*10–20 minutes\*\*



\---



\# Symptoms



Users may report:



\- "Your account has been locked."

\- Unable to sign into Windows

\- Unable to access Outlook

\- VPN authentication failures

\- Microsoft 365 sign-in failures

\- Password works on one device but not another

\- Account locks again immediately after being unlocked



\---



\# Possible Causes



\- Multiple incorrect password attempts

\- Cached credentials

\- Recently changed password

\- Mobile device using old password

\- VPN client using old credentials

\- Mapped network drives

\- Windows services running under the user account

\- Scheduled tasks

\- Active Directory replication delay



\---



\# Required Verification



Before making changes, verify:



\- User identity

\- Username

\- Department

\- Computer name

\- Manager (if required by policy)



\---



\# Resolution Procedure



\## Step 1 – Verify the Lockout



Confirm the account is locked by checking:



\- Active Directory Users and Computers (ADUC)

\- Identity management tools

\- Help Desk ticket history



Document:



\- Username

\- Time of lockout

\- Number of recent lockouts



\---



\## Step 2 – Unlock the Account



Using Active Directory Users and Computers:



1\. Locate the user account.

2\. Open \*\*Properties\*\*.

3\. Select the \*\*Account\*\* tab.

4\. Check \*\*Unlock account\*\*.

5\. Apply the changes.



Do \*\*not\*\* reset the password unless requested or required.



\---



\## Step 3 – Verify Recent Password Changes



Ask the user:



\- Did you recently change your password?

\- Are you signed into multiple devices?

\- Have you updated your password everywhere?



If a recent password change occurred, continue investigating for stored credentials.



\---



\## Step 4 – Check Common Sources of Cached Credentials



Verify the user has updated their password on:



\- Windows workstation

\- Outlook

\- Microsoft Teams

\- OneDrive

\- Mobile phone

\- Tablet

\- VPN client

\- Remote Desktop connections



\---



\## Step 5 – Review Credential Manager



Open:



```text

Control Panel

Credential Manager

```



Review:



\- Windows Credentials

\- Generic Credentials



Remove outdated credentials referencing:



\- FILE01

\- PRINT01

\- VPN connections

\- Microsoft 365

\- Legacy servers



Restart affected applications after removing outdated entries.



\---



\## Step 6 – Verify Mapped Network Drives



Open Command Prompt.



Run:



```cmd

net use

```



Look for:



\- Disconnected drives

\- Drives using outdated credentials



Reconnect the drives if necessary.



\---



\## Step 7 – Verify Scheduled Tasks and Services



If the account locks immediately after being unlocked, investigate:



\- Windows Services

\- Scheduled Tasks

\- Backup software

\- Scripts

\- Legacy applications



Confirm no services are attempting authentication with an outdated password.



\---



\## Step 8 – Verify Mobile Devices



Ask the user to update saved credentials on:



\- Outlook Mobile

\- Microsoft Teams

\- Company email

\- VPN application



Mobile devices frequently cause repeated account lockouts after password changes.



\---



\## Step 9 – Verify Successful Authentication



Have the user sign into:



\- Windows

\- Microsoft 365

\- Outlook

\- Teams

\- VPN (if applicable)



Confirm authentication succeeds without additional lockouts.



\---



\# Validation



Verify:



\- Account remains unlocked

\- Windows sign-in successful

\- Microsoft 365 authentication successful

\- VPN authentication successful (if applicable)

\- Outlook synchronizes successfully

\- No additional lockout events occur during testing



\---



\# Common Issues



\## Account Locks Again Immediately



Possible causes:



\- Cached credentials

\- Scheduled task

\- Windows service

\- Mobile device

\- VPN client



Resolution:



Identify the authentication source before unlocking the account again.



\---



\## Password Recently Changed



Verify every connected device has been updated with the new password.



Commonly overlooked devices include:



\- Smartphones

\- Tablets

\- VPN clients

\- Remote Desktop sessions



\---



\## VPN Causes Lockout



Verify:



\- VPN client uses current credentials

\- Cached VPN passwords removed

\- User reconnects using updated password



Follow:



KB-005 – VPN Troubleshooting



\---



\## Outlook Repeatedly Prompts for Password



Follow:



KB-004 – Outlook Profile Repair



\---



\# Security Best Practices



\- Verify the user's identity before unlocking an account.

\- Investigate recurring lockouts instead of repeatedly unlocking the account.

\- Remove outdated stored credentials whenever passwords change.

\- Document all account unlock actions.

\- Escalate suspicious lockout activity for security review.



\---



\# Escalation Criteria



Escalate to Tier 2 if:



\- Lockouts continue after cached credentials are removed

\- Scheduled tasks or services require modification

\- Active Directory replication issues are suspected

\- Authentication logs indicate an unknown source



Escalate to the Security Operations Team if:



\- Repeated lockouts originate from unknown systems

\- Brute-force activity is suspected

\- Multiple accounts become locked simultaneously

\- Indicators of compromise are identified



\---



\# Ticket Documentation Example



\*\*Issue\*\*



User reported being unable to sign into Windows because their Active Directory account was locked shortly after changing their password.



\*\*Resolution\*\*



Verified the user's identity, unlocked the Active Directory account, removed outdated credentials from Windows Credential Manager, updated saved credentials on the user's VPN client and mobile device, confirmed successful authentication, and monitored for additional lockout events.



\*\*Status\*\*



Resolved



\---



\# Related Documentation



\- KB-001-Password-Reset.md

\- KB-004-Outlook-Profile-Repair.md

\- KB-005-VPN-Troubleshooting.md

\- KB-010-Shared-Mailbox-Permissions.md

\- FORM-001-Password-Reset-Request.md

\- Infrastructure/Active-Directory/

\- Security-Policies.md

\- CMDB.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting the standard procedure for diagnosing and resolving Active Directory account lockouts. |

