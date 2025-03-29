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

``sh
cd C:\Chrome

## Packaging Google Chrome MSI for Intune

Run the following command to package the MSI:

```powershell
IntuneWinAppUtil.exe -C C:\Chrome -S GoogleChromeStandaloneEnterprise64.msi -O C:\Chrome
```

### Parameters:

- `-C` → Source folder containing Chrome MSI
    
- `-S` → Chrome MSI file name
    
- `-O` → Output folder where `.intunewin` file will be saved
    

### Output:

The tool will generate a file named:

```text
GoogleChromeEnterprise64.intunewin
```

Inside `C:\Chrome`

## Upload the Win32 App to Intune

1. Select **App type** → Choose **Windows app (Win32)**
    
2. Upload the `.intunewin` file
    
3. Click **Select app package file**
    
4. Browse to:
    
    ```text
    C:\Chrome\GoogleChromeEnterprise64.intunewin
    ```
    
5. Click **OK**
## Enter App Information

- **Name:** Google Chrome
    
- **Publisher:** Google
    
- **Category:** Productivity
    
- **Add a Logo:** (Select Image)

## Step 2: Configure App Installation

- **Install Program** (Options: Available, Uninstall: No)  
- **Step 3: Requirements**  
  - Operating System Architecture: 32-bit and 64-bit  
  - Minimum Operating System: Windows 10, 20H2  

- **Step 4: Detection Rules**  
  - Rule Format: Manually configure detection rules  
  - Add Rule Type: MSI and click OK  

- **Step 5: Dependencies**  

- **Step 6: Supersedence**  

- **Step 7: Assignments**  
  - Add all users  

- **Step 8: Review + Create and Create**
