\# KB-004 – Outlook Profile Repair



\---



\# Overview



This Knowledge Base article outlines the standard procedure for diagnosing and repairing Microsoft Outlook profile issues within the Apex Manufacturing enterprise environment.



Outlook profile corruption can prevent users from sending or receiving email, accessing calendars, or connecting to Microsoft Exchange Online. This guide provides a structured troubleshooting process before creating a new Outlook profile.



\---



\# Category



Microsoft 365



\---



\# Supported Systems



\- Windows 10 Enterprise

\- Windows 11 Enterprise

\- Microsoft Outlook

\- Exchange Online

\- Microsoft 365

\- Microsoft Entra ID



\---



\# Supported Roles



\- Tier 1 Service Desk

\- Tier 2 Desktop Support



\---



\# Estimated Resolution Time



\*\*15–30 minutes\*\*



\---



\# Symptoms



Users may report one or more of the following:



\- Outlook will not open

\- "Cannot start Microsoft Outlook"

\- Outlook freezes during startup

\- Outlook repeatedly asks for credentials

\- Email is not syncing

\- Calendar is not updating

\- Search functionality is not working

\- Outlook crashes unexpectedly



\---



\# Possible Causes



\- Corrupted Outlook profile

\- Damaged OST file

\- Cached credentials

\- Microsoft 365 authentication issues

\- Network connectivity problems

\- Corrupt Outlook add-ins

\- Windows profile corruption



\---



\# Required Verification



Before making changes, verify:



\- User identity

\- Microsoft 365 license assignment

\- Internet connectivity

\- Windows login successful

\- Issue affects Outlook only



\---



\# Resolution Procedure



\## Step 1 – Verify Microsoft 365 Service Status



Confirm there are no known Microsoft 365 service outages.



Verify:



\- Exchange Online

\- Outlook

\- Microsoft Authentication services



If a service outage exists, document the incident and notify the user.



\---



\## Step 2 – Verify Network Connectivity



Open Command Prompt.



Run:



```cmd

ping outlook.office.com

```



Expected Result:



Successful replies are received.



\---



\## Step 3 – Launch Outlook in Safe Mode



Press:



```

Windows + R

```



Run:



```cmd

outlook.exe /safe

```



If Outlook opens successfully:



\- Disable unnecessary add-ins

\- Restart Outlook normally

\- Verify issue resolved



\---



\## Step 4 – Clear Cached Credentials



Open:



```

Control Panel

Credential Manager

Windows Credentials

```



Remove outdated Microsoft Office and Outlook credentials.



Restart Outlook.



\---



\## Step 5 – Repair Microsoft Office



Navigate to:



```

Settings

Apps

Installed Apps

Microsoft 365 Apps

Modify

```



Select:



\- Quick Repair



If unsuccessful:



\- Online Repair



Restart the workstation after the repair completes.



\---



\## Step 6 – Create a New Outlook Profile



Open:



```

Control Panel

Mail (Microsoft Outlook)

Show Profiles

```



Select:



```

Add

```



Create a new Outlook profile.



Configure the user's Microsoft 365 account.



Set the new profile as the default profile.



\---



\## Step 7 – Verify Mailbox Synchronization



Open Outlook.



Confirm:



\- Inbox loads

\- Calendar loads

\- Contacts appear

\- New email synchronizes

\- Search functions correctly



\---



\# Validation



Verify the following:



\- Outlook opens normally

\- User successfully authenticates

\- Email synchronization working

\- Calendar synchronization working

\- Send/Receive successful

\- Search functioning normally

\- No repeated credential prompts



\---



\# Common Issues



\## Outlook Keeps Asking for Password



Possible causes:



\- Cached credentials

\- Expired password

\- MFA issues

\- Corrupt authentication token



Resolution:



\- Clear Windows Credential Manager

\- Verify password

\- Complete MFA authentication

\- Restart Outlook



\---



\## OST File Corruption



Symptoms:



\- Missing mail

\- Slow synchronization

\- Frequent crashes



Resolution:



1\. Close Outlook.

2\. Rename the OST file.

3\. Restart Outlook.

4\. Allow Outlook to recreate the OST file.



\---



\## Outlook Search Not Working



Run the Windows Search Index Troubleshooter.



If necessary:



\- Rebuild the search index.

\- Restart Outlook.



\---



\## Outlook Will Not Open



Verify:



\- Office installation

\- Add-ins

\- Windows Event Viewer

\- Microsoft 365 service status



Attempt Safe Mode before creating a new profile.



\---



\# Escalation Criteria



Escalate to Tier 2 if:



\- Multiple profile recreations fail

\- Mailbox corruption suspected

\- Microsoft 365 licensing issues identified

\- Exchange Online synchronization problems occur

\- Windows user profile corruption suspected



Escalate to the Microsoft 365 Administration Team if:



\- Mailbox repair is required

\- Exchange Online configuration changes are needed

\- Tenant-wide issues are identified



\---



\# Ticket Documentation Example



\*\*Issue\*\*



User reported Outlook would not open and repeatedly requested credentials.



\*\*Resolution\*\*



Verified Microsoft 365 availability, cleared cached credentials, launched Outlook in Safe Mode, created a new Outlook profile, and confirmed successful mailbox synchronization.



\*\*Status\*\*



Resolved



\---



\# Related Documentation



\- KB-001-Password-Reset.md

\- KB-002-MFA-Reset.md

\- RFC-009-New-Shared-Mailbox-Deployment.md

\- Infrastructure/Microsoft-365/

\- Security-Policies.md

\- CMDB.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting Outlook profile repair and troubleshooting procedures. |

