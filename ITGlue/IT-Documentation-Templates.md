# IT Documentation Templates

IT documentation is essential for managing IT assets, troubleshooting issues, and ensuring smooth operations in an MSP or IT support environment. A well-structured documentation system improves efficiency, reduces resolution times, and ensures consistency across IT teams. This document provides structured templates for documenting servers, network devices, Microsoft 365, standard operating procedures (SOPs), and troubleshooting guides.

Effective IT documentation should:
- Be **clear and concise** to help fellow IT workers to find information quickly.
- Follow a **consistent format** for ease of use.
- Be **updated regularly** to ensure accuracy.
![Screenshot](images/screenshot100.jpg)
## **1. Server Documentation**

# Server Name: [SERVER-2022]
## General Information
- **Role:** [Domain Controller / File Server / Application Server]
- **Operating System:** [Windows Server 2022]
- **IP Address:** [192.168.1.X]
- **Location:** [On-Prem / Cloud (Azure, AWS)]
- **Administrator Account:** [Documented in IT Glue / Vault]
- **Last Maintenance Date:** [YYYY-MM-DD]

## Services Running
- **Active Directory / DHCP / DNS**
- **File Sharing / Print Services**
- **Virtualization  / VMware**

## Backup & Recovery
- **Backup Solution:** [Veeam / Azure Backup / Acronis]
- **Retention Policy:** [Daily / Weekly / Monthly]
- **Recovery Procedure:** [Step-by-step guide]

## Monitoring & Alerts
- **Monitoring Tool:** [ SolarWinds / ConnectWise Automate]
- **Alerting Method:** [Email / Ticket Creation]
---
## **2. Network Device Documentation (Router, Switch, Firewall)**

# Device Name: [Meraki-MX68/ Cisco-2960X-01]
## General Information
- **Device Type:** [Firewall / Router / Switch]
- **Model:** [Cisco Meraki MX ]
- **IP Address:** [192.168.1.1]
- **Firmware Version:** [Latest / YYYY-MM-DD]
- **Last Config Change:** [YYYY-MM-DD]
- **Administrator Credentials:** [Stored in IT Glue / Vault]

## VLANs & Subnets
- VLAN 10 - Users (192.168.10.0/24)
- VLAN 20 - Servers (192.168.20.0/24)
- VLAN 30 - VoIP (192.168.30.0/24)
## Security & Firewall Rules
- **Allow RDP:** No
- **Allow VPN:** Yes
- **Geo-IP Blocking:** Enabled for [Country_List]

## Backup & Recovery
- **Configuration Backup Location:** [Cloud / Local Repository]
- **Restoration Procedure:** [Step-by-step guide
---
## **3. Microsoft 365 Documentation**

# Microsoft 365 Tenant: [Njikason.onmicrosoft.com]
## General Information
- **Admin Portal:** [kizito@njikason.onmicrosoft.com]
- **Primary Administrator:** [adele@Njikason.onmicrosoft.com
- **License Type:** [Business Premium ]
- **MFA Status:** [Enabled / Disabled]

## Users & Groups
- **User Count:** [50+]
- **Group Types:** [Security / Distribution / M365 Groups]
- **Shared Mailboxes:** [support@Njikason.onmicrosoft.com, sales@njikason.onmicrosoft.com]

## Email Security & Compliance
- **Spam Filtering:** Enabled
- **Retention Policies:** 30 Days
- **Conditional Access Policies:** Applied

## Backup & Disaster Recovery
- **Email Backup Provider:** [Barracuda / SkyKick]
- **SharePoint & OneDrive Backup:** [Enabled / Not Enabled]
---
## **4. Standard Operating Procedure (SOP) - Password Reset**

# Procedure: Password Reset  

When a user forgets their password, follow this procedure to reset it securely.  
![Screenshot](images/screenshot101.jpg)
## Steps  
1. **Verify User Identity**  
   - Confirm user's identity via security questions or an alternate method.  
   - Check if the user has MFA enabled.  

2. **Reset Password**  
   - For **Active Directory**:  
     - Open **Active Directory Users & Computers (ADUC)**  
     - Locate the user and click **Reset Password**  
     - Assign a **temporary password**  
     - Ensure **User must change password at next logon** is checked  

   - For **Microsoft 365**:  
     - Log in to **admin.microsoft.com**  
     - Navigate to **Users > Active Users**  
     - Select the user and click **Reset Password**  

3. **Notify the User**  
   - Provide them with the new password securely (phone call or IT Glue secure note).  
   - Advise them to update their credentials across devices.  
---
## **5. VPN Issues Troubleshooting**

# Issue: VPN Connection Not Working  

User reports they are unable to connect to the company VPN.  
## Troubleshooting Steps  
1. **Verify Internet Connection**  
   - Ensure the user can browse the web.  

2. **Check VPN Credentials**  
   - Verify the username and password are correct.  
   - Ensure MFA authentication is working.  

3. **Confirm VPN Server is Online**  
   - Check VPN logs in the firewall/router.  

4. **Reinstall VPN Client**  
   - Instruct the user to remove and reinstall the VPN client.  

5. **Escalation**  
   - If the issue persists, escalate to Level 2 with logs attached.  
---
## **Why Screenshots Are Not Included**

# Why I Can't Include IT Glue Screenshots
I currently do not have access to an IT Glue free trial, which limits my ability to provide screenshots or firsthand experience. However, I have compiled this documentation template based on research, including YouTube videos and technical guides. This structure follows IT Glue’s best practices for maintaining accurate and accessible IT documentation.
``
