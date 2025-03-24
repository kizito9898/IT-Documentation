# Microsoft Entra ID (Azure AD) - IT Administrator Guide

## 1. What is Microsoft Entra ID?

**Microsoft Entra ID (formerly Azure Active Directory)** is a cloud-based identity and access management (IAM) service from Microsoft. It helps organizations manage **user identities, authentication, and security policies** for applications and devices in Microsoft 365 and Azure environments.

### Key Uses of Entra ID:
- **User Authentication** – Secure sign-in for Microsoft 365, Azure, and third-party apps.
- **Single Sign-On (SSO)** – Users can access multiple applications with one login.
- **Multi-Factor Authentication (MFA)** – Adds extra security to sign-ins.
- **Conditional Access** – Restricts logins based on location, device, and risk factors.
- **Self-Service Password Reset (SSPR)** – Users can reset their passwords without IT help.
- **Identity Protection** – Detects and blocks suspicious login attempts.
- **Device Management** – Enforces security policies on Windows, iOS, Android, and macOS devices.
- **Role-Based Access Control (RBAC)** – Assigns user permissions based on job roles.
- **Audit Logs and Monitoring** – Tracks login activities and admin actions.

---

## 2. How to Create and Manage Users in Entra ID

### **2.1 Creating a New User**
As an IT Helpdesk or 365 Administrator you can create accounts in Microsoft 365 and Entra ID but you can't assign a license to user in Entra ID.

