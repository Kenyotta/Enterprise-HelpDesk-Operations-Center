\# KB-014 – Remote Desktop (RDP) Troubleshooting



\---



\# Overview



This Knowledge Base article provides the standard procedure for diagnosing and resolving Remote Desktop Protocol (RDP) connectivity issues within the Apex Manufacturing enterprise environment.



Remote Desktop enables authorized employees and IT personnel to securely access Windows workstations and servers remotely. This guide assists technicians in determining whether connectivity problems are caused by network connectivity, VPN access, DNS, firewall configuration, Remote Desktop settings, or user permissions.



\---



\# Category



Remote Access



\---



\# Supported Systems



\- Windows 10 Enterprise

\- Windows 11 Enterprise

\- Windows Server 2022

\- Active Directory

\- Microsoft Entra ID

\- Microsoft Intune

\- VPN Client



\---



\# Supported Roles



\- Tier 1 Service Desk

\- Tier 2 Desktop Support

\- Infrastructure Team



\---



\# Estimated Resolution Time



\*\*15–30 minutes\*\*



\---



\# Symptoms



Users may report:



\- "Remote Desktop can't connect to the remote computer."

\- Black screen after connecting

\- Authentication failures

\- Connection times out

\- Remote computer unavailable

\- Login succeeds but session disconnects

\- Unable to locate remote computer



\---



\# Possible Causes



\- Remote computer powered off

\- VPN not connected

\- DNS resolution failure

\- Firewall blocking RDP

\- Remote Desktop disabled

\- User lacks RDP permissions

\- Network outage

\- Incorrect computer name

\- Remote workstation asleep



\---



\# Required Verification



Before troubleshooting, verify:



\- User identity

\- Computer name

\- Asset tag (if available)

\- VPN authorization

\- User has Remote Desktop approval

\- Target computer is assigned to the user



\---



\# Resolution Procedure



\## Step 1 – Verify Internet Connectivity



Confirm the user has internet access.



Run:



```cmd

ping 8.8.8.8

```



If internet connectivity fails:



\- Resolve network connectivity before continuing.



\---



\## Step 2 – Verify VPN Connection



If the user is outside the corporate network:



Confirm the VPN client shows:



```text

Connected

```



If VPN is unavailable:



Follow:



KB-005 – VPN Troubleshooting



\---



\## Step 3 – Verify Computer Name



Confirm the correct computer name.



Example:



```text

FIN-WS-032

```



Avoid using outdated computer names.



\---



\## Step 4 – Verify DNS Resolution



Open Command Prompt.



Run:



```cmd

nslookup FIN-WS-032

```



Confirm the workstation resolves to the correct IP address.



\---



\## Step 5 – Test Network Connectivity



Run:



```cmd

ping FIN-WS-032

```



If successful:



Continue troubleshooting.



If unsuccessful:



Investigate:



\- VPN

\- DNS

\- Network connectivity

\- Firewall



\---



\## Step 6 – Verify Remote Desktop is Enabled



On the remote workstation:



Open:



```text

Settings

System

Remote Desktop

```



Confirm:



\- Remote Desktop is enabled.

\- Remote connections are allowed.



\---



\## Step 7 – Verify User Permissions



Confirm the user is:



\- Local Administrator



or



\- Member of the \*\*Remote Desktop Users\*\* group



Verify access through Active Directory if applicable.



\---



\## Step 8 – Verify Windows Firewall



Confirm Windows Defender Firewall allows:



```text

Remote Desktop

```



TCP Port:



```text

3389

```



Verify firewall policies have not blocked RDP.



\---



\## Step 9 – Verify the Remote Workstation



Confirm:



\- Workstation powered on

\- Not sleeping

\- Connected to the corporate network

\- User not logged off unexpectedly



\---



\## Step 10 – Test Remote Desktop



Launch:



```text

Remote Desktop Connection (mstsc)

```



Connect using:



```text

Computer:

FIN-WS-032



Username:

APEX\\sjohnson

```



Verify successful authentication.



\---



\# Validation



Verify:



\- Remote Desktop connection established

\- User authenticated successfully

\- Desktop loads normally

\- Applications function correctly

\- Session remains connected

\- User can perform required work



\---



\# Common Issues



\## Computer Cannot Be Found



Possible causes:



\- Incorrect computer name

\- DNS failure

\- VPN disconnected



Resolution:



\- Verify computer name

\- Test DNS

\- Reconnect VPN



\---



\## Authentication Failure



Verify:



\- Username

\- Password

\- Domain

\- Account not locked



Follow:



KB-001 – Password Reset



KB-011 – Account Lockout



\---



\## Black Screen



Possible causes:



\- Display driver

\- Session corruption

\- Network latency



Resolution:



\- Disconnect and reconnect

\- Restart the remote workstation if approved

\- Verify network performance



\---



\## Firewall Blocking RDP



Verify:



\- Windows Firewall rule enabled

\- TCP Port 3389 open

\- No conflicting firewall policies



\---



\## User Not Authorized



Verify membership in:



```text

Remote Desktop Users

```



Grant access only after receiving the appropriate approval.



\---



\# Security Best Practices



\- Verify user identity before granting Remote Desktop access.

\- Use VPN when connecting from external networks.

\- Grant Remote Desktop permissions using the Principle of Least Privilege.

\- Remove unnecessary Remote Desktop permissions during offboarding.

\- Document all Remote Desktop access requests and permission changes.



\---



\# Escalation Criteria



Escalate to Tier 2 if:



\- Remote Desktop remains unavailable after basic troubleshooting

\- DNS resolution issues persist

\- Firewall rules require modification

\- Remote Desktop services repeatedly stop



Escalate to the Infrastructure Team if:



\- Multiple users experience Remote Desktop failures

\- VPN gateway outages affect RDP

\- Domain Controllers or DNS servers are unavailable

\- Enterprise firewall changes are required



\---



\# Ticket Documentation Example



\*\*Issue\*\*



Remote employee was unable to connect to their assigned workstation using Remote Desktop.



\*\*Resolution\*\*



Verified VPN connectivity, confirmed DNS resolution, verified Remote Desktop was enabled, confirmed user membership in the Remote Desktop Users group, tested connectivity successfully, and confirmed the employee could access their workstation remotely.



\*\*Status\*\*



Resolved



\---



\# Related Documentation



\- KB-001-Password-Reset.md

\- KB-005-VPN-Troubleshooting.md

\- KB-011-Account-Lockout.md

\- KB-012-Domain-Join-Failure.md

\- Infrastructure/Networking/

\- Infrastructure/Active-Directory/

\- Security-Policies.md

\- CMDB.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting the standard Remote Desktop troubleshooting procedure. |

