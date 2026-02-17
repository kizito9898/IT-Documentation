# CIPP (Cyberdrain Improved Partner Portal)

CIPP (Cyberdrain Improved Partner Portal) is a multi-tenant management tool for Microsoft 365, making it easy to manage multiple clients from a centralized portal experience. It is also an open-source project.

It centralizes administration across tenants so MSPs do not have to log into each environment separately.

You can switch between tenants or manage all tenants at once from the top bar.
## Features

### User Management
- Adding users  
- Resetting passwords  

### Offboarding Wizards
- Automates mailbox conversion  
- Disables sign-in  
- Converts mailbox to shared mailbox  

### Conditional Access
- Conditional Access policies that can be applied across multiple tenants at once 

# GDAP (Granular Delegated Admin Privileges)

GDAP allows an MSP (like a company using CIPP) to get permission to manage a customer’s Microsoft 365 tenants without being Global Admins inside their environment.

Before GDAP, MSPs used DAP (Delegated Admin Privileges), which gave too much access
## Onboarding

- Onboarding is the most difficult part of the tool.  
- It involves onboarding steps with GitHub repositories.  
### CIPP Setup Wizard

- Used for creating app registrations for read and write permissions within CIPP.  
- Step 1: Select **"I would like CIPP to create an application for me."**  
- Step 2: Click **Start Setup Wizard**.  
### GDAP Validation

- Validate that you have a proper GDAP relationship (GDAP check).  
- Run GDAP check.  
- Run permissions check.  
### Tenant Onboarding

- Go to **Administration**.  
- Scroll down to **Tenant Onboarding**.  
- Onboard various tenants into CIPP.  
---
## GDAP Roles

- GDAP consists of roles such as:
  - Application Administrator  
  - Application Developer  
  - Azure DevOps Administrator  etc
### Role Wizard

- Select which roles you want to map to groups in your partner tenant.  

**Step 1:**  
- For each role selected, a new group will be created inside your partner tenant.  
- The group will be named:  
  `M365 GDAP <RoleName>`  

- Add users to these new groups to assign their GDAP permissions.  
---
## Offboarding Tenant

- Go to **Tenant Settings**.  
- Choose the tenant to offboard.  
- Open **Tenant Offboarding Settings**.  
- Review and confirm.  
--- 
# CIPP – Dashboard, Navigation, and Identity Management

## Onboarding Users

- Go to **Add Users**.  
- You can copy properties of another user.  
- More options are available when setting up a user account.  
- Copy group membership from an existing user. 

## User Overview (When Clicking a User)

When you click on a user (e.g., Alex Allen), the following options are available:

you can view more on a user profile, including:
 Go to **Administration** → **Users**.    
- User details  
- Microsoft 365 management details  
- OneDrive details  
- Last login details  
- Applied Conditional Access policies  
- Compromise remediation information  
---
## User Actions
Available actions include:
- Edit user  
- Edit mailbox permissions  
- Send MFA push  
- Reset password  
- Convert to shared mailbox  
- Generate temporary password  

# CIPP – Identity Management

Navigation:

- Administration → Users (User Management)

Features include:

- Equivalent to and extends Microsoft 365 Admin  
- Bulk Add (Wizard allows bulk creation of users)  
- Invite Guest  
- Add User  
  - Add User Wizard provides an interface for creating new user accounts in a partner tenant.  
---
## View Individual User

- Provides a comprehensive overview of user details and settings.  
- Serves as the main landing page when viewing a user.  
- Additional tabs are available for more specific operations such as:
  - Edit User  
  - Compromise Remediation  
# Edit User – Identity Management

* Navigate to:  
  **Identity Management → Administration → Users → Select a User → Click Edit User**  
  You will be redirected to the **Edit User** page.
### JIT Admin
- Create an account that is usable for a specific period of time.  
- Schedule start date and end date. 
# Exchange Settings

* This page displays information about the user’s Exchange configuration.

* Available Exchange Settings options:
  - Send MFA Push  
  - Convert Mailbox  
  - Delete Mailbox  
---
# Conditional Access

* Allows you to test your Conditional Access policies before deploying them to production.

* Ensure you deploy your test policy in **Report-Only Mode** to verify it works correctly without breaking access.
---
# Intune – Applications

* Navigate to:  
  **Intune → Applications → Add Applications**

* Add Microsoft Store App (choose app)

* Application Queue  
  - Shows applications queued for deployment to your tenant.

* Autopilot Devices  
  - This page lists all devices registered for Autopilot.

