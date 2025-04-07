### Azure Functions

Azure Functions is a Serverless Solution that allows you to write less code.  
- When you provision an app service instance it runs (cold) just to start alarm. And you pay for the actual time it's running.

---

### Azure File Storage or Server

Azure Saves up files that you can mount on Windows Server, Linux, macOS, (likes SMB protocol).

---

### Azure VPN

If you want to create a secure connection between a on-premises network and a VNet, then you can use a VPN (Virtual Private Network) connection.  
- A VPN network sends encrypted traffic over the public internet.

---

### Virtual Machine with Azure

**Step 1**  
- Log into Microsoft Azure Services  
- Click on the Virtual Machine  
- Then on Create -> Create Azure Virtual Machines  
- You create a Resource group (A Resource group is a collection of resources that shares lifecycle, permissions and policies)  
- Name the Resource group -> Homelab  
- Instance details -> Virtual machine name -> Server 2019  
- Image (Choose Server 2019 Data Center or Server 2022)

### Administrator Account

**Create Username**: helpdesk  
**Password**: Chigozie798  
- Review & Create (Once the validity is good)  
- Create

---

### After Azure Virtual Machine has been Created, you can login by:

**Using Connect**  
- Download RDP  
- Click on the RDP  
- Then enter your password and login  
  - **Server Name**: DCNY-01

---

### Log into the Windows 10 PC

- Connect  
- Download RDP  
- Click on the downloaded RDP  
- Click Connect  
- Enter password and Connect  

**Rename the PC**  
**Domain Name**: Kestech.local  

**Directory Services Restore Mode (DSRM) Password**:  
- Capital123  

*(Run PowerShell as an administrator)*

---

### Using PowerShell (Creating a new user in Active Directory)

```powershell
PS C:\users\helpdesk> Import-Module activedirectory
PS C:\users\helpdesk> get-command new-aduser
