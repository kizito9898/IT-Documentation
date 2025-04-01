
# IT Glue Documentation

## Introduction

### What is IT Glue?
IT Glue is a cloud-based IT documentation platform designed for Managed Service Providers (MSPs) and IT teams. It provides a centralized repository for storing and managing IT documentation, enabling teams to access critical information efficiently.

### Importance of IT Glue
- **Efficiency**: Reduces troubleshooting time by providing quick access to documented solutions.
- **Consistency**: Ensures standardized documentation across the IT team.
- **Accountability**: Tracks updates and changes for better audit control.

### Why Good Documentation Matters in IT Support
- Helps resolve issues faster by referencing past solutions.
- Reduces repetitive tasks by providing clear Standard Operating Procedures (SOPs).
- Enhances collaboration among team members.
- Ensures continuity when staff changes occur.

### Limitations of This Documentation
Due to the lack of access to an IT Glue trial version, this documentation is based on extensive research from industry resources, including YouTube tutorials, official documentation, and IT support knowledge bases. While screenshots cannot be included, the structured guidelines and mock data closely replicate real-world IT documentation practices used in MSP environments.

## IT Glue Structure
IT Glue is structured to provide a logical and organized way to store and retrieve IT documentation. Below are the key components:

### 1. IT Assets
This section includes documentation on all key IT assets managed by the MSP or IT team. It is categorized into three primary areas:

#### **Network Devices**
- Firewalls (e.g., Cisco ASA, pfSense, Meraki)
- Switches (e.g., Cisco, HP, Unifi)
- Routers
- VPN appliances
- Wireless access points

#### **Servers**
- Active Directory Domain Controllers
- File Servers
- Remote Desktop Servers
- Microsoft Exchange Servers
- Virtualization Hosts (Hyper-V, VMware ESXi)

#### **Applications**
- Microsoft 365 (Exchange, SharePoint, Teams)
- Microsoft Intune (Device Management, Policies)
- Ticketing Systems (ConnectWise, Zendesk, Freshdesk)
- Backup Solutions (Veeam, Acronis, Datto)
- Security Software (CrowdStrike, SentinelOne)

Each IT asset entry in IT Glue contains:
- **Name** (e.g., AD-DC01)
- **IP Address** (e.g., 192.168.1.10)
- **Location** (e.g., Data Center, Remote Office)
- **Role/Purpose** (e.g., Domain Controller, VPN Gateway)
- **Configuration Details** (e.g., OS Version, Installed Services)
- **Credentials** (if applicable, securely stored)
- **Related Documentation** (linked troubleshooting guides and SOPs)

### 2. Standard Operating Procedures (SOPs)
SOPs provide step-by-step instructions for common IT support issues. These ensure consistency and efficiency when resolving recurring issues.

#### **Examples of SOPs in IT Glue:**
- **Password Reset** (Active Directory, Microsoft 365)
- **New User Onboarding** (Creating accounts, setting permissions)
- **VPN Setup & Troubleshooting**
- **Printer Installation & Troubleshooting**
- **Software Deployment via Intune or PDQ Deploy**
- **Updating IT Glue Documentation**

Each SOP entry in IT Glue includes:
- **Purpose** (Why the procedure exists)
- **Prerequisites** (Any necessary information before starting)
- **Step-by-Step Guide** (Clear instructions with expected outcomes)
- **Troubleshooting Tips** (Common errors and resolutions)
- **Update Log** (Record of changes to the procedure)

### 3. Common Fixes & Workarounds
This section in IT Glue stores documentation for resolving frequently encountered issues. 

#### **Examples of Common Fixes:**
- Outlook Not Syncing
- Account Locked in Active Directory
- Printer Offline Fix
- VPN Connection Issues
- Microsoft Intune Device Enrollment Issues

Each troubleshooting entry contains:
- **Symptoms** (What issue users report)
- **Possible Causes** (What might be wrong)
- **Step-by-Step Fix** (How to resolve it)
- **Related Documentation** (Links to SOPs, IT assets)

## Server Documentation - Active Directory Server

### Server Details
- **Name:** AD-DC01  
- **IP Address:** 192.168.1.10  
- **Location:** Main Office  
- **Operating System:** Windows Server 2022  
- **Roles:** Domain Controller, DNS  

### Credentials (Stored in IT Glue)
- **Administrator Account:** kizitoNjika@onmicrosoft.com 
- **Recovery Account:** recovery@onmicrosoft.com  

### Common Issues & Fixes
#### User Account Locked
1. Open **Active Directory Users & Computers**.
2. Search for the **user account**.
3. Right-click and select **Unlock Account**.
4. Reset the password if needed.

#### Replication Issues
```powershell
repadmin /showrepl
```
If errors appear, check **event logs** and restart **Active Directory Services**.

## Standard Operating Procedure - Password Reset

### When to Use This Guide
- User forgot their password.
- Account is locked due to multiple failed attempts.

### Step 1: Verify User Identity
- Confirm the request via email or phone.
- Check with the **manager** if needed.

### Step 2: Reset Password in Active Directory
1. Open **Active Directory Users & Computers**.
2. Search for the **user account**.
3. Right-click and select **Reset Password**.
4. Enter the new password and confirm.

## File Sharing Configuration

### Configuring a Shared Drive
1. Create a shared folder on the **File Server**.
2. Set permissions using **NTFS & Share Permissions**.
3. Map the drive via **Group Policy Preferences**.
4. Test access from multiple user accounts.

## Network Devices Documentation

| Device Name | Type     | IP Address  | Location      | Notes                   |
| ----------- | -------- | ----------- | ------------- | ----------------------- |
| Firewall-01 | Firewall | 192.168.1.1 | Data Center   | Main perimeter firewall |
| Switch-01   | Switch   | 192.168.1.2 | Office Floor  | 48-Port Gigabit Switch  |
| VPN-01      | VPN      | 192.168.1.3 | Remote Access | VPN for external users  |

### Troubleshooting VPN Issues
- If VPN is down, check **firewall logs** and ensure **IKE/IPSec services** are running.

## Printer Troubleshooting Guide

### Common Printer Issues
- Printer is offline
- Print jobs stuck in queue
- Cannot connect to the network printer

### Fixing a Printer Offline Issue
1. Restart the **print spooler service**.
2. Ensure the printer is **set as the default**.
3. Reinstall the printer driver.

### Step 3: Update IT Glue Documentation
- Add a note: *"Password reset for [User] on [Date]."*

## Updating IT Glue Documentation

### How to Update an Existing Entry
1. Search for the existing document in **IT Glue**.
2. Click **Edit**, make necessary changes, and add the **update date**.
3. Save and review the update for accuracy.

### How to Create a New Documentation Entry
1. Click **New Document** in IT Glue.
2. Select the appropriate **category (Server, Network, SOP, etc.)**.
3. Add **relevant details, steps, and troubleshooting tips**.
4. Save and **tag for easy searching**.

## How IT Glue is Used in an MSP Workflow

### Step 1: Review Ticket in Zendesk or ConnectWise
- User reports: *"Cannot log in to VPN."*
- Check **past issues** in IT Glue.

### Step 2: Search IT Glue for Documentation
- Look up **VPN-01** in Network Devices.
- Find **troubleshooting steps**.

### Step 3: Remote Into the Device
- Use **ConnectWise Control** to access the user’s PC.
- Check **VPN client logs** for error codes.

### Step 4: Apply Fix and Update IT Glue
- If the issue is resolved, document the fix in IT Glue.
  *Example: "Resolved VPN login issue for UserX by resetting VPN profile."*
