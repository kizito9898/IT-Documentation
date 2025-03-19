# Microsoft 365 Administration Guide

## 📌 Introduction
Microsoft 365 Admin Center is the central hub for managing users, licenses, security, and services like Exchange, Teams, and SharePoint. This guide provides step-by-step instructions for common administrative tasks.

---

## 🔹 1. Microsoft 365 Admin Center Overview
### Accessing the Admin Center
1. Go to [Microsoft 365 Admin Center](https://admin.microsoft.com).
2. Sign in with an **admin account**.
3. Navigate the left-hand menu:
   - **Users** → Manage users, reset passwords.
   - **Groups** → Create and manage groups.
   - **Billing** → Assign licenses.
   - **Security & Compliance** → Set up MFA, monitor alerts.

---

## 🔹 2. User Management
### 🔹 Create a New User
1. Open **Admin Center** → Click **Users > Active Users**.
2. Click **+ Add User**.
3. Fill in:
   - **Name**: John Doe
   - **Username**: johndoe@yourdomain.com
   - **License**: Microsoft 365 E5
4. Click **Next > Finish**.

✅ **PowerShell Method**
```powershell
New-MgUser -DisplayName "John Doe" -UserPrincipalName "johndoe@yourdomain.com" -MailNickName "johndoe" -PasswordProfile @{ForceChangePasswordNextSignIn=$true}
