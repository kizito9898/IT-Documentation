# Device Enrollment for Windows Machines

## What is Microsoft Intune?
Microsoft Intune is a cloud-based endpoint management solution that allows organizations to manage and secure devices, applications, and data. It enables IT admins to enforce policies, deploy software, and ensure compliance across Windows, macOS, iOS, and Android devices. Intune is a key component of Microsoft Endpoint Manager.

---

## Microsoft Intune Admin Center

### Devices Overview
The **Devices** section in Intune provides a centralized dashboard displaying all managed devices. It allows IT administrators to monitor device compliance, onboard new devices, and manage existing ones.

### Setting Up Basic Equipment to Manage Devices
1. **Devices Overview** → **Windows Devices** → Click on **Enrollment**.

2. **Select Deployment Profiles** (Under **Windows Autopilot**)
   - **Windows Autopilot Deployment Profiles** → **Select Create Profile**
   - **Windows PC** → Basics (Give it a Name/Description)

3. **Convert All Targeted Devices to Autopilot**
   - **YES** → Out-of-the-Box Experience (Deployment Mode: **Joined to Entra ID** or **Hybrid**, User Account: **Admin or Standard**, Allow Pre-Provisioned Deployment: **Yes/No**)
   - **Assignments** (Add Groups + Add All Devices) → **Review & Create**.

---

## Next Configurations

1. **Configurations** → **Create** → **New Policy** (Windows 10 and Later)
2. **Profile Type** (Templates Name) → **Device Restrictions**
3. Select the **Restrictions** you want to enforce and click **Next**.
4. **Assignments** (Add Groups / All Users + Add All Devices) → **Review & Applicability**.

---

## Screenshot:
![Device Enrollment Notes](attachment:<your_screenshot_filename>)
