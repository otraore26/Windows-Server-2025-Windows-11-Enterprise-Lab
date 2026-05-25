# 🖥️ Windows Server 2025 Active Directory Home Lab – Domain Join & DNS Configuration

![Status](https://img.shields.io/badge/status-completed-success)
![Platform](https://img.shields.io/badge/platform-Windows%20Server%202025-blue)
![Client](https://img.shields.io/badge/client-Windows%2011-blueviolet)
![Domain](https://img.shields.io/badge/domain-tms.com-orange)
![Virtualization](https://img.shields.io/badge/virtualization-VirtualBox-lightgrey)
![Focus](https://img.shields.io/badge/focus-Active%20Directory%20%26%20DNS-critical)

---

# 📌 Overview

This cybersecurity home lab project demonstrates the deployment and configuration of a small enterprise Active Directory environment using **Windows Server 2025** and a **Windows 11 client machine** inside Oracle VirtualBox.

The goal of this project was to simulate a real-world enterprise environment where a Windows endpoint must communicate with an Active Directory Domain Controller through properly configured DNS services before successfully joining the domain.

The project focused heavily on:

- DNS configuration
- Active Directory domain services
- Windows domain joining
- User account management
- Enterprise identity infrastructure
- Client/server communication
- Basic Windows network troubleshooting

This lab helped reinforce how critical DNS is within Active Directory environments and demonstrated the process of integrating a workstation into a centralized identity management infrastructure.

---

# 🧰 Environment Setup

| Tool / Technology | Purpose |
|-------------------|---------|
| Windows Server 2025 | Active Directory Domain Controller |
| Windows 11 Enterprise | Domain-joined client workstation |
| Active Directory Domain Services (AD DS) | Centralized identity and authentication |
| DNS Server | Domain name resolution |
| Oracle VirtualBox | Virtualization platform |
| PowerShell | Administrative management |
| IPv4 Networking | Internal lab communication |
| Local User & Group Management | Access management |
| Active Directory Users and Computers | User provisioning |


---

# 🏢 Company / Lab Structure

## Simulated Organization

| Department | Purpose |
|------------|---------|
| IT Administration | Domain management and infrastructure |
| End Users | Standard employee workstation access |
| Active Directory Services | Identity and authentication |
| DNS Services | Internal hostname resolution |

---
##
## 🏗️ Lab Architecture


                    ┌─────────────────────────┐
                    │ Windows Server 2025     │
                    │ Domain Controller       │
                    │ DNS Server              │
                    │ Domain: tms.com         │
                    │ IP: 10.0.0.129          │
                    └──────────┬──────────────┘
                               │
                    Internal Virtual Network
                               │
                    ┌──────────┴──────────────┐
                    │ Windows 11 Enterprise   │
                    │ Domain Joined Client    │
                    │ DNS → 10.0.0.129        │
                    └─────────────────────────┘


---

## 🌐 Configure DNS on Windows 11

Step 1 — Open Network & Internet Settings

Navigate to:

Settings → Network & Internet → Ethernet

This step allows the Windows 11 client workstation to access Ethernet configuration settings before joining the Active Directory domain.
