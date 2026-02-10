# Ticket-17 — OneDrive Sync Failure

## Objective
Diagnose and resolve a OneDrive sync failure caused by disabled storage service assignment within a licensed Microsoft 365 user account.

---

## Lab Environment

- Platform: Microsoft 365 Admin Center
- Tenant Type: Microsoft 365 E5 Trial
- Admin Portal: https://admin.microsoft.com

---

## Issue Summary

A user reported inability to access or sync files via OneDrive despite having an active Microsoft 365 license.

---

## Steps Performed

### 1) Review License Service Assignment

Verified OneDrive / SharePoint storage service was enabled under the assigned license.

**Screenshot:**

![Service Enabled](images/01-onedrive-enabled-before.png)

---

### 2) Simulate Sync Failure

Disabled SharePoint (OneDrive backend) service to reproduce the issue.

**Screenshot:**

![Service Disabled](images/02-onedrive-service-disabled.png)

---

### 3) Verify Service Impact

Attempted to access OneDrive settings and observed storage provisioning unavailable.

**Screenshot:**

![Impact Observed](images/03-onedrive-service-impact.png)

---

### 4) Restore Storage Service

Re-enabled SharePoint storage service.

**Screenshot:**

![Service Restored](images/04-onedrive-service-reenabled.png)

---

### 5) Validate Restoration

Confirmed service assignment restored successfully within license configuration.

**Screenshot:**

![Restoration Confirmed](images/05-storage-service-restored.png)

---

## Validation

- Storage backend service verified
- Sync failure simulated
- Service restored successfully
- Access configuration validated

---

## Outcome

OneDrive sync functionality was restored by re-enabling the SharePoint storage service within the assigned Microsoft 365 license.
