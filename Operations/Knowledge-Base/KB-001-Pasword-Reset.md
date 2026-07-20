# KB-001 – Password Reset Procedure

---

# Overview

This Knowledge Base article provides the standard procedure for resetting a user's Active Directory password within the Apex Manufacturing enterprise environment.

Password resets are one of the most common Service Desk requests and should be completed using identity verification procedures to prevent unauthorized account access.

---

# Category

Identity & Access Management

---

# Supported Systems

- Active Directory
- Windows Server 2022
- Microsoft Entra ID (Hybrid)
- Microsoft 365
- Domain-Joined Windows Workstations

---

# Supported Roles

- Tier 1 Service Desk
- Tier 2 Desktop Support

---

# Estimated Resolution Time

**5–10 minutes**

---

# Symptoms

Users may report one or more of the following:

- Unable to log in to Windows
- Incorrect password message
- Password expired
- Unable to access Outlook
- Cannot access VPN
- Microsoft 365 login failures
- Password no longer accepted after recent change

---

# Possible Causes

- Password expired
- Forgotten password
- User entered incorrect password multiple times
- Password synchronization delay
- Recently changed password on another device
- Cached credentials

---

# Required Verification

Before resetting a password, verify the user's identity using at least two approved methods.

Examples include:

- Employee ID
- Manager confirmation
- Corporate badge
- Verified phone number
- Security questions (if applicable)

> **Important:** Never reset a password without verifying the user's identity.

---

# Resolution Procedure

## Step 1 – Open Active Directory Users and Computers

1. Log in to **DC01** with an authorized administrative account.
2. Open **Active Directory Users and Computers (ADUC)**.
3. Locate the user's Organizational Unit (OU).

---

## Step 2 – Locate the User

Search for the user by:

- First Name
- Last Name
- Username
- Employee ID

Verify the correct account before making changes.

---

## Step 3 – Reset the Password

1. Right-click the user account.
2. Select **Reset Password**.
3. Enter a temporary password that meets the organization's password policy.
4. Confirm the password.

---

## Step 4 – Require Password Change

Enable:

- ✅ User must change password at next logon

Unless otherwise approved by management.

Do **not** enable:

- Password never expires
- User cannot change password

Unless specifically authorized.

---

## Step 5 – Unlock the Account (If Necessary)

If the account is locked:

1. Open **Properties**.
2. Select the **Account** tab.
3. Check **Unlock account**.
4. Apply changes.

---

## Step 6 – Inform the User

Provide the temporary password securely.

Advise the user to:

- Log in immediately
- Create a new password
- Avoid reusing previous passwords
- Verify successful access to Microsoft 365 and VPN if applicable

---

# Password Requirements

Passwords must meet company policy.

Minimum requirements:

- At least 12 characters
- Uppercase letter
- Lowercase letter
- Number
- Special character
- Cannot contain username
- Cannot reuse recent passwords

---

# Validation

Confirm the following:

- User successfully signs in
- Password change completed
- Outlook opens successfully
- Microsoft 365 authentication succeeds
- VPN authentication succeeds (if applicable)
- No account lockout remains

---

# Common Issues

## Password Immediately Fails

Possible causes:

- Incorrect username
- Password synchronization delay
- Keyboard layout mismatch
- Caps Lock enabled

---

## User Still Cannot Log In

Verify:

- Correct domain selected
- Account enabled
- Account unlocked
- Network connectivity
- Active Directory replication

---

## Microsoft 365 Still Requests Old Password

Resolution:

- Sign out of Office applications
- Restart Outlook
- Remove cached credentials from Windows Credential Manager if necessary
- Sign back in using the new password

---

# Escalation Criteria

Escalate to Tier 2 if:

- Active Directory replication failures occur
- User account is disabled
- Password reset fails repeatedly
- Trust relationship errors exist
- Domain Controller is unavailable
- Microsoft Entra ID synchronization issues are suspected

---

# Ticket Documentation Example

**Issue**

User unable to sign in after password expiration.

**Resolution**

Verified user identity, reset Active Directory password, unlocked account, required password change at next logon, and confirmed successful Windows and Microsoft 365 authentication.

**Status**

Resolved

---

# Related Documentation

- FORM-001-User-Access-Request.md
- RFC-006-Active-Directory-Group-Modification.md
- Infrastructure/Active-Directory/
- Security-Policies.md
- CMDB.md

---

# Revision History

| Version | Date | Author | Description |
|----------|------|--------|-------------|
| 1.0 | September 2026 | Kenyotta Eave | Initial enterprise knowledge base article documenting the standard Active Directory password reset procedure. |