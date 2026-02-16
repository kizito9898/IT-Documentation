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

## Overall Impression

Overall, CIPP feels like a natural extension of the Microsoft 365 Administrator portal, but with extra features and automation that make it much easier to use.

---

# GDAP (Granular Delegated Admin Privileges)

GDAP allows an MSP (like a company using CIPP) to get permission to manage a customer’s Microsoft 365 tenants without being Global Admins inside their environment.

Before GDAP, MSPs used DAP (Delegated Admin Privileges), which gave too much access.
# CIPP (Cyberdrain Improved Partner Portal)

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

---

## Devices

- View all devices with details such as:
  - Display name  
  - Enrollment type  
  - Model  
  - Operating System  

---

## Intune

Navigation:

- **Applications** → **Autopilot** → **Device Management**

Device actions include:

- Sync device  
- Reboot device  
- Retrieve LAPS password  

---

## Add Autopilot Device

As a partner, you can register devices to Windows Autopilot using available methods.

---

## Push Applications from CIPP

Navigation:

- **Applications** → **Applications Queue**

Steps:

- Add Chocolatey app  
- Add Store app  
- Add Office app  
- Add MSP app  

Examples:

- Adobe  
- Google Chrome  
# CIPP – Security, Applications, Teams, and SharePoint

## Defender AV Status

- View Defender Antivirus status.

---

## Tenant Administration

Navigation:

- **Tenant Administration** → **Enterprise Applications**

### Intune Applications

- Push applications from Chocolatey.
- Enable and deploy applications to tenants.
- Deploy MSP applications such as:
  - Huntress  
  - HaloPSA  

---
## Teams & SharePoint

### OneDrive

Navigation:

- **Teams & SharePoint** → **OneDrive**

You can:

- See all OneDrive allocations in the OneDrive list  
- View last active date  
- View file count  
- View allocated storage (GB)  
- Perform actions such as:
  - Add permissions  
  - Remove permissions  

---

### SharePoint Sites

- View SharePoint site list.  
- Perform bulk add sites.  
- View:
  - URL  
  - Owners  
  - Last active date  
  - Data mapping URL  

Actions available:

- Add members  
- Remove members  
- Assign Site Admin  
- Remove Site Admin  

---

### Teams Management

Navigation:

- **Teams** → **Managing Teams**

You can:

- Add members  
- Remove members  

View details such as:

- Team details  
- Member policies  
- Guest policies  
- Team owners  
- Team members  
- Installed applications  

---

## Conditional Access

Navigation: from the dashboard scroll down to

- **Conditional Access** → **CA Policies**

You can deploy Conditional Access policies such as:

- Block high-risk users  
- CA Test policies  
- Require device compliance  

### Deployment Steps

1. Select tenants.  
2. Select template to apply.  
3. Review and deploy.  

### Template Library

- Select tenant.  
- Create Conditional Access policies.  
- Can also create policies for Intune.  

### CA Policy Tester

- Test Conditional Access policies before putting them into production.  
# CIPP – Conditional Access, Standards, Backup, and Exchange

## CA Vacation Mode

- Add a scheduled task to add or remove a user from Conditional Access exclusions.
- Applies for a specific period of time.

---

## Standards (Security Baselines)

Standards can be applied across your tenants, including:

- General standard settings  
- Global standards  
- Enabled alerts  
- Remediation settings  

---

## Backup Wizards

- Backups are stored in CIPP storage.
- They can be restored using the CIPP restore backup feature.
- You can back up:
  - Identity  
  - Conditional Access  
  - Intune compliance policies  

### Restore Backup

- Use the restore backup option to recover previously saved configurations.

---

# Email & Exchange

Navigation:

- **Administration** → **Mailboxes**
- **Deleted Mailboxes**
- **Mailbox Rules**
- **Contacts**
- **Quarantine**
- **Tenant Allow/Block Lists**

---

## Mailboxes

In the mailbox view, you can see:

- User Principal Name (UPN)  
- Display name  
- Primary email address  
- Recipient type  
- Available actions  

### Mailbox Actions

- Edit calendar permissions  
- Research compromised account  
- Convert to shared mailbox  
- Hide from Global Address List  
- Other administrative actions  

---

## Shared Mailboxes

- Add a new shared mailbox.
- View additional mailbox details.

---

## Restore Mailboxes

- Restore deleted mailboxes.
- View mailboxes applied to a tenant.
