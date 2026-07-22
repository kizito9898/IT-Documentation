# Windows Server 2025 Lab Documentation

## Overview

Windows Server 2025 is Microsoft's latest Long-Term Servicing Channel (LTSC) operating system built on the Windows 11 codebase. It is designed for modern infrastructure, offering deeper cloud integration, significantly enhanced storage performance, and updated security baselines compared to its predecessor, Windows Server 2022.

---
# Getting Started

- Download the **Windows Server 2025 Evaluation ISO** from the Microsoft Evaluation Center.

- After downloading the ISO file, launch **VMware Workstation Pro**.
## VMware Baseline Configuration

- **vCPUs:** 2
- **Memory:** 4 GB - 8 GB RAM
- **Virtual Disk:** 60 GB NVMe
## Creating the Virtual Machine

- Navigate to **File** → **Create New Virtual Machine**.

- Click **Next**.

- Select **I will install the operating system later**, then click **Next**.

- Select **Microsoft Windows Server 2025** as the operating system.

- Allocate the virtual disk size (**Recommended: 60 GB**).

- Click **Customize Hardware**.

- Locate the downloaded Windows Server 2025 ISO:
  - Select **New CD/DVD (SATA)**.
  - Choose **Use ISO Image File**.
  - Browse to the downloaded Windows Server 2025 ISO.
  - Click **Close**, then **Finish**.
## Powering On the Virtual Machine

- Click **Power On This Virtual Machine**.

- Click inside the virtual machine window.

- Press the **Spacebar** when prompted to boot from the Windows Server 2025 ISO.

- Select the preferred language settings.
- Select **Keyboard: US**.
- Click **Next**.
- Select the Windows Server edition (**Desktop Experience**).
- Click **Next**.
- Accept the Microsoft License Terms.
- Click **Install**.

- After the installation completes, create and configure the **Administrator** password.

- Windows Server 2025 is now fully installed. The Evaluation ISO license is valid for **180 days**.

---
## Installing VMware Tools

For a better performance and user experience, install VMware Tools.

- Open **File Explorer**.
- Navigate to the **VMware Tools** virtual CD.
- Run **Setup64.exe**.
- Follow the VMware Tools installation wizard.
- Complete the installation.
- Restart the virtual machine.
---
# Rename the Windows Server 2025

Renaming the server provides a consistent naming convention before configuring Active Directory roles and features. It also makes the server easier to identify instead of using the default Windows Server computer name.
### Steps

- Open **File Explorer**.
- Right-click **This PC**.
- Select **Properties**.
- Click **Advanced System Settings**.
- Open the **Computer Name** tab.
- Click **Change**.
- Enter a new computer name of your choice.
- Click **OK**.
- Restart the server when prompted for the changes to take effect.
---
# Installing Active Directory Users and Computers (AD DS)

### Opening the Add Roles and Features Wizard

- Open **Server Manager**.
- In the upper-right corner, click **Manage**.
- Select **Add Roles and Features**.
- The **Add Roles and Features Wizard** opens.
- Under **Installation Type**, select:

  - **Role-based or feature-based installation**.
- Select the target server (the server appears with its IP address).
- Click **Next**.
- Under **Server Roles**, select:

  - **Active Directory Domain Services (AD DS)**

- Click **Next** through the remaining pages.
- On the **Features** page, accept the required features.

This installs the following Active Directory components:

- Active Directory Domain Services
- Group Policy Management
- AD DS Role Administration Tools
- Required management features
- Click **Install**.
---
## Promoting the Server to a Domain Controller

After the installation is complete:

- Click **Promote this server to a domain controller**.

### Deployment Configuration

- Select **Add a new forest**.
- Enter the root domain name.

Example:

```text
Njikason.local
```

- Click **Next**.
### Domain Controller Options

- Enter the **Directory Services Restore Mode (DSRM)** password.
- Ignore the DNS delegation warning for now.
- Click **Next**.
### Additional Options

- Leave the default settings.
- Click **Next**.
### Prerequisites Check

- Wait for the prerequisite checks to complete successfully.
- Click **Install**.

After the installation finishes:

- The server automatically restarts.
- The server is now configured as a **Domain Controller**.
---
# Opening Active Directory Users and Computers

### Method 1

- Open the **Start Menu**.
- Select **Windows Tools**.
- Open **Active Directory Users and Computers**.
### Method 2

- Open **Server Manager**.
- Click **Tools**.
- Select **Active Directory Users and Computers**.

The Active Directory management console opens.

---
# Joining Windows 11 to an Active Directory Domain

Joining a Windows 11 computer to Active Directory allows administrators to centrally manage users, computers, and security policies across the organization's network.

Some common administrative tasks include:

- Creating and managing user accounts.
- Managing computer objects.
- Resetting user passwords.
- Unlocking locked user accounts.
- Applying Group Policy settings.
- Controlling user access to company resources.

Joining a computer to the domain gives IT administrators centralized control over devices while allowing users to securely access company network resources and services.