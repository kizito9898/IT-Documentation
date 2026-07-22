

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
- Add Marketing users to the **Marketing** security group
# Adding Users to Security Groups

Open the required security group.

Example:

- Open the **Accounting** security group.
- Select the **Members** tab.
- Click **Add**.
- Type the username.
- Click **Check Names** until the user is resolved.
- Click **OK**.
- Click **Apply**.

The selected users are now members of the **Accounting** security group.

---

# Windows File Permissions

In Windows environments, especially file servers and shared folders, there are two main permission types:

- NTFS Permissions
- Share Permissions

Both control who can access files and what actions users can perform. They work together but apply in different situations.

---

## NTFS Permissions

NTFS permissions are stored on drives formatted with the **New Technology File System (NTFS)**.

They apply both:

- Locally (when logged into the computer)
- Over the network

### Common NTFS Permission Levels

- **Full Control**
  - Read
  - Write
  - Modify
  - Delete
  - Change permissions

- **Modify**
  - Read
  - Write
  - Edit
  - Delete

- **Read & Execute**
  - View files
  - Open files
  - Run programs

- **List Folder Contents**
  - View files and folders inside a directory

- **Read**
  - Open files
  - View file contents

- **Write**
  - Create new files and folders
  - Modify existing files

---

## Share Permissions

Share permissions control access when a folder is shared over the network.

They only apply when users access the folder through a shared network path.

Example:

```text
\\FileServer\SharedFolder
```

### Common Share Permission Levels

- **Full Control**
  - Read
  - Write
  - Modify
  - Delete
  - Change permissions

- **Change**
  - Read
  - Write
  - Modify

- **Read**
  - View files
  - View subfolders
  - Read file data
  - Run programs

When a user connects to a shared folder from another computer, **Share Permissions** determine the user's initial level of access. NTFS permissions are then combined with Share Permissions to determine the user's effective permissions.