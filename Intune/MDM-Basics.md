# Android Device Enrollment in Intune (Home Lab)

## Overview
This guide will help you set up a home lab to enroll an Android device in Microsoft Intune. You can use a **real Android phone** or a **virtual Android emulator** like BlueStacks or Android Studio.

---

## Prerequisites

Before you start, make sure you have:

- A **Microsoft 365 account** with **Intune admin access**
- An **Intune license** assigned to your user
- Access to **Microsoft Intune Admin Center**: [https://intune.microsoft.com](https://intune.microsoft.com)
- An **Android device** (physical or virtual)

---

## Step 1: Enable Android Enrollment in Intune

1. **Sign in** to [Intune Admin Center](https://intune.microsoft.com).
2. Go to **Devices > Android > Android Enrollment**.
3. Select **Android Enterprise Settings** and enable enrollment.
4. Choose the enrollment type:
   - **Work Profile (BYOD)** → for personal devices
   - **Fully Managed** → for company-owned devices
   - **Dedicated Devices** → for kiosks or shared devices
5. Click **Save**.

If you are using **Fully Managed** enrollment, you will also need to create an **Enrollment Profile** and save the **QR Code** for setup.

---

## Step 2: Set Up an Android Emulator (If You Don’t Have a Physical Device)

### Option 1: Use BlueStacks Emulator (Easiest)
1. **Download and install** BlueStacks: [https://www.bluestacks.com](https://www.bluestacks.com)
2. Open BlueStacks and **sign in with a Google account**.
3. Install the **Microsoft Intune Company Portal** app from the **Google Play Store**.

### Option 2: Use Android Studio Emulator
1. **Download and install** Android Studio: [https://developer.android.com/studio](https://developer.android.com/studio)
2. Open **AVD Manager** and create an Android Virtual Device (e.g., Pixel 4, Android 11).
3. Start the emulator and install **Microsoft Intune Company Portal**.

---

## Step 3: Enroll the Android Device in Intune

### **For BYOD (Work Profile)**
1. Open the **Google Play Store**.
2. Install **Microsoft Intune Company Portal**.
3. Open the **Company Portal app**.
4. **Sign in** with your **Microsoft 365 work account**.
5. Tap **Begin** and follow the steps.
6. Tap **Set Up Work Profile** and accept permissions.
7. Complete the setup and **restart the device if needed**.

### **For Fully Managed Devices**
1. **Factory reset the device** (Go to Settings > Reset > Erase All Data).
2. On the setup screen, **tap 6 times** on the first screen to enter **QR Code Enrollment Mode**.
3. Scan the **QR Code** you saved earlier from Intune.
4. Follow the on-screen instructions to enroll.

---

## Step 4: Verify Enrollment

### **On the Device**
1. Open the **Company Portal app**.
2. Go to **Devices**.
3. Check if the device shows as **Managed & Compliant**.

### **In Intune Admin Center**
1. Go to [https://intune.microsoft.com](https://intune.microsoft.com).
2. Navigate to **Devices > All Devices**.
3. Find your Android device.
4. Check the **Compliance Status**.

---

## Step 5: Set Up Compliance Policies

1. **Go to** [Intune Admin Center](https://intune.microsoft.com).
2. Navigate to **Devices > Compliance policies**.
3. Click **Create policy**.
4. Select **Android** as the platform.
5. Configure **compliance settings**, such as:
   - **Require device encryption**
   - **Enforce screen lock with a PIN or password**
   - **Block rooted devices**
6. Click **Next**, assign to **All Users or a specific group**.
7. Click **Create**.

After applying, go to **Devices > Compliance Policies > Policy Status** to check if devices are compliant.

---

## Step 6: Configure Conditional Access

1. Go to **Microsoft Entra Admin Center**: [https://entra.microsoft.com](https://entra.microsoft.com).
2. Navigate to **Security > Conditional Access**.
3. Click **New Policy**.
4. Name your policy (e.g., "Require Compliant Devices").
5. Under **Assignments**, select **Users and Groups**.
6. Under **Cloud Apps**, choose "All cloud apps" or specific apps like **Microsoft 365**.
7. Under **Conditions**, select **Device Compliance** and set it to **Require compliant device**.
8. Click **Grant > Require device to be marked as compliant**.
9. Click **Enable Policy > Create**.

Now, only compliant devices can access Microsoft 365 apps.

---

## Step 7: Explore App Protection Policies

1. Go to **Intune Admin Center**.
2. Navigate to **Apps > App Protection Policies**.
3. Click **Create Policy**.
4. Select **Android** as the platform.
5. Under **Apps**, choose "Microsoft apps" or add custom apps.
6. Configure **Data Protection settings**:
   - **Prevent copy/paste between work and personal apps**
   - **Require PIN for app access**
   - **Encrypt app data when the device is locked**
7. Click **Create**.

To check if policies apply, open **Microsoft Outlook** or **Teams** on the enrolled Android device.

---

## Next Steps

- Monitor device compliance in **Intune Admin Center**.
- Adjust policies based on security needs.
- Test access restrictions to ensure security policies work as expected.

This guide now includes **Compliance Policies, Conditional Access, and App Protection Policies**.
