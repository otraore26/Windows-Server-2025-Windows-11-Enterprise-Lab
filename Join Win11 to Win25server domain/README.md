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


<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/97aef22aa1bcc24e1095c5327d2cd063ec6ae89f/Join%20Win11%20to%20Win25server%20domain/Step%201%20go%20to%20the%20setting%20then%20go%20to%20Network%20and%20Internet%20and%20then%20click%20on%20ethernet%20.png">

---
## Step 2 — Open Ethernet Properties

Inside the Ethernet configuration page, review the active network profile and scroll down to locate the DNS server assignment section.

The workstation must communicate directly with the Domain Controller DNS service for successful domain authentication.


<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/97aef22aa1bcc24e1095c5327d2cd063ec6ae89f/Join%20Win11%20to%20Win25server%20domain/Step%202%20Select%20Public%20Recommend%20scrow%20down%20to%20edit%20DNS%20ssrver%20assigmnent.png">

---

### Step 3 — Configure DNS Settings Manually

Select:

Edit DNS Settings → Manual

Enable IPv4 configuration to manually assign the Domain Controller DNS server.



<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/97aef22aa1bcc24e1095c5327d2cd063ec6ae89f/Join%20Win11%20to%20Win25server%20domain/Step%203select%20manual%20and%20set%20IPV4.png">

### Step 4 — Configure Preferred DNS Server

Set the Preferred DNS Server to the IP address of the Windows Server 2025 Domain Controller:

10.0.0.xxx

This configuration allows the Windows 11 client to locate the Active Directory services and authenticate against the domain.

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/97aef22aa1bcc24e1095c5327d2cd063ec6ae89f/Join%20Win11%20to%20Win25server%20domain/Step%204%20%20Put%20IPV4%20on%20and%20fill%20out%20the%20preferred%20DNS%20with%20your%20active%20directory%20IPV4.png">

---

 ### Step 5 — Save DNS Configuration

After entering the DNS server information, click:

Save

to apply the network configuration changes.

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/97aef22aa1bcc24e1095c5327d2cd063ec6ae89f/Join%20Win11%20to%20Win25server%20domain/Step%205%20set%20up%20and%20save%20it%20.png">

---
### Step 6 — Verify DNS Configuration

Verify that:

DNS Assignment = Manual
IPv4 DNS Server = 10.0.0.129

This confirms that the workstation is using the Domain Controller as its primary DNS server.

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/5e46e3dbcd63a49596f75ea9270a4f4ea7e19e88/Join%20Win11%20to%20Win25server%20domain/Step%206.png">

---

### Step 7 — Validate Network Connectivity

Open:

Control Panel → Network and Sharing Center

Verify successful IPv4 connectivity and Ethernet communication between the client workstation and the server infrastructure.

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/5e46e3dbcd63a49596f75ea9270a4f4ea7e19e88/Join%20Win11%20to%20Win25server%20domain/Step%207%20go%20to%20Panel%20then%20go%20to%20the%20network%20and%20sharing%20.png">

---

### 🏢 Join Windows 11 to the Active Directory Domain
Step 8 — Configure Domain Membership

Navigate to:

System → About → Domain or Workgroup

Select:

Change → Domain

Enter the enterprise domain name:

tms.com

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/5e46e3dbcd63a49596f75ea9270a4f4ea7e19e88/Join%20Win11%20to%20Win25server%20domain/Step%208%20go%20to%20the%20System%20and%20Then%20scrow%20down%20and%20select%20domain%20names%20And%20choose%20computer%20name%20and%20domain%20.png">

---
### Step 9 — Authenticate Using Domain Administrator Credentials

Provide Domain Administrator credentials with permission to join systems to the Active Directory environment.

This operation securely authenticates the Windows 11 workstation against the Domain Controller.

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/5e46e3dbcd63a49596f75ea9270a4f4ea7e19e88/Join%20Win11%20to%20Win25server%20domain/Step%209%20put%20admin%20credential%20%20And%20password.png">

---

### Step 10 — Successful Domain Join

Windows 11 successfully joined the:

tms.com

Active Directory domain.

A system reboot is required to finalize domain enrollment and apply enterprise policies.

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/5e46e3dbcd63a49596f75ea9270a4f4ea7e19e88/Join%20Win11%20to%20Win25server%20domain/Step%2010%20Win%2011%20join%20the%20Win25%20successfully.png">

---

### 👥 Create Active Directory Users
Step 11 — Create Enterprise User Accounts

Using:

Active Directory Users and Computers

new enterprise user accounts were provisioned inside the domain environment.

The following user attributes were configured:

First Name
Last Name
User Logon Name (UPN)
Pre-Windows 2000 Username
Password Policies





