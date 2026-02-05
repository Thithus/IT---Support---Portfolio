# Ticket 04 – Installed Application Not Opening

## Issue Summary
A user reported that an installed application failed to open when launched from the desktop shortcut.

---

## Environment
- Operating System: Windows 10 / 11
- Application Type: Desktop Software
- Launch Method: Desktop Shortcut

---

## User Problem
The installed application did not open when the user attempted to launch it. No functionality was accessible through the shortcut.

---

## Questions Asked
To gather more details, the following questions were asked:

- Has the application worked previously?
- When did the issue first occur?
- Were there any recent system or application updates installed?
- Is any error message displayed when launching the application?

---

## Checks Performed
The following troubleshooting checks were conducted:

- Verified application installation status
- Checked Task Manager for application process activity
- Reviewed compatibility settings
- Inspected application security and permission settings

---

## Root Cause
Incorrect application configuration and permission settings prevented the software from launching correctly.

---

## Resolution Steps

1. Opened **Task Manager** to monitor application behavior  
2. Verified whether the application process was running  
3. Accessed **Application Properties**  
4. Reviewed compatibility configuration  
5. Corrected incompatible settings and permissions  
6. Relaunched the application to test functionality  

---

## Evidence

### Application Properties Review
![App Properties](images/checking.png)

### Task Manager Process Check
![Task Manager Check](images/verification.png)

### Application Launch Successful
![App Working](images/confirmation.png)

---

## Result
The application opened successfully and functioned as expected after correcting configuration and permission settings.

---

## Prevention / Best Practices

- Avoid modifying compatibility settings unnecessarily
- Ensure applications are updated to supported versions
- Install software using standard installation procedures
- Verify application permissions before escalation

---

## Tools Used

- Application Properties
- Task Manager
- Apps & Features
- Web Browser
