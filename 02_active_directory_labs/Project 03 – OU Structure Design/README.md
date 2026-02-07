# Project 03 – OU Structure Design (Active Directory)

## Project Summary

This project focused on designing and implementing a structured Organizational Unit (OU) hierarchy within Active Directory to logically organize users by department and prepare the environment for Group Policy deployment and administrative delegation.

---

## Environment

* Operating System: Windows Server 2022
* Hypervisor: VirtualBox
* Domain: landonhotel.local
* Domain Controller: DC-1
* Tool Used: Active Directory Users and Computers (ADUC)

---

## Objective

To simulate enterprise directory structuring by creating departmental Organizational Units and organizing domain users according to business functions.

---

## Lab Tasks Completed

### 1) Open ADUC and Verify Domain Structure

Opened Active Directory Users and Computers and verified the domain environment.

![Domain Structure](images/1-domain-structure.png)

---

### 2) Create Department Organizational Units

Created the following OUs at the domain root level:

* IT
* HR
* Finance
* Sales

These OUs provide logical separation for administration and future policy targeting.

![OU Creation](images/2-ou-created.png)

---

### 3) Organize Users into Department OUs

Moved previously created users from the **Corp-Users** OU into their respective departments:

* John.IT → IT
* Sara.HR → HR
* Mike.Finance → Finance

This reflects enterprise identity organization practices.

![Users Organized](images/3-users-moved.png)

---

## Validation Check

Validated the final OU hierarchy by expanding the domain tree and confirming users were correctly placed in their respective departments.

![Final OU Structure](images/4-final-ou-structure.png)

---

## Result

A structured OU hierarchy was successfully implemented, enabling improved directory organization, simplified administration, and readiness for department-based Group Policy deployment.

---

## Skills Demonstrated

* Organizational Unit design
* Directory structuring
* Identity organization
* Administrative hierarchy planning
* Enterprise Active Directory management
