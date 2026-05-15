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