* Add Profiles  
  - Manage Autopilot profiles across your Microsoft 365 tenants.
---
# Devices

* Manage Intune devices across your Microsoft 365 tenants.

* Available device actions:
  - View in Intune  
  - Rename Device  
  - Sync Device  
  - Locate Device  
  - Wipe Device  
  - Keep Enrollment State  
  - Fresh Start  
  - Retire Device  

---
# Configuration Policies

* Compliance Policies  
  - Create templates based on policy  
  - Assign to all users  
  - Delete policy  

* Protection Policies  
  - Apply Policy  
    - The Apply Policy Wizard provides the ability to select one or more tenants and add MDM policy to their MDM portal.

Steps:
1. Tenant Selection  
2. Policy Configuration  
3. Confirmation  
* Audit & Device Score
---
# Teams & SharePoint

* OneDrive  
  - View OneDrive information for users in your Microsoft 365 tenants.  
  - Add & Remove Permissions  
# SharePoint

* Navigate to:  
  **SharePoint → Review SharePoint Sites & Usage**

* Available options:
  - Add Site  
  - Bulk Edit Sites  

* Teams  
  - The List Teams page displays all teams along with:
    - Name  
    - Description  
    - Overview (Public or Private team)  

  - Add Team  
    - Allows you to create a new team  

  - Team Activity  

  - Business Voice  
---
# Email & Exchange

* View information on all mailboxes in your Microsoft 365 tenants.

* Provides the ability to:
  - View Exchange mailboxes  
  - Edit mailbox  
  - View connected mobile devices  
  - Add shared mailbox  
  - Add M365 user  
  - View deleted mailboxes  
  - Configure mailbox rules  

* Contacts  
  - View & Edit Contacts in your M365 tenants  
  - All Contacts  
  - Edit Contact  
  - Contact Templates (Deploy, Add & Edit Contact)
* Quarantine  
* Retention Policies & Tags  
* Transport Rules  
* Connectors  
* Resource Management  
* Reports  
---
# Tools

* Tenant Tools  
  - Graph Explorer  
  - Application Approval  
  - Tenant Lookup  
  - IP Database  
---
# Email Tools

* Message Trace  
  - Allows you to trace an email instantly from any recipient or sender within the last 10 days.
---
# Template Library

* Retrieve the latest version of a specific tenant’s policies.
---
# Scheduler

* Allows you to schedule CPP functionality to be executed at a later date and send results to your:
  - PSA  
  - Webhook  
  - Email  
## 1. Introduction

**CIPP (Cyberdrain Improved Partner Portal)** is an open-source, multi-tenant management platform designed for Managed Service Providers (MSPs). It serves as a centralized "single pane of glass" for administering Microsoft 365 environments.

Instead of logging into each client's tenant individually, CIPP allows administrators to:

- Switch between tenants instantly via a unified top bar.
    
- Apply configurations to all tenants simultaneously.
    
- Automate routine tasks like onboarding and offboarding.
    
---

## 2. Security & Permissions (GDAP)

CIPP relies on **GDAP (Granular Delegated Admin Privileges)** to function securely.

### What is GDAP?

GDAP is a Microsoft security feature that allows MSPs to manage customer tenants with "least privilege" access. Unlike the older DAP (Delegated Admin Privileges), which granted broad Global Admin rights, GDAP allows you to request specific roles for specific durations.

### GDAP Roles & The Role Wizard

To manage clients effectively, you must map roles in CIPP to groups in your partner tenant.

- **Role Mapping:** You select roles (e.g., _Application Administrator_, _Intune Administrator_, _Exchange Administrator_).
    
- **Group Creation:** CIPP creates a corresponding group for each role in your partner tenant (e.g., `M365 GDAP Exchange Admin`).
    
- **Assignment:** You add your technicians to these groups to grant them permissions across client tenants.
    

---

## 3. Setup & Onboarding

This section covers how to set up the CIPP instance and bring client tenants into the ecosystem.

### CIPP Instance Setup

- **Setup Wizard:** Automates the creation of App Registrations required for CIPP to read/write data.
    
    - Step 1: Select **"I would like CIPP to create an application for me."**
        
    - Step 2: Click **Start Setup Wizard**.
        

### Tenant Onboarding

Once CIPP is running, you must onboard client tenants.

1. Navigate to **Administration** → **Tenant Onboarding**.
    
2. **GDAP Validation:** Run the "GDAP Check" to ensure a valid relationship exists between the partner tenant and the client.
    
