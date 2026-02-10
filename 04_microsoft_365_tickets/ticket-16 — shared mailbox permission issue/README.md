# Ticket-16 — Shared Mailbox Permission Issue

## Objective
Diagnose and resolve a shared mailbox access issue caused by missing delegation permissions within Exchange Online.

---

## Lab Environment

- Platform: Exchange Admin Center
- Tenant Type: Microsoft 365 E5 Trial
- Admin Portal: https://admin.microsoft.com

---

## Issue Summary

A user reported being unable to access the HR department shared mailbox required for team communications.

---

## Steps Performed

### 1) Access Exchange Admin Center

Opened Exchange Admin Center from Microsoft 365 Admin Portal.

**Screenshot:**

![Exchange Dashboard](images/01-exchange-admin-center-dashboard.png)

---

### 2) Review Mailbox Inventory

Navigated to the mailbox directory to review existing mailboxes.

**Screenshot:**

![Mailbox Inventory](images/02-mailbox-inventory-before-shared.png)

---

### 3) Create Shared Mailbox

Provisioned HR department shared mailbox.

**Screenshot:**

![Mailbox Created](images/03-shared-mailbox-created.png)

---

### 4) Verify Permission State

Observed no delegation permissions assigned to the shared mailbox.

**Screenshot:**

![No Permissions](images/04-shared-mailbox-no-permissions.png)

---

### 5) Assign Mailbox Access

Granted Test User1 delegation permissions.

**Screenshot:**

![Permissions Assigned](images/05-permission-assigned.png)

---

### 6) Validate Access Restoration

Confirmed user delegation successfully applied.

**Screenshot:**

![Access Restored](images/06-access-restored-confirmation.png)

---

## Validation

- Shared mailbox provisioned
- Permission gap identified
- Delegation configured
- Access restored

---

## Outcome

User access to the shared mailbox was restored through proper delegation assignment within Exchange Online.
