\# KB-003 – Map a Network Drive



\---



\# Overview



This Knowledge Base article provides the standard procedure for mapping a network drive to a user's workstation within the Apex Manufacturing enterprise environment.



Mapped network drives provide employees with secure access to departmental file shares hosted on enterprise file servers.



\---



\# Category



File Services



\---



\# Supported Systems



\- Windows 10 Enterprise

\- Windows 11 Enterprise

\- Active Directory

\- FILE01 File Server

\- SMB File Shares

\- Group Policy



\---



\# Supported Roles



\- Tier 1 Service Desk

\- Tier 2 Desktop Support



\---



\# Estimated Resolution Time



\*\*10–15 minutes\*\*



\---



\# Symptoms



Users may report one or more of the following:



\- Missing network drive

\- "Network path not found" error

\- "Access is denied" message

\- Unable to save files

\- Red X displayed on mapped drive

\- File Explorer freezes when opening the drive

\- Shared folder not visible



\---



\# Possible Causes



\- User not connected to the corporate network or VPN

\- Incorrect drive mapping

\- Missing Active Directory permissions

\- File server unavailable

\- DNS resolution failure

\- Expired user credentials

\- Group Policy not applied



\---



\# Required Verification



Before making changes, verify:



\- User identity

\- Department

\- Assigned file share

\- Device is domain joined

\- VPN connection status (if remote)



\---



\# Resolution Procedure



\## Step 1 – Verify Network Connectivity



Confirm the workstation is connected to:



\- Corporate network

\- Approved VPN (if remote)



Open Command Prompt and test connectivity:



```cmd

ping FILE01

```



Expected Result:



Replies are received successfully.



\---



\## Step 2 – Verify File Server Availability



Confirm FILE01 is online.



Test access using File Explorer:



```text

\\\\FILE01

```



If the server cannot be reached:



\- Verify DNS resolution

\- Confirm server availability

\- Escalate if necessary



\---



\## Step 3 – Verify User Permissions



Open \*\*Active Directory Users and Computers\*\*.



Verify the user belongs to the required security group.



Examples:



\- Finance\_FileShare\_RW

\- HR\_FileShare\_RW

\- IT\_FileShare\_RW



If group membership is incorrect:



\- Submit an access request if required.

\- Follow the approved access management process.



\---



\## Step 4 – Map the Network Drive



Open \*\*File Explorer\*\*.



1\. Select \*\*This PC\*\*.

2\. Click \*\*Map Network Drive\*\*.

3\. Choose an available drive letter.

4\. Enter the network path.



Example:



```text

\\\\FILE01\\Finance

```



Enable:



\- ✔ Reconnect at sign-in



Select \*\*Finish\*\*.



\---



\## Step 5 – Authenticate (If Prompted)



If prompted:



\- Enter domain credentials.

\- Verify the correct domain is selected.

\- Save credentials only if permitted by company policy.



\---



\## Step 6 – Test Access



Confirm the user can:



\- Open folders

\- Create a test document

\- Save changes

\- Delete the test document (if appropriate)

\- Browse subfolders



\---



\# Validation



Verify the following:



\- Network drive appears in File Explorer

\- User can browse folders

\- Read permissions function correctly

\- Write permissions function correctly (if authorized)

\- Drive reconnects after logoff/logon

\- No access errors remain



\---



\# Common Issues



\## Network Path Not Found



Possible causes:



\- VPN disconnected

\- DNS failure

\- Incorrect UNC path

\- File server offline



Resolution:



\- Verify VPN connection

\- Ping FILE01

\- Confirm the UNC path

\- Contact Infrastructure if FILE01 is unavailable



\---



\## Access Is Denied



Verify:



\- Active Directory group membership

\- NTFS permissions

\- Share permissions

\- User is accessing the correct department share



If permissions appear correct but access still fails, escalate to Tier 2.



\---



\## Red X on Drive



Possible causes:



\- Temporary network interruption

\- VPN disconnected

\- File server restarted



Resolution:



\- Open the mapped drive.

\- Reconnect VPN.

\- Refresh File Explorer.

\- Remap the drive if necessary.



\---



\## Drive Does Not Reconnect After Restart



Verify:



\- "Reconnect at sign-in" was selected.

\- Group Policy has applied successfully.



Run:



```cmd

gpupdate /force

```



Restart the workstation if required.



\---



\# Escalation Criteria



Escalate to Tier 2 if:



\- File server is unreachable

\- NTFS permissions require modification

\- Share permissions require modification

\- Group Policy fails repeatedly

\- DNS resolution problems persist

\- Drive mappings fail across multiple users



Escalate to the Infrastructure Team if:



\- FILE01 is offline

\- Storage issues are detected

\- Network-wide file access problems occur



\---



\# Ticket Documentation Example



\*\*Issue\*\*



User unable to access the Finance shared drive after receiving a new workstation.



\*\*Resolution\*\*



Verified VPN connectivity, confirmed Active Directory group membership, mapped the Finance network drive using the approved UNC path, validated read/write access, and confirmed successful reconnection after user sign-in.



\*\*Status\*\*



Resolved



\---



\# Related Documentation



\- KB-009-New-Employee-Workstation-Setup.md

\- RFC-006-Active-Directory-Group-Modification.md

\- Infrastructure/Servers/

\- Infrastructure/Active-Directory/

\- Asset-Inventory.md

\- CMDB.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting the standard procedure for mapping and troubleshooting network drives. |

