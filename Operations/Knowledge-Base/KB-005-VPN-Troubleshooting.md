\# KB-005 – VPN Troubleshooting



\---



\# Overview



This Knowledge Base article provides the standard procedure for diagnosing and resolving Virtual Private Network (VPN) connectivity issues within the Apex Manufacturing enterprise environment.



The corporate VPN provides secure remote access to internal resources including file shares, Remote Desktop, intranet applications, and Microsoft services. This guide helps technicians identify common VPN issues and restore secure connectivity.



\---



\# Category



Remote Access



\---



\# Supported Systems



\- Windows 10 Enterprise

\- Windows 11 Enterprise

\- Corporate VPN Client

\- Microsoft Entra ID

\- Microsoft Authenticator

\- Active Directory

\- VPN Gateway



\---



\# Supported Roles



\- Tier 1 Service Desk

\- Tier 2 Desktop Support



\---



\# Estimated Resolution Time



\*\*15–20 minutes\*\*



\---



\# Symptoms



Users may report one or more of the following:



\- Unable to connect to the VPN

\- VPN disconnects unexpectedly

\- Authentication failed

\- VPN client will not launch

\- Connected to VPN but unable to access internal resources

\- Slow VPN performance

\- MFA prompt not received

\- "Server unavailable" message



\---



\# Possible Causes



\- No internet connectivity

\- Incorrect username or password

\- Expired password

\- MFA failure

\- VPN gateway unavailable

\- Outdated VPN client

\- DNS resolution issues

\- Firewall blocking VPN traffic

\- User account not authorized for VPN access



\---



\# Required Verification



Before troubleshooting, verify:



\- User identity

\- Remote work authorization (if applicable)

\- VPN access approval

\- Internet connectivity

\- Device is company-managed or approved



\---



\# Resolution Procedure



\## Step 1 – Verify Internet Connectivity



Open a web browser and confirm the user can access public websites.



Alternatively, run:



```cmd

ping 8.8.8.8

```



If internet connectivity is unavailable:



\- Troubleshoot the local network connection.

\- Do not continue VPN troubleshooting until internet access is restored.



\---



\## Step 2 – Verify VPN Client Status



Confirm:



\- VPN client is installed

\- Application launches normally

\- Latest approved version is installed

\- No error messages appear during startup



Restart the VPN client if necessary.



\---



\## Step 3 – Verify User Credentials



Confirm the user is entering:



\- Correct username

\- Current password

\- Correct domain (if applicable)



If the password has expired, follow:



\- KB-001 – Password Reset Procedure



\---



\## Step 4 – Verify MFA Authentication



Ask the user whether they received an MFA prompt.



If no prompt appears:



\- Verify Microsoft Authenticator notifications

\- Confirm the correct authentication method is registered

\- Follow KB-002 – MFA Reset if necessary



\---



\## Step 5 – Connect to the VPN



Initiate a VPN connection.



Confirm:



\- Authentication successful

\- VPN status displays "Connected"

\- IP address assigned successfully



\---



\## Step 6 – Verify Internal Resource Access



After connecting, verify access to internal resources.



Examples:



```text

\\\\FILE01

```



```text

https://helpdesk.apex.local

```



Confirm the user can:



\- Access shared drives

\- Open internal web applications

\- Reach Remote Desktop resources (if authorized)



\---



\## Step 7 – Verify DNS Resolution



Open Command Prompt.



Run:



```cmd

nslookup FILE01

```



Expected Result:



The correct internal IP address is returned.



\---



\## Step 8 – Restart the Workstation



If all previous steps fail:



1\. Disconnect VPN.

2\. Restart the workstation.

3\. Launch the VPN client.

4\. Attempt a new connection.



\---



\# Validation



Verify the following:



\- VPN connection established

\- MFA completed successfully

\- Internal file shares accessible

\- Internal applications accessible

\- DNS resolution functioning

\- No authentication errors remain

\- User can continue normal work



\---



\# Common Issues



\## Authentication Failed



Possible causes:



\- Incorrect password

\- Expired password

\- Disabled account

\- Account lockout



Resolution:



\- Verify credentials

\- Reset password if required

\- Unlock account if necessary

\- Confirm account is enabled



\---



\## No MFA Prompt



Verify:



\- Internet connectivity

\- Notification permissions

\- Registered authentication device

\- Microsoft Authenticator configuration



If necessary:



\- Reset MFA registration



\---



\## Connected but Cannot Access Internal Resources



Possible causes:



\- DNS failure

\- Split tunneling configuration

\- File server unavailable

\- Firewall restrictions



Resolution:



\- Verify DNS resolution

\- Ping internal resources

\- Verify routing

\- Escalate if infrastructure issues are suspected



\---



\## VPN Disconnects Frequently



Possible causes:



\- Weak internet connection

\- Wireless interference

\- VPN client bug

\- Gateway instability



Resolution:



\- Test on a wired connection if possible

\- Update the VPN client

\- Restart the VPN service

\- Review VPN logs



\---



\## Slow VPN Performance



Verify:



\- User internet speed

\- Active downloads

\- VPN server load

\- Background applications consuming bandwidth



Advise the user to pause unnecessary downloads and retry.



\---



\# Escalation Criteria



Escalate to Tier 2 if:



\- VPN client repeatedly crashes

\- Internal resources remain inaccessible after successful connection

\- DNS or routing issues persist

\- VPN configuration requires modification

\- User requires advanced client reconfiguration



Escalate to the Network Infrastructure Team if:



\- VPN gateway is unavailable

\- Multiple users report identical issues

\- Firewall or routing changes are required

\- VPN certificate or gateway issues are identified



\---



\# Ticket Documentation Example



\*\*Issue\*\*



Remote employee unable to connect to the corporate VPN after changing their password.



\*\*Resolution\*\*



Verified internet connectivity, confirmed updated credentials, completed MFA verification, established a successful VPN connection, and validated access to internal file shares and corporate applications.



\*\*Status\*\*



Resolved



\---



\# Related Documentation



\- KB-001-Password-Reset.md

\- KB-002-MFA-Reset.md

\- KB-003-Map-Network-Drive.md

\- RFC-005-VPN-Configuration-Change.md

\- Infrastructure/Networking/

\- Infrastructure/Microsoft-365/

\- Security-Policies.md

\- CMDB.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting standard VPN troubleshooting procedures for remote users. |

