# Ticket-18 — Printer Not Printing (Print Spooler Failure)

## Objective
Diagnose and resolve a printing failure caused by the Print Spooler service being stopped on a Windows client workstation.

---

## Lab Environment

- Operating System: Windows 10 / Windows 11
- Device Type: Client Workstation (VM)
- Printer Type: Microsoft Print to PDF (Virtual Printer)
- User Context: Standard Local User
- Admin Context: Local Administrator
- Tools Used:
  - Services.msc
  - Devices and Printers
  - Print Queue Console

---

## Issue Summary

A standard user reported that print jobs were not processing and documents failed to print despite selecting a valid printer.

---

## User Impact Validation

### 1) Verify Printer Installation

Opened:  
Control Panel → Devices and Printers

Confirmed Microsoft Print to PDF was installed.

**Screenshot:**  
![Printer Installed](images/01-printer-installed.png)

---

### 2) Attempt Test Print

User attempted to print a document.

Observed print job did not process.

**Screenshot:**  
![Print Job Stuck](images/02-print-job-stuck.png)

---

### 3) Review Print Queue

Opened printer queue and confirmed job was stuck/pending.

**Screenshot:**  
![Queue Pending](images/03-print-queue-pending.png)

---

## Administrative Troubleshooting

### 4) Identify Service Failure

Accessed Services console via:

services.msc

Observed Print Spooler service was stopped.

**Screenshot:**  
![Spooler Stopped](images/04-spooler-stopped.png)

---

### 5) Restore Print Service

Restarted Print Spooler service.

**Screenshot:**  
![Spooler Started](images/05-spooler-started.png)

---

### 6) Clear Stuck Jobs

Removed pending jobs from the print queue.

**Screenshot:**  
![Queue Cleared](images/06-queue-cleared.png)

---

## Resolution Validation

### 7) Confirm Printing Functionality

User performed a new test print successfully.

**Screenshot:**  
![Test Print Success](images/07-test-print-success.png)

---

## Root Cause

The Print Spooler service was stopped, preventing print jobs from being processed.

---

## Resolution

Restarted the Print Spooler service and cleared stuck print jobs to restore printing functionality.

---

## Outcome

Printing services were restored, and the user was able to process print jobs successfully.

---

## Key Learning

This lab demonstrates:

- User vs Administrator troubleshooting roles
- Dependency of printing on the Spooler service
- Queue management procedures
- Windows service recovery workflow
- Real-world helpdesk escalation model
