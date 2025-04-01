# IT Glue Documentation

## Introduction

### What is IT Glue?
IT Glue is a cloud-based IT documentation platform designed for Managed Service Providers (MSPs) and IT teams. It provides a centralized repository for storing and managing IT documentation, enabling teams to access critical information efficiently.

### Importance of IT Glue
- **Efficiency**: Reduces troubleshooting time by providing quick access to documented solutions.
- **Consistency**: Ensures standardized documentation across the IT team.
- **Security**: Protects sensitive IT information with role-based access controls.
- **Accountability**: Tracks updates and changes for better audit control.

### Why Good Documentation Matters in IT Support
- Helps resolve issues faster by referencing past solutions.
- Reduces repetitive tasks by providing clear Standard Operating Procedures (SOPs).
- Enhances collaboration among team members.
- Ensures continuity when staff changes occur.

## IT Glue Structure

### IT Assets (Network, Servers, Applications)
- **Servers** – Active Directory Server, File Server, Remote Desktop Server
- **Network Devices** – Firewall, Switches, VPN
- **Applications** – Microsoft 365, Intune, ConnectWise

### Standard Operating Procedures (SOPs)
- Password Reset
- Adding a New User in Microsoft 365
- VPN Setup Guide
- Printer Troubleshooting
- File Sharing Configuration
- Updating IT Glue Documentation

### Common Fixes & Workarounds
- Outlook Not Syncing
- Account Locked in Active Directory
- Printer Offline Fix
- VPN Connection Issues
- Microsoft Intune Device Enrollment Issues

## Server Documentation - Active Directory Server

### Server Details
- **Name:** AD-DC01  
- **IP Address:** 192.168.1.10  
- **Location:** Main Office  
- **Operating System:** Windows Server 2019  
- **Roles:** Domain Controller, DNS  

### Credentials (Stored in IT Glue)
- **Administrator Account:** admin@company.com  
- **Recovery Account:** recovery@company.com  

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

### Step 3: Update IT Glue Documentation
- Add a note: *"Password reset for [User] on [Date]."*

## Microsoft Intune Documentation

### Device Enrollment Guide
#### Enrolling a Windows Device
1. Open **Settings > Accounts > Access work or school**.
2. Click **Connect** and enter Microsoft 365 credentials.
3. Follow the prompts to complete the enrollment.
4. Verify the device in **Microsoft Endpoint Manager**.

#### Troubleshooting Enrollment Issues
- Ensure the device is **not already enrolled**.
- Check for **compliance policies** blocking the enrollment.
- Restart the device and retry the enrollment.

## Microsoft 365 Documentation

### Adding a New User
1. Open **Microsoft 365 Admin Center**.
2. Navigate to **Users > Active Users**.
3. Click **Add a user**, enter details, and assign a license.
4. Send credentials to the user securely.

### Outlook Not Syncing
- Restart **Outlook** and check for pending updates.
- Clear the **Outlook cache**.
- Run **Outlook /safe** mode to check for add-in conflicts.

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

## Updating IT Glue Documentation

### How to Update an Existing Entry
1. Search for the existing document in **IT Glue**.
2. Click **Edit**, make necessary changes, and add the **update date**.
3. Save and review the update for accuracy.

### How to Create a New Documentation Entry
1. Click **New Document** in IT Glue.
2. Select the appropriate **category (Server, Network, SOP, etc.)**.
3. Add **relevant details, screenshots, and steps**.
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

## Next Steps
- **Create these documentation files in Obsidian**.
- **Organize them into categories** (IT Assets, SOPs, Troubleshooting).
- **Push them to GitHub Pages**.
- **Use this as your MSP IT knowledge base in interviews**.

For further assistance on setting up **MkDocs Material** for publishing on GitHub, feel free to ask.
