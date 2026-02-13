# Ticket-03 — Shared Mailbox Access Request (Service Request Workflow)

## Ticket Information
- Ticket ID: SR-3001
- Ticket Type: Service Request
- Requested By: testuser1
- Department: HR
- Environment: Microsoft 365 Tenant
- Date Logged: 13 Feb 2026

---

## Request Summary
User requested access to the HR shared mailbox to assist with departmental communications and reporting tasks.

---

## Classification
- Category: Identity & Access Management
- Subcategory: Mailbox Permissions

---

## Priority & SLA
- Priority: P3 (Standard Service Request)
- SLA Target:
  - Response: 4 hours
  - Fulfillment: 1 business day

---

## Approval Workflow
Manager approval was obtained from the HR Department prior to access provisioning.

---

## Assignment Group
- Assigned To: M365 Service Desk
- Escalation Group: Messaging / Exchange Online Team

---

## Provisioning Steps

### 1) Navigated to Shared Mailboxes
Accessed Microsoft 365 Admin Center → Teams & Groups → Shared Mailboxes.

![Shared Mailboxes](images/01-shared-mailboxes-admin-center.png)

---

### 2) Opened HR Shared Mailbox
Selected the HR shared mailbox for permission assignment.

![HR Mailbox](images/02-hr-mailbox-open.png)

---

### 3) Assigned User Permissions
Added users to the shared mailbox delegation list to grant access permissions.

> Note: Multiple users appear due to prior lab configuration.

![Permission Assignment](images/03-add-member-permission.png)

---

## User Validation

### 4) User Logged into Outlook Web
User accessed mailbox via Outlook Web Access.

![User Outlook Login](images/04-user-outlook-login.png)

---

### 5) Shared Mailbox Visibility Confirmed
HR shared mailbox appeared in the user mailbox folder list, confirming successful permission synchronization.

![Mailbox Visible](images/05-hr-mailbox-visible.png)

---

### 6) Test Email Sent
User successfully sent an email from the HR shared mailbox to validate Send As permissions.

![Test Email](images/06-test-email-sent.png)

---

## Additional Issue Identified During Validation

During testing, mailbox access was initially impacted because the user account was blocked from signing in.

The sign-in block was removed in Microsoft 365 Admin Center, after which mailbox permissions synchronized successfully.

This reflects a realistic identity access troubleshooting scenario.

---

## Fulfillment Outcome
Access successfully provisioned and validated.

---

## Escalation Decision
Escalation not required — request fulfilled within Service Desk scope.

---

## Ticket Status
**Closed — Fulfilled**
