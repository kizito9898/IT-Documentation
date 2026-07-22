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