1. **Sign in** to the [Microsoft Entra admin center](https://entra.microsoft.com/).
2. Navigate to **Users** > **All Users**.
3. Click **+ New user** > **Create user**.
4. Enter the following details:
   - **User principal name (UPN)** (e.g., `James@Njikason.onmicrosoft.com)
   - **Name** (Full name of the user)
   - **Password** (Auto-generated or create one for them)(allow them change password on next login)
   - **Groups and Roles** (Assign permissions)
5. Click **Create** to add the user.

### **2.2 Managing Users**
- To **reset a password**, select the user > Click **Reset password**.
- To **assign roles**, select the user > Click **Assigned roles** > Choose a role (e.g., Global Admin, User Admin).
- To **disable or delete** a user, go to the user's profile > Click **Block sign-in** or **Delete**.

---

## 3. How to Create and Manage Groups

### **3.1 Creating a New Group**
1. Go to **Microsoft Entra admin center** > **Groups**.
2. Click **+ New group**.
3. Choose a **Group type**:
   - **Security** – Used for permission control.
   - **Microsoft 365** – Used for collaboration (Teams, SharePoint).
4. Enter a **Group name** and **Description**.
5. Assign **members** (users, devices, or other groups).
6. Click **Create**.
### Creating a Dynamic Group**
1. Navigate to **Microsoft Entra admin center** > **Groups**.
2. Click **+ New group**.
3. Choose **Security** or **Microsoft 365 Group**.
4. Under **Membership type**, select **Dynamic User** or **Dynamic Device**.
5. Click **Add dynamic query**.
6. Set rules (e.g., `department -eq "IT"` to add all IT users).
7. Click **Create**.

### **3.2 Managing Groups**
- **Add or remove members**: Open the group > Click **Members** > **+ Add members** or **Remove members**.
- **Assign a group owner**: Select **Owners** > **+ Add owners** > Choose a user.
- **Delete a group**: Open the group > Click **Delete group**.


## 4. Configuring Multi-Factor Authentication (MFA)

### **4.1 Enforcing MFA for Users**
1. Go to **Microsoft Entra admin center** > **Users**.
2. Click **Per-user MFA** settings.
3. Select the user(s) > Click **Enable MFA**.
4. Instruct users to complete setup using:
   - Microsoft Authenticator App
   - Phone call or SMS verification

### **4.2 Enabling MFA for All Users (Security Defaults)**
1. Navigate to **Microsoft Entra admin center** > **Properties**.
2. Click **Manage security defaults**.
3. Toggle **Enable security defaults** to **Yes**.
4. Click **Save**.

---

## 5. Setting Up Conditional Access Policies

### **5.1 Creating a Conditional Access Policy**
1. Go to **Microsoft Entra admin center** > **Security** > **Conditional Access**.
2. Click **+ New policy**.
3. Enter a **policy name**.
4. Under **Assignments**, choose:
   - **Users** – Select users or groups to apply the policy.
   - **Cloud apps** – Choose which applications to secure.
   - **Conditions** – Set login rules (e.g., IP address, device compliance).
5. Under **Access controls**, choose:
   - **Grant access with MFA** or **Block access**.
6. Click **Create** to activate the policy.

---

## 6. How to Enable Self-Service Password Reset (SSPR)

1. Go to **Microsoft Entra admin center** > **Password reset**.
2. Click **Properties** > Enable **Self-service password reset** for:
   - **None** (Disabled)
   - **Selected users** (Choose specific groups)
   - **All users** (Recommended)
3. Under **Authentication methods**, set at least **two** options:
   - Email
   - Phone number
   - Security questions
4. Click **Save**.

---

## 7. Monitoring and Audit Logs

### **7.1 Viewing Sign-In Logs**
1. Navigate to **Microsoft Entra admin center** > **Sign-in logs**.
2. Filter by **date, user, or application**.
3. Click an event to view details like:
   - IP address
   - Login status (Success/Failure)
   - MFA prompt (Yes/No)

### **7.2 Viewing Audit Logs**
1. Go to **Microsoft Entra admin center** > **Audit logs**.
2. Check logs for:
   - User creations, deletions, and modifications.
   - Role assignments.
   - Security policy changes.

---

## 8. Role-Based Access Control (RBAC)

### **8.1 Assigning Roles to Users**
1. Go to **Microsoft Entra admin center** > **Roles and administrators**.
2. Choose a **Role** (e.g., Global Admin, User Admin).
3. Click **+ Add assignments**.
4. Select a **user** and click **Assign**.

### **8.2 Common Roles in Entra ID**
| Role                       | Description                          |
| -------------------------- | ------------------------------------ |
| **Global Administrator**   | Full access to all settings          |
| **User Administrator**     | Manages users and groups             |
| **Security Administrator** | Manages security policies            |
| **Helpdesk Administrator** | Resets passwords and manages tickets |

---

## 9. Device Management in Entra ID

### **9.1 Registering Devices**
1. Navigate to **Microsoft Intune admin center** > **Devices**.
2. Click **Enroll devices**.
3. Select **Windows, macOS, iOS, or Android**.
4. Follow the on-screen steps for enrollment.

### **9.2 Managing Device Compliance**
1. Go to **Microsoft Intune admin center** > **Compliance policies**.
2. Click **+ Create policy**.
3. Select **OS type** (Windows, macOS, etc.).
4. Set policies like:
   - Require BitLocker encryption.
   - Block jailbroken/rooted devices.
5. Click **Create**.

---

## Conclusion

# Microsoft Entra ID (Azure AD) - Advanced IT Support Guide

## 1. Troubleshooting Entra ID Issues

### **1.1 Common Entra ID Issues and Fixes**
| Issue                                       | Cause                                            | Solution                                                                             |
| ------------------------------------------- | ------------------------------------------------ | ------------------------------------------------------------------------------------ |
| **User can’t sign in**                      | Wrong password, account locked, MFA issues       | Reset password, check MFA settings, verify Conditional Access policies               |
| **User is locked out**                      | Too many failed login attempts                   | Unlock account via **Microsoft Entra admin center** > **Users** > **Reset password** |
| **MFA is not working**                      | Outdated MFA settings, authentication app issues | Check **Security Info** in My Sign-Ins, resync MFA device                            |
| **Conditional Access blocking login**       | Policy misconfiguration                          | Review **Conditional Access** > Disable test policies                                |
| **User not receiving password reset email** | Email settings issue                             | Ensure **Self-Service Password Reset (SSPR)** is enabled                             |
| **Group-based access not working**          | Incorrect group membership                       | Check user’s **Group Memberships** under **Users**                                   |

### **1.2 How to Check Sign-In Logs for Troubleshooting**
1. Go to **Microsoft Entra admin center** > **Sign-in logs**.
2. Select the affected **User**.
3. Check the **Status**:
   - **Success** – Login is working fine.
   - **Failure** – Click for more details (error codes help in troubleshooting).
4. Identify reasons:
   - **Wrong password** (User error)
   - **Blocked sign-in** (Policy or admin action)
   - **MFA required but failed** (Reconfigure MFA)

---

## 2. Creating Groups in Microsoft Entra ID

### **2.1 Microsoft 365 Groups vs. Security Groups vs. Dynamic Groups**
| Group Type              | Purpose                                              |
| ----------------------- | ---------------------------------------------------- |
| **Microsoft 365 Group** | Used for collaboration (Teams, Outlook, SharePoint)  |
| **Security Group**      | Used for permission control (Access to resources)    |
| **Dynamic Group**       | Auto-assigns members based on user/device attributes |

### **2.2 Creating a Microsoft 365 Group**
1. Go to **Microsoft Entra admin center** > **Groups**.
2. Click **+ New group**.
3. Select **Group type**: **Microsoft 365**.
4. Enter **Group name** and **Description**.
5. Add **Owners** and **Members**.
6. Click **Create**.

### **2.3 Creating a Dynamic Group**
1. Navigate to **Microsoft Entra admin center** > **Groups**.
2. Click **+ New group**.
3. Choose **Security** or **Microsoft 365 Group**.
4. Under **Membership type**, select **Dynamic User** or **Dynamic Device**.
5. Click **Add dynamic query**.
6. Set rules (e.g., `department -eq "IT"` to add all IT users).
7. Click **Create**.

---

## 3. Identity Protection in Entra ID

### **3.1 What is Microsoft Entra ID Identity Protection?**
Identity Protection helps detect and respond to security risks like:
- **Leaked credentials** – If a user’s credentials are found in a data breach.
- **Unusual sign-in locations** – Flags risky logins from unknown locations.
- **Impossible travel** – If a user logs in from Nigeria and the US within minutes.

### **3.2 How to Monitor Identity Protection**
1. Go to **Microsoft Entra admin center** > **Identity Protection**.
2. Check:
   - **Risky Users** – Users with suspicious activity.
   - **Risky Sign-ins** – Logins flagged as high risk.
   - **Risk Detections** – Alerts for suspicious activity.

### **3.3 How to Respond to Identity Risks**
- **Block risky sign-ins** using Conditional Access.
- **Force password resets** for compromised users.
- **Enable MFA** for high-risk users.

---

## 4. Authentication Methods – Best Practices

### **4.1 Password Protection**
- Use **at least 14 characters** with a mix of **uppercase, lowercase, numbers, and symbols**.
- **Block weak passwords** with **Password Protection**:
  1. Go to **Microsoft Entra admin center** > **Security** > **Password Protection**.
  2. Enable **Enforce custom banned passwords**.

### **4.2 Multi-Factor Authentication (MFA) Best Practices**
- **Enforce MFA for all users** via **Security Defaults**.
- **Use Microsoft Authenticator** instead of SMS (Best recommended practices)
- **Enable passwordless authentication** (FIDO2 keys, Windows Hello).

### **4.3 Authentication Strength Policy**
1. Go to **Microsoft Entra admin center** > **Security** > **Authentication Methods**.
2. Enable:
   - **Passwordless sign-in** (FIDO2 security keys, Windows Hello).
   - **Strong MFA enforcement** for admin accounts.
3. Save the policy.

---

## Conclusion



---

