# Microsoft Entra ID (Azure AD) - IT Administrator

## 1. What is Microsoft Entra ID?

**Microsoft Entra ID (formerly Azure Active Directory)** is a cloud-based identity and access management (IAM) service from Microsoft. It helps organizations manage **user & Groups, authentication, and security policies** for applications and devices in Microsoft 365 . it is a cloud based version of the on-premises Active Directory uses and computers and it can be configured as a Hybrid solution known as Entra ID Connect to sync.

### Key Uses of Entra ID : 
- **User Authentication** – Secure sign-in for Microsoft 365, Azure, and third-party apps.
- **Single Sign-On (SSO)** – Users can access multiple applications with one login.
- **Multi-Factor Authentication (MFA)** – Adds extra security to sign-ins.
- **Conditional Access** – Restricts logins based on location, device, and risk factors.
- **Self-Service Password Reset (SSPR)** – Users can reset their passwords without IT help.
- **Device Management** – Enforces security policies on Windows, iOS, Android, and macOS devices

---
![Screenshot](images/screenshot27.jpg)
## 2. How to Create and Manage Users in Entra ID

### **2.1 Creating a New User**
As an IT Helpdesk or 365 Administrator you can create a user account in Microsoft 365 and Entra ID but you can't assign a license to user in Entra ID.

1. **Sign in** to the [Microsoft Entra admin center](https://entra.microsoft.com/).
2. Navigate to **Users** > **All Users**.
3. Click **+ New user** > **Create user**.
4. Enter the following details:
   - **User principal name (UPN)** (e.g., `James@Njikason.onmicrosoft.com)
   - **Name** (Full name of the user)
   - **Password** (Auto-generated or create one for them)(allow them change password on next login)
   - **Groups and Roles** (Assign permissions)
5. Click **Create** to add the user.

![Screenshot](images/screenshot29.jpg)
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
![Screenshot](images/screenshot31.jpg)
### Creating a Dynamic Group
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
![Screenshot](images/screenshot41.jpg)
---
## 4. Configuring Multi-Factor Authentication (MFA)

 - By Default you can also create Multi-Factor Authentication on Microsoft 365 allowing you sign in into your account using an authenticator app by scanning the QR Code using your mobile device or whatever.
### **4.1 Enforcing MFA for Users**
1. Go to **Microsoft Entra admin center** > **Users**.
2. Click **Per-user MFA** settings.
3. Select the user(s) > Click **Enable MFA**.
4. Instruct users to complete setup using:
   - Microsoft Authenticator App
   - Phone call or SMS verification
![Screenshot](images/screenshot34.jpg)
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

1. Go to **Microsoft Entra admin center** > **Protection** >**Password Reset** .
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

## Devices in Entra ID  

Microsoft Entra ID (formerly Azure AD) provides centralized device management, allowing organizations to enforce security policies, monitor compliance, and manage device lifecycles.  

### Managing Devices in Entra ID  

- **All Devices Dashboard**: Provides a list of all enrolled devices with their compliance and enrollment status.  
- **Device Actions**: IT admins can perform actions such as **remote wipe, sync, restart, or password reset**.  
- **Integration with Intune**: Devices managed in Entra ID can be linked with Intune for additional security policies and app management.  
- **BitLocker and Security Policies**: Ensures data protection through encryption and security baselines. 
![Screenshot](images/screenshot35.jpg)
##  Device Management  

- Regularly **review device compliance reports** to identify and address security risks.  
- Implement **Conditional Access** to restrict access from noncompliant or unmanaged devices.  
- Use **device cleanup policies** to remove stale or inactive devices.  
- Integrate with **Microsoft Intune** for advanced device management and endpoint security. 


---

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

## 2. Authentication Methods – MFA

### **2.1 Password Protection**
- Use **at least 14 characters** with a mix of **uppercase, lowercase, numbers, and symbols**.
- **Block weak passwords** with **Password Protection**:
  1. Go to **Microsoft Entra admin center** > **Security** > **Password Protection**.
  2. Enable **Enforce custom banned passwords**.
![Screenshot](images/screenshot151.jpg)
### **2.2 Multi-Factor Authentication (MFA) Best Practices**
- **Enforce MFA for all users** via **Security Defaults**.
- **Use Microsoft Authenticator** instead of SMS (Best recommended practices)
- **Enable passwordless authentication** (FIDO2 keys, Windows Hello).
![Screenshot](images/screenshot152.jpg)
### **2.3 Authentication Strength Policy**
1. Go to **Microsoft Entra admin center** > **Security** > **Authentication Methods**.
2. Enable:
   - **Passwordless sign-in** (FIDO2 security keys, Windows Hello).
   - **Strong MFA enforcement** for admin accounts.
3. Save the policy.

---

