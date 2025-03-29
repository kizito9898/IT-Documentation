# Windows Apps Management in Intune

Windows Apps management in Intune allows IT administrators to add, deploy, monitor, and control applications on Windows devices enrolled in Intune. It supports different app types, including Win32 apps, Microsoft Store apps, Line of Business (LOB) apps, and web links.

## Why is this Important?

- Helps IT admins track and control software deployment in an organization.
- Ensures users get approved and up-to-date applications.
- Allows for remote app installation, updates, and removals.
- Supports security and compliance by managing which software users can install.

## How it Works

1. Windows app → Click on Create → Select the app you want to enroll (Microsoft Edge, Windows 10 and later) and Next → 
2. App Information → Select Next → App Settings (Channel Stable) → 
3. Assignments → Review & Create

# Enrolling Win32 (Custom Windows App) in Intune

## Steps to Enroll a Win32 App

1. Click on **Create** from the Windows app.
2. Select **App Type** → Choose **Windows app (Win32)**.
3. Go to **App Information** → Click **Select File**.

### Important Note:
A Win32 app must be **converted into an Intunewin format** before being uploaded to Intune, as it is the only format Intune recognizes.

## Preparing a Win32 App for Intune

### 1. Download the Win32 Content Prep Tool
Download the **Win32 Content Prep Tool** from Microsoft's GitHub repository:  
[Microsoft-Win32-Content-Prep-Tool](https://github.com/microsoft/Microsoft-Win32-Content-Prep-Tool)

### 2. Download the Application
Download **Google Chrome Enterprise** (Download the 64-bit `.msi` file).

### 3. Organize the Files
- Place the **Google Chrome Enterprise .msi** file in a folder, e.g., `C:\Chrome`.
- Extract the **Win32 Content Prep Tool** (`IntuneWinAppUtil.exe`) and place it in the **same folder** as the Google Chrome `.msi` file.

### 4. Convert the App to Intunewin Format
- Open **Command Prompt (CMD) as Administrator**.
- Navigate to your working directory:

```sh
cd C:\Chrome
 