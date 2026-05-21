#  Windows-Server-2025-Windows-11-Enterprise-Lab

This IT and cybersecurity home lab project was built to simulate a small enterprise Windows environment using Oracle VirtualBox, Windows Server 2025, and Windows 11 Pro.

## 🏗️ Lab Architecture

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/d616fa5705bf4e811b901e743f2fdd1af102daf1/Windows%20Server%2025%20%26%20Win%2011%20Enterprise%20Lab%20Architecture%201.png">

## 📥 Step 1 | Download Windows ISO Files

Downloaded:
✅ Windows Server 2025 Evaluation ISO
✅ Windows 11 Pro ISO

Source:
Microsoft Evaluation Center

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/445cc667880f57c668475ec1b0109a3539169f55/Windows%20Server%202022/Select%20Windows%20Server%202025%20Download%20.png">



## 🖥️ Step 2 | Create Windows Server 2025 Virtual Machine

Created a new virtual machine in Oracle VirtualBox.

Configuration:

🛠️ Operating System:
Microsoft Windows

🛠️ Version:
Windows 2022 (64 bit)

🛠️ VM Name:
WinServer25

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/a930b6e0e35736c0fc96b2f7d25150acdc5be909/Windows%20Server%202022/Step%202%20Installing%20Winserver%2025%20on%20VM.png">



## ⚙️ Step 3 | Configure Hardware Resources

Allocated system resources for the virtual machine.

Hardware Configuration:

💾 Memory:
5120 MB RAM

🧠 Processors:
4 CPUs

🖥️ EFI Enabled:
Optional depending on setup

This step ensured the virtual machine had enough resources to run enterprise services efficiently.


<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/76a4f944c5b61046062a1fbb48fb8a87a1951c8c/Windows%20Server%202022/Step%203%20Set%20up%20Hardaware.png">



##

## 💽 Step 4 | Configure Virtual Disk

Created and expanded the virtual hard disk.

Disk Configuration:

📦 Disk Type:
VDI (VirtualBox Disk Image)

💾 Disk Size:
100 GB

This provides enough storage for:
✅ Windows Server
✅ Active Directory
✅ Future security tools and labs

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/52c60fd32dfa386d9e2d5c483843d8f67e0690ee/Windows%20Server%202022/Step%204%20Increasing%20the%20virtual%20disk.png">

## 🪟 Step 5 | Install Windows Server 2025

Installed:
Windows Server 2025 Standard Evaluation Desktop Experience

The installation process included:
✅ System setup
✅ Initial configuration
✅ Administrator password creation

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/074c6911b3311a039075dce2b857f5f9a3ff7b69/Windows%20Server%202022/Step%206%20Ready%20to%20install%20on%20the%20VM.png">

## 🖧 Step 6 | Configure Server Manager

After installation, opened Server Manager to begin configuring enterprise services.

Verified:
✅ Local Server
✅ Server Roles
✅ Initial System Health

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/9c19d485498d23007dbd4c1094fb9d71d5f43260/Windows%20Server%202022/Step%207%20Inside%20Win%20server%202025.png"> 


## 🔐 Step 7 | Install Active Directory Domain Services

Installed:
✅ Active Directory Domain Services (AD DS)

Included management tools:
✅ Group Policy Management
✅ AD DS Administrative Center
✅ PowerShell Tools

This prepares the server to become a Domain Controller.

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/9c19d485498d23007dbd4c1094fb9d71d5f43260/Windows%20Server%202022/Step%2011%20Adding%20different%20features%20.png">

##
## 🌐 Step 8 | Configure Domain Controller

Configured:
✅ New Forest
✅ Root Domain
✅ DNS Services

Functional Levels:

Windows Server 2025

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/acf0b487fb5368cafd7a1589b3cd535ba2c9b414/Windows%20Server%202022/Step%2012%20Set%20up%20passworf%20for%20Directory%20Service%20Restore%20Mode.png">

##

## 🔑 Step 9 | Configure DSRM Password

Configured the:
Directory Services Restore Mode (DSRM) password

