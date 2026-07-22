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

# Rename the Windows Server 2025 Computer

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