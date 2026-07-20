\# KB-002 – Multi-Factor Authentication (MFA) Reset



\---



\# Overview



This Knowledge Base article outlines the standard procedure for resetting a user's Multi-Factor Authentication (MFA) registration within the Apex Manufacturing enterprise environment.



An MFA reset is performed when a user loses access to their authentication device, replaces their phone, or experiences authentication failures that cannot be resolved through normal troubleshooting.



\---



\# Category



Identity \& Access Management



\---



\# Supported Systems



\- Microsoft Entra ID

\- Microsoft 365

\- Microsoft Authenticator

\- Azure Portal

\- Windows 10

\- Windows 11



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



\- New phone cannot receive MFA prompts

\- Microsoft Authenticator not working

\- Unable to approve sign-in requests

\- Lost or stolen mobile device

\- MFA prompt never appears

\- Verification code rejected

\- Sign-in blocked because of MFA



\---



\# Possible Causes



\- Mobile device replaced

\- Microsoft Authenticator removed

\- Lost or stolen phone

\- Corrupted Authenticator app

\- Expired authentication session

\- Incorrect device time

\- User registered the wrong device



\---



\# Required Verification



Before resetting MFA, verify the user's identity using at least two approved verification methods.



Examples include:



\- Employee ID

\- Manager confirmation

\- Corporate badge

\- Verified phone number

\- Security questions (if applicable)



> \*\*Important:\*\* Never reset a user's MFA registration without confirming their identity.



\---



\# Resolution Procedure



\## Step 1 – Open Microsoft Entra Admin Center



1\. Sign in using an authorized administrative account.

2\. Open the Microsoft Entra Admin Center.

3\. Navigate to:



```

Users

```



4\. Search for the affected employee.



\---



\## Step 2 – Verify the Correct User



Confirm:



\- Display Name

\- Username

\- Department

\- Manager



Ensure the correct account has been selected before making changes.



\---



\## Step 3 – Review Authentication Methods



Open the user's authentication methods and verify the registered MFA devices.



Look for:



\- Microsoft Authenticator

\- Phone Number

\- FIDO2 Security Key

\- Temporary Access Pass (if used)



\---



\## Step 4 – Reset MFA Registration



Select the option to require the user to re-register their authentication methods.



Confirm the action.



\---



\## Step 5 – Remove Obsolete Devices



If outdated devices remain registered:



\- Remove old mobile devices

\- Remove inactive authentication methods

\- Keep only approved authentication methods



\---



\## Step 6 – Instruct the User



Ask the user to:



1\. Sign in to Microsoft 365.

2\. Follow the MFA setup wizard.

3\. Install Microsoft Authenticator (if needed).

4\. Scan the QR code.

5\. Complete the test notification.

6\. Configure an additional authentication method if required.



\---



\# Validation



Verify the following:



\- User successfully signs in

\- MFA prompt received

\- Authentication approved

\- Microsoft 365 accessible

\- Outlook functioning

\- Teams functioning

\- VPN authentication successful (if applicable)



\---



\# Common Issues



\## QR Code Will Not Scan



Possible causes:



\- Camera permissions disabled

\- Low screen brightness

\- Incorrect Authenticator application

\- Damaged display



Resolution:



\- Increase screen brightness

\- Clean camera lens

\- Verify Microsoft Authenticator is installed

\- Enter the setup code manually if necessary



\---



\## No MFA Notification



Verify:



\- Internet connectivity

\- Notification permissions enabled

\- Device time synchronized

\- Microsoft Authenticator running

\- Battery optimization disabled for the app



\---



\## Verification Code Rejected



Possible causes:



\- Incorrect device time

\- Wrong account selected

\- Expired authentication code



Resolution:



\- Synchronize device time

\- Reopen Authenticator

\- Generate a new verification code



\---



\## User Lost Their Phone



If the user no longer has access to their registered device:



1\. Verify identity.

2\. Reset MFA registration.

3\. Remove the old device.

4\. Register the replacement device.



\---



\# Security Best Practices



Advise users to:



\- Register at least two authentication methods.

\- Keep recovery information current.

\- Report lost or stolen devices immediately.

\- Never approve unexpected MFA requests.

\- Never share authentication codes.



\---



\# Escalation Criteria



Escalate to Tier 2 if:



\- Authentication methods cannot be modified

\- Microsoft Entra ID synchronization issues occur

\- Conditional Access policies block sign-in

\- User account is disabled

\- Repeated MFA failures continue after reset



Escalate to the Identity \& Access Management Team if:



\- Authentication policies require modification

\- Security concerns are identified

\- Suspicious login activity is detected



\---



\# Ticket Documentation Example



\*\*Issue\*\*



User replaced their mobile phone and could no longer complete Microsoft 365 Multi-Factor Authentication.



\*\*Resolution\*\*



Verified user identity, reset MFA registration, removed the previous device, guided the user through Microsoft Authenticator setup, and confirmed successful sign-in.



\*\*Status\*\*



Resolved



\---



\# Related Documentation



\- FORM-010-MFA-Reset-Request.md

\- KB-001-Password-Reset.md

\- RFC-005-VPN-Configuration-Change.md

\- Infrastructure/Microsoft-365/

\- Security-Policies.md

\- CMDB.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting the standard Microsoft Entra ID Multi-Factor Authentication reset procedure. |

