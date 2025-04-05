
## What is Active Directory?

Active Directory (AD) is a Microsoft directory service used in Windows Server environments to manage users, computers, groups, and other network resources.  
It helps organizations:
- Control access to resources  
- Enforce security policies  
- Simplify administration  

---
## Active Directory Domain Services Installation

**Before you begin:**

1. Open **Server Manager**.
2. Click **Next**.
3. Select **Role-based or feature-based installation**.
4. Click **Next**.
5. Click on **Active Directory Domain Services**.
6. Click **Add Features**.
7. Click **Next**, then **Install** (wait for it to succeed).
8. Click **Promote this server to a domain controller**.
9. Select **Add a new forest**.
10. Enter the **Root domain name** (e.g., `mykasm.com`).
11. Create a password (e.g., `Password@123`).
12. Click **Next**.
13. Wait for **Prerequisites check**.
14. Click **Install** — it will restart your computer.

> **Note:** Active Directory Users & Computers are now installed in the server.

---
## Creating a New Account in Active Directory

1. From the **Start Menu**, click on **Windows Administrative Tools**.
2. Go to **Active Directory Users & Computers**.
3. Right-click on **Users**.
4. Scroll down to **New** → **User**.
5. Fill in:
   - User's name  
   - Password (check "User must change password at next login")  
6. Click **Finish**.

---

## Show More Details About a User

If you want more features displayed (like showing more details about a user):

- Right-click on **View** (in the top menu).
- Scroll down to **Advanced Features** and check it.

---

## How to Find a User, Contact, and Groups in Active Directory

1. Navigate to your Domain Controller (e.g., **Njikason**).
2. Right-click on it → Select **Find**.
3. Set the search scope to **Entire Directory** (in case the users or objects are not in the default Users OU).
