# Device Enrollment for Windows Machines

## What is Microsoft Intune?
Microsoft Intune is a cloud-based endpoint management solution that allows organizations to manage and secure devices, applications, and data. It helps IT administrators enforce security policies, deploy software, and monitor device compliance across Windows, macOS, iOS, and Android devices.

### Benefits of Microsoft Intune for Organizations:
- **Device Management:** Allows IT teams to enroll, configure, and manage devices remotely.
- **Application Deployment:** Enables secure deployment and management of business apps.
- **Security & Compliance:** Enforces security policies like encryption, antivirus, and conditional access.
- **Cloud Integration:** Works seamlessly with Microsoft 365, Azure AD, and Defender for Endpoint.
- **BYOD Support:** Allows organizations to manage corporate data on personal devices securely.

---

## Microsoft Intune Admin Center

### Devices Overview
1. Shows an overview of all devices.
2. Displays device onboarding and management options.
3. Provides insights into device info within Intune.

### Setting Up Basic Equipment to Manage Devices
1. Go to **Devices Overview** → **Windows Devices**.
2. Click on **Enrollment**.

---

## Deployment Profiles

### Creating a Deployment Profile
1. Select **Deployment Profiles** under **Windows Autopilot**.
2. Click **Create Profile**.
   - **Platform:** Windows PC  
   - **Profile Type:** Basics  
   - **Name & Description:** Provide a descriptive name.

### Configuration Options
1. **Out-of-Box Experience (OOBE)**
   - **Deployment Mode:** Join to Azure AD or Hybrid AD Join.
   - **User Account Type:** Standard user or Administrator.
   - **Pre-Provisioned Deployment (Windows Autopilot for pre-setup devices):** Yes/No.

2. **Assignments**
   - Add **Groups** → **All Devices**.

3. Click **Review & Create** to finalize the setup.

---

## Next Configuration

### Creating a Configuration Profile
1. Go to **Configuration** → **Create** → **New Policy** (Includes Windows 10 and later).
2. Choose **Profile Type** and enter a template name.
3. Select **Device Restrictions** and configure desired restrictions.
4. Click **Next**.
5. **Assignments**
   - Add **Groups/Users** → **All Devices**.
6. Click **Apply & Deploy**.

---

This Markdown format is structured for easy readability in Obsidian. Let me know if you need any modifications!  
