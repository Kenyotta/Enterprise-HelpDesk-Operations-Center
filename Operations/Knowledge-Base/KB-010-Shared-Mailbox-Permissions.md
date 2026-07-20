\# KB-010 – Shared Mailbox Permissions



\---



\# Overview



This Knowledge Base article outlines the standard procedure for granting, modifying, removing, and verifying access to shared mailboxes within the Apex Manufacturing Microsoft 365 environment.



Shared mailboxes allow multiple authorized employees to send, receive, and manage email from a common mailbox without requiring a separate user license under standard Microsoft licensing guidelines.



\---



\# Category



Microsoft 365 Administration



\---



\# Supported Systems



\- Microsoft 365

\- Exchange Online

\- Microsoft Entra ID

\- Outlook Desktop

\- Outlook on the Web (OWA)

\- Windows 10 Enterprise

\- Windows 11 Enterprise



\---



\# Supported Roles



\- Tier 1 Service Desk

\- Microsoft 365 Administrators



\---



\# Estimated Resolution Time



\*\*10–20 minutes\*\*



\---



\# Purpose



This procedure ensures:



\- Authorized users receive appropriate mailbox access

\- Access requests are documented and approved

\- Permissions follow the Principle of Least Privilege

\- Microsoft 365 security policies remain compliant



\---



\# Permission Types



\## Full Access



Allows the user to:



\- Open the mailbox

\- Read email

\- Move messages

\- Create folders

\- Delete messages

\- Manage mailbox content



Cannot send email as the mailbox unless additional permissions are assigned.



\---



\## Send As



Allows the user to:



\- Send email appearing as the shared mailbox



Recipients cannot determine who actually sent the message.



\---



\## Send on Behalf



Allows the user to send email on behalf of the mailbox.



Example:



```text

Sarah Johnson on behalf of Finance Department

```



\---



\# Prerequisites



Verify:



\- Approved access request received

\- Manager approval documented

\- Mailbox exists

\- User account active

\- Microsoft 365 account licensed (if required)



\---



\# Required Information



Collect:



| Item | Example |

|------|---------|

| User Name | Sarah Johnson |

| Username | sjohnson |

| Department | Finance |

| Shared Mailbox | finance@apexmanufacturing.com |

| Permission Requested | Full Access |

| Request Number | RFC-008 |



\---



\# Resolution Procedure



\## Step 1 – Verify Approval



Confirm:



\- Manager approval

\- Department approval (if required)

\- Security approval for sensitive mailboxes



Do not modify mailbox permissions without documented authorization.



\---



\## Step 2 – Verify User Account



Confirm:



\- Account enabled

\- Password not expired

\- User licensed appropriately

\- Microsoft 365 account active



\---



\## Step 3 – Verify Shared Mailbox Exists



Using the Microsoft 365 Admin Center or Exchange Admin Center, confirm:



\- Mailbox exists

\- Mailbox is healthy

\- Mailbox is not scheduled for deletion



\---



\## Step 4 – Assign Permissions



Assign the approved permission level:



\- Full Access

\- Send As

\- Send on Behalf



Verify permissions are applied successfully.



\---



\## Step 5 – Allow Replication



Microsoft 365 permission changes may require several minutes to propagate.



Advise the user that access may not be immediate.



\---



\## Step 6 – Verify Outlook Access



Have the user:



\- Close Outlook

\- Reopen Outlook

\- Allow mailbox synchronization



If automatic mapping is enabled, verify the shared mailbox appears in the folder list.



If not, manually add the mailbox through Outlook account settings.



\---



\## Step 7 – Test Mailbox Functionality



Verify the user can:



\- Open the mailbox

\- Read messages

\- Create folders

\- Send email (if authorized)

\- Receive new messages

\- Search mailbox contents



\---



\# Validation



Confirm:



\- Mailbox opens successfully

\- Folder structure visible

\- Email synchronization functioning

\- Correct permissions applied

\- User can perform approved actions only



\---



\# Common Issues



\## Shared Mailbox Does Not Appear



Possible causes:



\- Replication delay

\- Outlook cache

\- Auto-mapping delay



Resolution:



\- Restart Outlook

\- Wait for Microsoft 365 replication

\- Manually add the mailbox if necessary



\---



\## Access Denied



Verify:



\- User assigned the correct permissions

\- Permission changes replicated

\- User signed into the correct Microsoft 365 account



\---



\## Cannot Send As Mailbox



Verify:



\- "Send As" permission assigned

\- Outlook restarted after permission change

\- Microsoft 365 replication completed



\---



\## Mailbox Missing from Outlook



Verify:



\- Mailbox still exists

\- Auto-mapping enabled

\- Outlook profile healthy



If Outlook continues to malfunction, follow:



KB-004 – Outlook Profile Repair



\---



\# Security Best Practices



\- Verify all access requests are approved before making changes.

\- Grant the minimum permissions required for the user's job.

\- Remove access promptly when employees change roles or leave the organization.

\- Document every permission change within the ticketing system.

\- Review shared mailbox permissions periodically.



\---



\# Escalation Criteria



Escalate to the Microsoft 365 Administration Team if:



\- Permission changes fail repeatedly

\- Mailbox corruption is suspected

\- Exchange Online synchronization errors occur

\- Multiple users lose mailbox access simultaneously

\- Mailbox restoration is required



\---



\# Ticket Documentation Example



\*\*Issue\*\*



Finance manager requested Full Access and Send As permissions for a newly assigned employee to the Finance shared mailbox.



\*\*Resolution\*\*



Verified management approval, confirmed the user account was active, assigned Full Access and Send As permissions through Exchange Online, confirmed successful permission replication, and verified the user could open the mailbox and send email as the Finance shared mailbox.



\*\*Status\*\*



Resolved



\---



\# Related Documentation



\- FORM-007-Shared-Mailbox-Access-Request.md

\- RFC-008-Department-Mailbox-Creation.md

\- KB-004-Outlook-Profile-Repair.md

\- Infrastructure/Microsoft-365/

\- Security-Policies.md

\- CMDB.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting the standard procedure for managing shared mailbox permissions in Microsoft 365. |

