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