Purpose:
The DSRM password is used for:
✅ Active Directory recovery
✅ Domain controller maintenance
✅ Disaster recovery operations

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/acf0b487fb5368cafd7a1589b3cd535ba2c9b414/Windows%20Server%202022/Step%2013%20This%20is%20when%20we%20are%20creating%20a%20new%20domain%20forest%20.png">

## 🧠 Step 10 | Configure NetBIOS Name

Configured the NetBIOS domain name for proper domain identification inside the network environment.

Example:
TMS
<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/50ad4ad8fc6762f52924ad29c7299bc5e71861ad/Windows%20Server%202022/Step%20100%20NetBios.png">


# 🖥️ Windows 11 Enterprise Lab Deployment

This project documents the deployment and configuration of a Windows 11 Pro virtual machine inside Oracle VirtualBox as part of my enterprise cybersecurity homelab.

The Windows 11 workstation was later prepared for Active Directory domain integration within the `tms.com` lab environment.

---

# 📌 Objectives

✅ Deploy Windows 11 Pro in VirtualBox  
✅ Configure enterprise workstation settings  
✅ Prepare Windows client for Active Directory  
✅ Simulate enterprise endpoint deployment  
✅ Practice Windows administration and virtualization  

---

# 🧰 Technologies Used

- Oracle VirtualBox
- Windows 11 Pro
- Windows Server 2025
- Active Directory
- DNS
- PowerShell
- Command Prompt

---

# 🌐 Lab Environment

| Component | Details |
|---|---|
| Domain Name | `tms.com` |
| Client Machine | Windows 11 Pro |
| Domain Controller | Windows Server 2025 |
| Virtualization Platform | Oracle VirtualBox |

---

# 📥 Step 1 — Download Windows 11 ISO

Downloaded the official Windows 11 ISO image from Microsoft for x64 devices.

<img width="1000" alt="Step 1" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%201%20Download%20Windows%2011.png">

---

# 🖥️ Step 2 — Create Windows 11 Virtual Machine

Created a new Windows 11 virtual machine inside Oracle VirtualBox and mounted the ISO image.

<img width="1000" alt="Step 2" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%202%20Installing%20WIN11%20On%20Virtualbox.png">

---

# ⚙️ Step 3 — Configure Hardware Resources

Allocated hardware resources for the virtual machine.

Configuration:
- 5 GB RAM
- 4 Virtual CPUs

<img width="1000" alt="Step 3" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%203%20Increase%20the%20Hardware%20.png">

---

# 💽 Step 4 — Configure Virtual Disk

Created and configured an 80 GB virtual disk for the Windows 11 virtual machine.

<img width="1000" alt="Step 4" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%204%20Increasing%20the%20Virtual%20disk.png">

---

# 🚀 Step 5 — Start Windows 11 Installation

Booted the virtual machine and launched the Windows 11 setup process.

<img width="1000" alt="Step 5" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%205%20Win%2011%20running%20on%20VB.png">

---

# 🌍 Step 6 — Configure Keyboard Settings

Selected keyboard layout and regional settings during installation.

<img width="1000" alt="Step 6" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%206%20Selecting%20Keyboard.png">

---

# 🏢 Step 7 — Select Windows 11 Pro Edition

Selected Windows 11 Pro because it includes enterprise features useful for cybersecurity and Active Directory labs.

Features include:
- Domain Join
- Group Policy
- Remote Desktop
- BitLocker

<img width="1000" alt="Step 7" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%207%20Selecting%20Win%2011%20Pro%20since%20it%20includes%20features%20useful%20for%20labs.png">

---

# 💾 Step 8 — Select Installation Disk

Selected the virtual disk where Windows 11 would be installed.

<img width="1000" alt="Step 8" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%208%20Selecting%20location%20to%20install%20WIN11.png">

---

# 🔓 Step 9 — Bypass Microsoft Account Requirement
<img width="1000" alt="Step 8" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%209%20how%20by%20pass%20Win11%20Local%20Setup%20.png">

<img width="1000" alt="Step 8" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%2010%20Win11%20Setup%20Bypass.png">

Used Command Prompt during setup to bypass the Microsoft online account requirement.

Command used:

```cmd
start ms-cxh:localonly

