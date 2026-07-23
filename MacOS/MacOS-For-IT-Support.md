# macOS for IT Support Troubleshooting

## Introduction

Welcome to my macOS documentation.

As an IT Support Professional with a strong foundation in Windows environments, I built this section to document my hands-on learning of Apple's macOS operating system.

My goal is simple: to broaden my technical skill set and demonstrate my ability to support users across multiple platforms.

I am currently building this portfolio and will continue updating it with step-by-step configurations, troubleshooting workflows, and screenshots as I explore macOS.

> **Note:** Some configurations are being tested in a local environment without a primary Apple ID.

---
## Cross-Platform Troubleshooting

Understanding how macOS handles local networking, permissions, and file systems makes me a more adaptable and effective IT Support professional and problem solver.

---
## Portfolio Objective

This repository serves as my living documentation as I expand beyond a Windows-only environment and continue developing my cross-platform IT support capabilities.

The goal is to build practical experience supporting both Windows and macOS environments through hands-on configuration, troubleshooting, and documentation.

# Case Study 1: User Having Performance Issues with a Mac Device

## Scenario

A user contacted IT Support reporting slow performance on their macOS device.

I reached out to the user via email and performed basic troubleshooting, such as asking the user to restart the system. However, the issue still persisted.

---
# Troubleshooting Sluggish macOS Performance

## Step 1: Isolate the Resource Hog (Activity Monitor)

The macOS equivalent of **Task Manager** in Windows is **Activity Monitor**. It is the primary diagnostic tool used to identify processes consuming excessive system resources.

### Open Activity Monitor

1. Press:

```text
Command (⌘) + Space
```

2. Type:

```text
Activity Monitor
```

3. Press **Enter**.

---
## Check CPU Usage

1. Open the **CPU** tab.
2. Sort processes by **% CPU** in descending order.
3. Look for:
   - Third-party applications consuming excessive CPU.
   - Stuck system processes.
   - Any process consistently using more than **80% CPU**.

---
## Check Memory Usage

1. Open the **Memory** tab.
2. Review the **Memory Pressure** graph located at the bottom of the window.

### Memory Pressure Colors

- **Green** – RAM usage is healthy and the system has sufficient available memory.
- **Yellow/Red** – The Mac is under memory pressure and is actively using storage (swap memory), which can significantly reduce system performance.
# macOS IT Support Troubleshooting

## Case Study 1: User Having Issues with Slow Mac Performance (Continued)

### Free Up Memory (RAM)

- Click on the **Memory** tab in **Activity Monitor**.
- Select applications that are consuming excessive memory.
- Click **Stop** or **Force Quit** to close unnecessary applications and free up RAM.

### Disable Startup Applications

- Open **System Settings**.
- Navigate to:

  **General → Login Items & Extensions**

- Review the list of applications that launch automatically when the Mac starts.
- Remove unnecessary applications using the **(-)** button to prevent them from starting automatically.

### Clear User Cache

- Open **Spotlight Search**.
- Type:

  ```
  ~/Library/Caches
  ```

- Open the **Caches** folder.
- Select unnecessary cache files or folders and move them to the **Trash**.

---
# Case Study 2: Mac Battery Drains Too Quickly

## Scenario

The user contacted IT Support because their Mac battery was draining much faster than expected.

## Troubleshooting Steps

### Check Battery Settings

- Open **System Settings**.
- Navigate to:

  **Battery** or **Energy**

- Enable **Low Power Mode** when needed to extend battery life.

### Identify High Energy Applications

- Open **Activity Monitor**.
- Select the **Energy** tab.
- Identify applications consuming excessive energy.
- Close unnecessary applications to reduce battery usage.
---
# Case Study 3: Wi-Fi Keeps Disconnecting Randomly

## Possible Cause

This issue can occur when macOS stores multiple old Wi-Fi profiles and passwords, causing connection conflicts.

## Troubleshooting

- Open the **Terminal** application.
- Continue troubleshooting by removing outdated Wi-Fi configurations or resetting the saved network settings

## Wi-Fi Keeps Disconnecting Randomly

Run the following command in Terminal:

```bash
sudo ifconfig en0 down && sudo ifconfig en0 up
```

- Enter your administrator password and press **Enter**.
- This resets the Wi-Fi connection without restarting the Mac.

---

## Storage Issues on macOS

If a user reports low storage or the Mac is running out of space:

1. Navigate to:
   - **Apple Menu** → **System Settings** → **Storage**
2. Review what is consuming storage space.
3. Delete unnecessary files such as:
   - Trash
   - Large documents
   - Other unwanted files
4. Enable **Empty Trash Automatically** if appropriate.

**Keyboard shortcut to bypass Trash when deleting:**

- **Option + Command + Delete**

### Remove Old Application Support Files

1. Open **Finder**.
2. From the menu bar, select **Go**.
3. Scroll down and choose **Go to Folder**.
4. Enter:

```text
/Library/Application Support
```

5. Review old application support files that are no longer needed.
6. Delete unnecessary files (administrator password may be required).

---

## External Drive Is Not Being Recognized

If a user's external drive is not appearing:

1. Open **Finder**.
2. Go to **Finder Settings** (or **Finder Preferences**, depending on the macOS version).
3. Verify that **External disks** are enabled under the appropriate tab.
4. Confirm that the external drive is selected to appear in Finder.

This is one of the first checks an IT support technician should perform before moving on to more advanced troubleshooting.








