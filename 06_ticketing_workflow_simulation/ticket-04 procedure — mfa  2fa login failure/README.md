# Ticket-04 — MFA / 2FA Login Failure (Incident Workflow)

## Ticket Information
- Ticket ID: INC-4001
- Ticket Type: Incident
- Reported By: testuser2
- Department: HR
- Environment: Microsoft 365 / Microsoft Entra ID
- Date Logged: 13 Feb 2026

---

## Issue Summary
User reported being unable to complete Multi-Factor Authentication (MFA) during Microsoft 365 login, preventing access to corporate email and cloud services.

---

## Classification
- Category: Identity & Security
- Subcategory: MFA Authentication Failure

---

## Priority & SLA
- Priority: P2 (User access blocked)
- SLA Target:
  - Response: 1 hour
  - Resolution: 4 hours

---

## Assignment Group
- Assigned To: Identity & Access Management Service Desk
- Escalation Group: Security Operations / Entra ID Engineering

---

# 🧪 Incident Investigation & Resolution Steps

---

## 1) User Login Attempt & MFA Failure

User attempted login via Microsoft 365 portal and was prompted for Multi-Factor Authentication approval through Microsoft Authenticator.

Authentication could not be completed, resulting in access failure.

![MFA Login Failure](images/01-mfa-login-failure.png)

---

## 2) Admin Accessed User Profile in Entra ID

Admin navigated to Microsoft Entra Admin Center and located the affected user account for investigation.

Path:
Entra Admin Center → Users → All Users → testuser2

![User Profile](images/02-user-profile-entra.png)

---

## 3) Authentication Methods Review

Admin opened the Authentication Methods blade to review registered MFA devices and sign-in methods.

This step validates whether the user has properly configured authentication factors.

![Authentication Methods](images/03-auth-methods-view.png)

---

## 4) Reset MFA Registration

Admin performed identity remediation by resetting the user’s authentication methods.

Action performed:

- Require re-register MFA
- Reset authentication methods

This forced the user to configure MFA again securely.

![Reset MFA Methods](images/04-reset-mfa-methods.png)

---

# 🧪 User Re-Registration Workflow

---

## 5) MFA Setup Prompt Triggered

User attempted login again and was presented with a forced MFA re-registration prompt.

System message:

“Let’s keep your account secure — set up Microsoft Authenticator.”

![MFA Setup Prompt](images/05-mfa-setup-prompt.png)

---

## 6) Authenticator Registration

User completed MFA enrollment:

- Installed Microsoft Authenticator
- Linked account
- Approved sign-in verification

![Authenticator Registration](images/06-authenticator-registration.png)

---

# ✅ Resolution Validation

---

## 7) Successful MFA Login

User successfully authenticated using newly configured MFA method and gained access to Microsoft 365 services.

![Successful Login](images/07-successful-mfa-login.png)

---

# 🧾 Root Cause Analysis

Authentication failure occurred due to outdated or non-functional MFA registration tied to the user account.

Resetting authentication methods resolved the issue.

---

# 🛠️ Resolution Actions Taken

- Investigated user sign-in logs
- Reviewed authentication methods
- Reset MFA configuration
- Forced secure re-registration
- Validated successful authentication

---

# 📊 Escalation Decision

Escalation not required.  
Issue resolved within Tier-1 Identity Support scope.

---

# ✅ Incident Outcome

User access restored successfully following MFA remediation.

---

# Ticket Status
**Closed — Resolved**
