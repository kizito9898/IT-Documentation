#  **PowerShell Cheat Sheet for IT Support** (Beginner Friendly)

PowerShell is a powerful tool that helps IT support teams troubleshoot, manage systems, and automate tasks efficiently. This guide covers the most commonly used commands to help you get started.  

---

##  **1. Getting Help**  

New to PowerShell? Don't worry! You can always ask for help.  

### See general help information:
```powershell
Get-Help
```
This command will show basic information about PowerShell commands.  

### Find out what a specific command does:
```powershell
Get-Help Get-Service
```
Think of this like checking a dictionary for a word’s meaning.  

### See examples of how to use a command:
```powershell
Get-Help Get-Service -Examples
```
If you're unsure how to use a command, this will show real-world examples.  

---

##  **2. Finding Commands and Modules**  

### List all available PowerShell commands:
```powershell
Get-Command
```
This helps you discover what PowerShell can do.  

### Check which modules (toolkits) are loaded:
```powershell
Get-Module
```
Modules contain extra commands for specific tasks.  

### See all installed modules on your system:
```powershell
Get-Module -ListAvailable
```
If you're missing a command, it might be in a module that isn't loaded yet.  

### Load the Active Directory module (for managing users, groups, and computers):
```powershell
Import-Module ActiveDirectory
```
You need this if you're working with users in an organization.  

---

##  **3. Checking System Information**  

### Find out your computer’s name:
```powershell
hostname
```
Useful when connecting to remote systems.  

### Get detailed system information:
```powershell
Get-ComputerInfo
```
This gives a full breakdown of your PC’s specs.  

### Check your Windows version and OS details:
```powershell
Get-WmiObject win32_operatingsystem
```
Helpful when troubleshooting compatibility issues.  

### Find out how much RAM you have and your computer model:
```powershell
Get-WmiObject Win32_ComputerSystem
```
Good for checking if a PC meets software requirements.  

### List all running programs (processes):
```powershell
Get-Process
```
If your PC is running slow, this helps you see what’s consuming resources.  

### List all services (background programs) running:
```powershell
Get-Service
```
If something isn’t working, check if the required service is running.  

---

##  **4. Network Troubleshooting**  

### Test if a website or server is reachable (like using "ping"):
```powershell
Test-Connection google.com
```
If a website isn’t loading, this checks if the issue is on your end.  

### View your computer’s IP address:
```powershell
Get-NetIPAddress
```
Use this when setting up a network or troubleshooting connection issues.  

### See all available network adapters:
```powershell
Get-NetAdapter
```
Helpful for checking if your Wi-Fi or Ethernet is working.  

### Test if a domain name resolves correctly (DNS check):
```powershell
Resolve-DnsName google.com
```
Use this if you have internet but websites don’t load properly.  

---

##  **5. Managing Users (Local & Active Directory)**  

###  Local Users  

### List all user accounts on your computer:
```powershell
net user
```
If you need to check who has access to the PC.  

### View details of a domain user:
```powershell
net user username /domain
```
Useful when checking login issues for domain users.  

###  Active Directory (For IT Support in Organizations)  

### Find a user in Active Directory:
```powershell
Get-ADUser username
```
See if a user exists in the system.  

### View all details about a user:
```powershell
Get-ADUser username -Properties *
```
Useful for troubleshooting access issues.  

### Reset a user’s password:
```powershell
Set-ADAccountPassword -Identity username -Reset -NewPassword (ConvertTo-SecureString "NewPassword123" -AsPlainText -Force)
```
A lifesaver when someone forgets their password!  

### Unlock a locked account:
```powershell
Unlock-ADAccount -Identity username
```
If a user gets locked out, this will let them log back in.  

---

##  **6. Microsoft 365 Management (Requires MSOnline Module)**  

### Connect to Microsoft 365 admin services:
```powershell
Connect-MsolService
```
Required before managing users in Microsoft 365.  

### List all Microsoft 365 users:
```powershell
Get-MsolUser
```
Check if an employee has a valid Microsoft 365 account.  

### Reset a user’s Microsoft 365 password:
```powershell
Set-MsolUserPassword -UserPrincipalName user@domain.com -NewPassword "Password123" -ForceChangePassword $true
```
Very useful for IT support when someone forgets their login.  

### List all mailboxes in Exchange Online:
```powershell
Get-Mailbox
```
Verify if a user has a mailbox assigned.  

---

##  **7. Managing Files and Folders**  

### View files in a folder:
```powershell
Get-ChildItem
```
Think of this as using "ls" in Linux or "dir" in Windows.  

### Copy a file to another location:
```powershell
Copy-Item -Path "C:\file.txt" -Destination "D:\Backup\file.txt"
```
Great for backups.  

### Move (cut & paste) a file:
```powershell
Move-Item -Path "C:\file.txt" -Destination "D:\file.txt"
```
Use this instead of dragging files manually.  

### Delete a file:
```powershell
Remove-Item -Path "C:\file.txt"
```
Be careful—this doesn’t go to the Recycle Bin!  

---

##  **8. Managing Windows Services**  

### Check if a service is running:
```powershell
Get-Service -Name wuauserv
```
(Checks Windows Update service status)  

### Start a service:
```powershell
Start-Service -Name wuauserv
```

### Stop a service:
```powershell
Stop-Service -Name wuauserv
```

### Restart a service:
```powershell
Restart-Service -Name wuauserv
```
If an app isn’t working, restarting its service might fix it.  

---

##  **Pro Tips**  

 Press `Tab` to autocomplete commands.  
 Use `Ctrl + C` to stop a running command.  
To save your session's output, use:  
```powershell
Start-Transcript -Path "C:\PowerShellLog.txt"
