# Ticket-01 — VPN Connection Failure (Ticketing Workflow Simulation)

## Ticket Information
- Ticket ID: INC-2001
- Ticket Type: Incident
- Reported By: testuser1
- Department: Finance
- Environment: Windows 11 (VM/Lab)
- Date Logged: 12 Feb 2026

---

## Issue Summary
User reported being unable to connect to the corporate VPN (Corp-VPN). Connection attempts returned a VPN connection failure error.

---

## Classification
- Category: Network
- Subcategory: VPN Connectivity

---

## Priority, Severity, SLA
- Priority: P2 (High)
- Severity: Single user unable to access corporate resources remotely
- SLA Target:
  - Response: 1 hour
  - Resolution: 4 hours

---

## Assignment Group
- Assigned To: Tier 1 Service Desk
- Escalation Group (if required): Network Infrastructure Team

---

## Simulation Notes (Lab Context)
This lab simulates a real-world VPN incident using a Windows built-in VPN profile with a non-existent VPN server (`vpn.corp.local`).  
Success criteria for this simulation is restoring correct client network configuration (DNS/connectivity) and documenting the incident lifecycle (priority, SLA, escalation decision, resolution notes).

---

## Step-by-Step Troubleshooting (with Evidence)

### 1) Verified VPN Settings & Profile
Opened Windows VPN settings and confirmed VPN profile configuration.

![VPN Settings](images/01-vpn-settings.png)  
![VPN Profile Created](images/02-vpn-profile-created.png)

---

### 2) Reproduced the Issue (User Impact Confirmed)
Attempted VPN connection as the affected user and captured the failure message.

![VPN Connection Failed](images/03-vpn-connection-failed.png)

---

### 3) Verified Internet Connectivity
Confirmed the device had internet access (rules out basic connectivity outage).

![Ping Success](images/04-ping-8.8.8.8-success.png)

---

### 4) Performed DNS Resolution Test
Tested DNS resolution for the VPN hostname (`vpn.corp.local`). Resolution failed as expected in the lab environment.

![nslookup Failed](images/05-nslookup-vpn-corp-local-failed.png)

---

### 5) Simulated a Common Corporate Root Cause (DNS Misconfiguration)
To simulate a realistic enterprise issue, DNS was intentionally set to an invalid server (`10.10.10.10`) and re-tested.

![Invalid DNS Config](images/06-dns-set-invalid-10.10.10.10.png)  
![nslookup Failed with Invalid DNS](images/07-nslookup-failed-invalid-dns.png)

---

### 6) Resolution — Restored Correct DNS Configuration
DNS settings were restored to automatic (valid resolver), returning the device to a correct network state.

![DNS Set to Automatic](images/08-dns-set-automatic.png)

---

## Root Cause
VPN connectivity was impacted by an invalid DNS configuration (simulated). Incorrect DNS prevents hostname resolution and can block VPN connectivity/authentication workflows.

---

## Resolution
- Restored DNS configuration to automatic (valid DNS resolver)
- Verified internet connectivity and DNS behavior
- Retried VPN connection attempt (lab server remains non-existent by design)

---

## Escalation Decision
Escalation was **not required** because the endpoint DNS misconfiguration was corrected at Tier 1.  
(If this was a production environment with a valid VPN gateway and issue persisted, escalation would be made to the Network Infrastructure Team.)

---

## Ticket Status
**Closed — Resolved (within SLA)**
