# KB-001: Password Reset Procedure

## Knowledge Base Information

| Field | Value |
|--------|-------|
| KB ID | KB-001 |
| Category | Active Directory |
| Priority | High |
| Author | Kenyotta Eave |
| Status | Published |
| Last Updated | July 2026 |

---

# Purpose

This article provides the standard procedure for resetting a user's Active Directory password within an enterprise environment.

Password resets are one of the most common Help Desk requests and should always be performed in accordance with organizational security policies and user identity verification procedures.

---

# Scope

This procedure applies to:

- Active Directory user accounts
- Domain-joined Windows workstations
- Standard employee accounts
- Help Desk Level 1 technicians

---

# Common Symptoms

Users may report:

- Forgotten password
- Unable to sign in
- Password expired
- Incorrect password message
- Multiple failed login attempts
- Account requesting password change

---

# Possible Causes

Common causes include:

- Forgotten password
- Expired password
- Password policy enforcement
- User typing incorrect credentials
- Cached credentials
- Account lockout after repeated failed attempts

---

# Prerequisites

Before resetting a password:

- Verify the user's identity.
- Confirm authorization to perform the reset.
- Ensure access to Active Directory Users and Computers (ADUC).
- Review organizational password policies.

Never reset a password without first verifying the user's identity.

---

# Resolution Procedure

## Step 1 – Verify User Identity

Confirm the user's identity using approved verification methods.

Examples may include:

- Employee ID
- Manager verification
- Security questions
- Company-issued identification

---

## Step 2 – Open Active Directory Users and Computers

1. Log in with an administrative account.
2. Open **Active Directory Users and Computers (ADUC)**.
3. Locate the user's Organizational Unit (OU).
4. Select the appropriate user account.

---

## Step 3 – Reset the Password

1. Right-click the user account.
2. Select **Reset Password**.
3. Enter a temporary password.
4. Confirm the password.
5. Enable:

- **User must change password at next logon**

6. Select **OK**.

---

## Step 4 – Inform the User

Provide the temporary password securely.

Do not send passwords through unsecured communication channels.

Inform the user that they will be required to create a new password during their next login.

---

## Step 5 – Test Authentication

If possible:

- Verify the user can successfully sign in.
- Confirm password change is successful.
- Verify access to required resources.

---

# Verification

Successful completion should result in:

- User successfully signs in.
- Password change completed.
- Account functions normally.
- User regains access to required resources.

---

# Troubleshooting

If the user still cannot log in:

- Verify the correct username.
- Confirm the account is not locked.
- Verify domain connectivity.
- Ensure password replication has completed.
- Confirm keyboard layout and Caps Lock status.

---

# Escalation

Escalate the incident if:

- Administrative permissions are unavailable.
- Domain controllers are unreachable.
- Password replication fails.
- Active Directory errors occur.
- Security concerns are identified.

---

# Security Considerations

Always:

- Verify user identity before resetting passwords.
- Never disclose passwords to unauthorized individuals.
- Use temporary passwords only.
- Require password changes at first login.
- Follow organizational password policies.

---

# References

- Microsoft Active Directory Users and Computers
- Organizational Password Policy
- Help Desk Standard Operating Procedures

---

# Revision History

| Version | Date | Description |
|----------|------|-------------|
| 1.0 | July 2026 | Initial publication |