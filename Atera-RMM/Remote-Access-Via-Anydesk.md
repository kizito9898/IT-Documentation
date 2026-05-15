# Remote Connection with AnyDesk

## Introduction to AnyDesk

AnyDesk is a fast and secure remote desktop application that allows users to remotely access and control computers, servers, and mobile devices from anywhere.

It provides:

- Low-latency remote connections
- High frame-rate screen sharing
- Remote work capabilities
- IT support functionality
- File sharing and file transfer across:
    - Windows
    - macOS
    - Linux
    - Android

## AnyDesk Integration with Atera

AnyDesk is integrated with Atera RMM, allowing technicians to remotely connect to managed devices through installed Atera agents.

The connection process is similar to Splashtop remote access.


## Connecting to a Device Using AnyDesk

1. Navigate to **Devices** in Atera.
2. Select the target device.
3. Click **Connect**.
4. Choose **AnyDesk** as the remote connection method.
5. Launch the AnyDesk session.
6. Enter the connection password if required.
7. The end user must approve the connection request before remote access is granted.

Once accepted, the technician gains remote access to the user's system.

## Remote Support Scenario

Using AnyDesk, I connected to a Windows 11 Pro device to troubleshoot a user issue.

### Reported Issue

The user reported difficulty accessing a shared work folder required for daily operations.

### Troubleshooting Steps

1. Logged the issue in the ticketing system.
2. Asked the user:
    - Whether the shared folder had been accessible previously
    - Which shared folder they needed access to
3. Verified the user's permissions.
4. Confirmed access rights to the shared directory.
5. Remapped the shared folder for the user.

## Network Connectivity Check

To confirm internet connectivity and network access, I performed a connectivity test using:

```
ping 8.8.8.8
```

This helped verify that the device had an active internet connection and could communicate externally.

# File Transfer and Device Management with Atera

## File Browsing and Transfer

Atera allows technicians to transfer files between local and remote devices during remote support sessions.

### Uploading Files to a Remote Device

1. Open the remote connection session.
2. Navigate to the **File Transfer** or **Browse Files** feature.
3. Select the folder location from the primary device.
4. Choose the required file.
5. Click **Upload**.
6. The file is transferred and downloaded to the remote device.

This feature is useful for:

- Sending software installers
- Delivering configuration files
- Uploading troubleshooting tools
- Sharing documents with end users

## Disconnecting a Remote Session

After completing support activities:

1. Disconnect the remote connection session.
2. Ensure all troubleshooting tasks are completed before ending the session.

---

# Device Management Features in Atera

The **Manage** section in Atera provides several administrative and troubleshooting tools, including:

- Patch Management
- Software Inventory
- Run Scripts
- Service Manager
- Task Manager
- Command Prompt
- PowerShell
- Additional remote management tools

---

# Running Scripts on Windows 11 Devices

## Accessing Shared Script Library

1. Navigate to the target device.
2. Click **Manage**.
3. Open **Scripts**.
4. Access the **Shared Script Library**.

### Example Usage

Scripts can be used for:

- System cleanup
- Configuration changes
- Removing temporary files
- Automating administrative tasks
- Troubleshooting Windows issues

Example:

- Running cleanup and removal scripts on a Windows 11 Pro device.

---

# Managing Services with Service Manager

The **Service Manager** allows administrators to:

- Start services
- Stop services
- Restart services

### Example

Managing the **Print Spooler** service:

1. Open **Service Manager**.
2. Locate **Print Spooler**.
3. Choose:
    - Start
    - Stop
    - Restart

This is useful when troubleshooting printer-related issues.

---

# Using Command Prompt and PowerShell

Atera allows IT professionals to run:

- Command Prompt commands
- PowerShell scripts

Commands can be executed as:

- System user
- Logged-in user

This helps administrators perform remote diagnostics and advanced troubleshooting tasks.

---

# Managing Background Applications with Task Manager

The **Task Manager** feature helps identify applications consuming excessive system resources.

## Troubleshooting Slow Performance

### Scenario

A user reports slow system performance on their device.

### Steps Performed

1. Open **Task Manager** from the device management tools.
2. Review running applications and background processes.
3. Identify unnecessary or resource-intensive tasks.
4. Select the unnecessary application.
5. Click **End Task**.

This helps improve system performance and free up CPU and memory resources.

---
# Remote Device Power Actions

Atera allows administrators to perform remote power actions, including:

- Log off
- Restart
- Shutdown

These actions can be performed remotely without physically accessing the device.