3. **Permissions Check:** Verifies that CIPP has the necessary API permissions to manage the tenant.
    

### Tenant Offboarding

When a client leaves the MSP, offboarding ensures clean removal of access.

- Navigate to **Tenant Settings** → **Tenant Offboarding Settings**.
    
- Select the tenant and confirm removal. This removes CIPP’s access to that specific environment.
    

---

## 4. Identity & User Management

This module consolidates all user-related actions, replacing the standard Microsoft 365 Admin Center for day-to-day tasks.

### User Overview

Navigate to **Identity Management** → **Administration** → **Users**. Clicking on a user (e.g., _Alex Allen_) opens a detailed profile containing:

- **M365 & OneDrive Details:** Storage usage, licensing, and last login time.
    
- **Security Posture:** Applied Conditional Access policies and compromise remediation history.
     
- Microsoft 365 management details  
- OneDrive details  
- Last login details  
- Applied Conditional Access policies  
- Compromise remediation information  

### User Actions (Day-to-Day)

- **Quick Actions:** Reset passwords, send MFA push notifications, and unlock accounts.
    
- **Edit User:** Modify properties, contact info, and licenses.
    
- **JIT (Just-In-Time) Admin:** Create a temporary admin account for a technician that automatically expires after a scheduled start and end date.
    
### Lifecycle Automation

- **Bulk Add Wizard:** Create multiple users across tenants simultaneously using templates.
    
- **Offboarding Wizard:** A critical tool for employee departures. It automates:
    
    - Disabling sign-in.
        
    - Converting the user mailbox to a Shared Mailbox.
        
    - Removing licenses.
        
    - Canceling future calendar events.
---
## 5. Device Management (Intune)

Manage endpoints (laptops, mobiles) across all tenants from one view.

### Devices

Navigate to **Intune** → **Devices**.

- **Device Actions:** Perform remote actions such as _Wipe_, _Retire_, _Fresh Start_, _Sync_, or _Rename_.
    
- **Autopilot:** Manage Autopilot device hashes and profiles for zero-touch deployment.
    

### Applications

Navigate to **Intune** → **Applications**.

- **Add Applications:** Deploy apps (e.g., Microsoft Store apps) to specific tenants or groups.
    
- **Application Queue:** Monitor the status of app deployments.
    

### Configuration Policies

- **Compliance Policies:** Create and assign templates that dictate device security requirements (e.g., BitLocker enabled, minimum OS version).
    
- **Apply Policy Wizard:** Deploys MDM policies to multiple tenants in three steps:
    
    1. Select Tenants.
        
    2. Configure Policy.
        
    3. Confirm Deployment.
        

---

## 6. Collaboration & Content

Manage the structure and security of Teams, SharePoint, and OneDrive.

### Teams

- **List Teams:** View all Teams, their privacy status (Public/Private), and member counts.
    
- **Management:** Create new Teams or modify existing ones.
    

### SharePoint

- **Site Management:** View storage usage, add new sites, or bulk edit site settings.
    
- **Permissions:** Add or remove user access to specific SharePoint libraries.
    

### OneDrive

- **Inspector:** View OneDrive status for specific users and modify permissions (e.g., granting a manager access to a terminated employee's files).
    

---

## 7. Email & Exchange Administration

Comprehensive tools for managing mail flow and mailboxes.

### Mailbox Management

- **General Actions:** Convert to Shared Mailbox, configure delegation rights, and edit mailbox permissions.
    
- **Tools:**
    
    - **Message Trace:** instantly trace emails across the last 10 days to troubleshoot delivery issues.
        
    - **Quarantine:** Release or block quarantined emails.
        

### Resources & Contacts

- **Resource Management:** Manage room and equipment mailboxes.
    
- **Contacts:** Create and edit global contacts or deploy contact templates to standardize address books.
    

---

## 8. Advanced Tools & Automation

### Conditional Access (CA)

- **Multi-Tenant Deployment:** Apply a standard baseline CA policy to multiple tenants at once.
    
- **Report-Only Mode:** Deploys policies in a "log-only" state to test their impact without locking users out.
    

### Scheduler

Automates CIPP maintenance tasks. You can schedule scripts or compliance checks to run at specific times and push the results to:

- A PSA (Professional Services Automation) tool.
    
- A Webhook (for custom integrations).
    
- Email reports.
    

### Template Library

A repository that allows you to "snapshot" a tenant's configuration (e.g., Intune policies or Transport rules) and save it as a template to deploy to other clients.