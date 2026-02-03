# Active Directory & Group Policy Home Lab

## Overview
This project is a hands-on **Windows Server Active Directory lab** built to simulate a real on-prem IT environment.  
The lab focuses on deploying a domain controller, configuring DNS, joining clients to a domain, and managing users and computers using Group Policy.

This project was intentionally built without shortcuts to better understand troubleshooting, misconfigurations, and real-world behavior.

---

## Technologies Used
- Windows Server (AD DS, DNS)
- Windows Client (Domain Join)
- Active Directory Users and Computers (ADUC)
- Group Policy Management Console (GPMC)

---

## Lab Architecture
- **DC01** – Domain Controller running AD DS and DNS  
- **Client01** – Domain-joined Windows workstation  
- Static IP addressing and DNS pointing to DC01

*(See diagram in /diagrams)*

---

## Objectives
- Deploy and configure Active Directory Domain Services
- Configure DNS for domain authentication
- Join a Windows client to the domain
- Create users and organizational units (OUs)
- Apply Group Policy Objects (GPOs)
- Troubleshoot policy application issues

---

## Implementation Steps

### 1. Domain Controller Setup
- Installed Windows Server
- Promoted server to Domain Controller
- Installed AD DS and DNS roles

### 2. DNS & Networking
- Configured static IP on DC01
- Set DNS to point to domain controller
- Verified name resolution from client

### 3. Domain Join
- Joined Windows client to the domain
- Verified authentication and connectivity

### 4. Active Directory Management
- Created domain users
- Created Organizational Units (OUs)
- Moved computer objects into appropriate OUs

### 5. Group Policy Configuration
- Created GPOs (ex: restrict Control Panel access)
- Linked GPOs to correct OUs
- Verified application using `gpresult` and RSOP

---

## Troubleshooting & Lessons Learned
- Computers joined the domain but landed in the **default Computers container**
- GPOs existed but did not apply until properly **linked and enforced**
- DNS configuration details directly affected authentication and policy behavior
- Learned to verify results instead of assuming success

See detailed notes in `/notes/troubleshooting-notes.md`.

---

## Screenshots
Screenshots documenting setup, errors, and verification steps are available in the `/screenshots` directory.

---

## Future Improvements
- Add additional users and security groups
- Implement password and account lockout policies
- Expand lab into a hybrid on-prem / Azure AD scenario

---

## Why This Matters
This lab demonstrates practical experience with:
- Active Directory administration
- Group Policy management
- Troubleshooting real configuration issues
- Foundational skills used in IT Support, SysAdmin, and Data Center roles

