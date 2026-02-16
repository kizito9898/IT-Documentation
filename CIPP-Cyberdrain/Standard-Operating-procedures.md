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

---
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
  - Azure DevOps Administrator  

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
# CIPP – User Management and Device Management Notes

## User Profile View

You can view more on a user profile, including:
 Go to **Administration** → **Users**.  
- You can switch between tenants or manage all tenants.  
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

Click on the three dots (**...**) for more actions:

- Require MFA registration  
- Add to groups  
---
## Onboarding Users

- Go to **Add Users**.  
- You can copy properties of another user.  
- More options are available when setting up a user account.  
- Copy group membership from an existing user.  
### JIT Admin
- Create an account that is usable for a specific period of time.  
- Schedule start date and end date.  
# CIPP – Dashboard, Navigation, and Identity Management

## Dashboard Navigation

Main navigation areas include:

- Identity Management  
- Tenant Administration  
- Security & Compliance  
- Intune  
- Teams & SharePoint  
- Email & Exchange  

---

## User Overview (When Clicking a User)

When you click on a user (e.g., Alex Allen), the following options are available:

- View User  
- Edit User  
- Exchange Settings  
- Compromise Remediation  
- Conditional Access  

---

## Tools (CIPP)

Navigation:

- Tools  
  - Tenant Tools  
  - Email Tools  
  - Dark Web Tools  
  - Template Library  
  - Community Repositories  
  - Scheduler  

---

## Tenant Administration

Navigation:

- Administration → Tenants  
- Alert Configuration  
- Audit Logs  
- Enterprise Applications  
- Secure Score  
- App Consent Requests  
- Authentication Methods  
- Partner Relationships  
- GDAP Management  
---
## Intune

Navigation:

- Applications → Autopilot → Device Management  
- Devices  
- Configuration Policies  
- Compliance Policies  
- Protection Policies  
- Policy Templates  
- Scripts  
---
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
---
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

* Manage Intune devices across your Microsoft 365 tenants. and the following features applies to

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
