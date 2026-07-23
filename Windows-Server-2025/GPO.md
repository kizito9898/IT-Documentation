# Group Policy Management

## What is Group Policy Management?

Group Policy is the primary mechanism for enforcing configuration standards across a Windows Active Directory environment. It allows IT administrators to define configurations once and apply them centrally to thousands of computers and users, significantly reducing manual configuration time.

## Objective

This section documents my hands-on experience using the **Group Policy Management Console (GPMC)** in Active Directory to:

- Enforce security baselines
- Automate client configurations
- Centralize user and computer settings across a domain

## Prerequisites

Before working with Group Policy Management, ensure the following prerequisites are met:

- Active Directory Domain Services (AD DS) is configured and operational.
- A Domain Administrator account or delegated administrative permissions are available.
- Group Policy Management tools are installed.
- A Windows 11 client machine is joined to the domain for testing Group Policy Objects (GPOs).
# Getting Started

## Launching Group Policy Management Console (GPMC)

There are two ways to open the Group Policy Management Console:

### Method 1: Run Command

1. Press **Windows + R** to open the **Run** dialog.
2. Type:

   ```text
   gpmc.msc
   ```

3. Press **Enter** to launch the **Group Policy Management Console (GPMC)**.

### Method 2: Server Manager

1. Open **Windows Server Manager**.
2. Click **Tools**.
3. Select **Group Policy Management**.
---
# Creating a New Group Policy Object (GPO)

1. Expand **Group Policy Objects**.
2. Right-click **Group Policy Objects**.
3. Select **New**.
4. Enter a name for the policy (for example, **Test GPO**).
5. Click **OK**.
---
# Configuring Security Filtering

To apply the policy to only a specific user:

1. Select the newly created **Test GPO**.
2. Under **Security Filtering**, you will see **Authenticated Users** by default.
3. Click **Add**.
4. Enter the name of the test user.
5. Click **Check Names**.
6. Click **OK**.
7. Remove **Authenticated Users** from the Security Filtering list.
8. If prompted, confirm the removal and click **OK**.

---

# Linking the GPO

1. Link the GPO to the target Organizational Unit (OU) (for example, **Users**).
2. This allows the policy to be applied within that OU while Security Filtering ensures only the specified test user receives the policy.

---

## Note

Even if the GPO is linked to the top-level **Users** OU, the policy will only apply to the specific user added in **Security Filtering**, since **Authenticated Users** has been removed.

# Group Policy Management – GPO Delegation and Configuring Windows Defender Firewall

## GPO Delegation

At the top of the **Test GPO**, the **Delegation** tab allows administrators to grant specific permissions to users or groups that the policy applies to, such as:

- Full Control
- Edit
- Read

The **Settings** tab displays the details of the Group Policy Object (GPO), including:

- The configured policy settings.
- Whether the GPO contains **Computer Configuration** or **User Configuration** settings.
- Which users or computers the GPO applies to.

---

# Lab: Disable the Domain Firewall Using Group Policy

## Step 1: Create a New GPO

1. Open **Group Policy Management**.
2. Expand **Group Policy Objects**.
3. Right-click **Group Policy Objects** and select **New**.
4. Name the policy:

   ```
   Disable Domain Firewall
   ```

5. Click **OK**.

---

## Step 2: Edit the GPO

1. Right-click the newly created **Disable Domain Firewall** GPO.
2. Select **Edit**.

The editor displays two main sections:

- Computer Configuration
- User Configuration

> **Note:** Since disabling the Windows Defender Firewall is a computer-wide setting, this configuration must be made under **Computer Configuration**, not **User Configuration**.

### Policies vs Preferences

- **Policies** enforce settings that users generally cannot change.
- **Preferences** configure settings that users can usually modify later if necessary.

---
## Step 3: Navigate to Windows Defender Firewall Settings

Navigate to:

```text
Computer Configuration
└── Policies
    └── Windows Settings
        └── Security Settings
            └── Windows Defender Firewall with Advanced Security
```

Expand **Windows Defender Firewall with Advanced Security** to configure the firewall profiles and settings for domain-joined computers.


