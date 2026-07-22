

## What is a File Server?

A file server is a computer or server that stores files in one central place and lets other computers access those files over a network.

A file server also controls who can access which files, lets multiple users access files at the same time, and keeps files available even if someone's computer is turned off.

This is how a file server works in Active Directory.

The key components include:

- Domain Controller (DC), which runs Active Directory.
- Stores user accounts, groups, and permissions.
- Authenticates users when they log in.
---
# Getting Started with File Server

Go to the server and open **File Explorer**.

- Navigate to the **C:** drive.
- Create a new folder called **Company Data**.
- For this lab practice, create four department folders:
  - HR
  - IT
  - Marketing
  - Accounting

After creating the folders, continue with Active Directory configuration.

---
# Create Security Groups in Active Directory

Navigate to **Windows Server 2025**.

- Open **Server Manager**.
- Click **Tools**.
- Select **Active Directory Users and Computers**.
- When Active Directory opens, expand your domain.
- Browse to the **USA OU**.
- Open the **Users** OU.
- Create security groups for each department folder:
  - Accounting
  - HR
  - IT
  - Marketing

These security groups will later be used to assign folder permissions instead of assigning permissions directly to individual users.

---
# Add Users to Security Groups

Add users to their appropriate department security groups.

Example:

- Add Accounting users to the **Accounting** security group.
- Add HR users to the **HR** security group.
- Add IT users to the **IT** security group.
- Add Marketing users to the **Marketing** security group.