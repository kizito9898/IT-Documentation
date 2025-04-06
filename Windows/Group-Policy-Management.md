# Group Policy

**Group Policy (GPO)** is a tool in Windows that helps IT administrators control and configure multiple computers in a network. It allows them to set rules and settings for users and computers without having to configure each one manually.

---

## How It Works

- **Group Policy Objects (GPOs)** contain the rules and settings.
- GPOs are linked to **Active Directory (AD)** and applied to users or computers.
- When a user logs in or a computer starts, it checks for policies and applies them.

---

## How to Locate Group Policy Management

1. Navigate to **Server Manager** → **Tools** → **Group Policy Management**.
2. Click on **Forest** → **Domains** → Right-click on **Domain**.
3. Select **Create a GPO in this domain**.
4. 

---

## Create a GPO (e.g., for Password Policy)

- Setting a password policy to enforce strong passwords and enhance security.

**Example:**
- Name: `Password Policy`
- Click **OK** and right-click to configure settings.
