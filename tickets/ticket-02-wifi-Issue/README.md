# Ticket 02 – No Network Connectivity on User System

## Issue Summary
A user reported that their system was unable to access the internet due to network connectivity failure.

---

## Environment
- Operating System: Windows 10 / 11
- Connection Type: Ethernet / Wired Network
- Network Environment: Local workstation

---

## User Problem
The user stated that they could not browse the internet or access any online resources from their system.

---

## Questions Asked
To diagnose the issue, the following questions were asked:

- Is the network cable or connection active?
- Are other systems affected?
- When did the issue start?
- Were there any recent system or network changes?

---

## Checks Performed
The following troubleshooting checks were conducted:

- Verified network adapter status
- Checked IP address assignment using Command Prompt (`ipconfig`)
- Tested connectivity using a web browser
- Confirmed network availability on the system

---

## Root Cause
The network adapter was disabled, preventing the system from obtaining network connectivity.

---

## Resolution Steps

1. Opened **Network & Internet Settings**
2. Navigated to **Network Adapter Options**
3. Identified the disabled Ethernet adapter
4. Re-enabled the network adapter
5. Checked IP configuration using `ipconfig`
6. Tested internet connectivity via web browser

---

## Evidence

### Disabled Network Adapter
![Disabled Adapter](images/disabled_adapter.png)

### Adapter Enabled
![Enabled Adapter](images/enabled_adapter.png)

### Successful Internet Connectivity
![Internet Working](images/confirmation.png)

---

## Result
Network connectivity was successfully restored, and the user was able to access the internet normally.

---

## Prevention / Best Practices

- Ensure network adapters are enabled before escalating issues
- Educate users on checking basic network settings
- Verify physical and virtual network connections
- Restart network adapters if connectivity fails

---

## Tools Used

- Windows Network & Internet Settings
- Network Adapter Configuration
- Command Prompt (`ipconfig`)
- Web Browser
