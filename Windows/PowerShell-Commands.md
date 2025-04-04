#  PowerShell Cheat Sheet for IT Support (Beginner Friendly)

---

##  1. Getting Help

Displays help about PowerShell commands:

```powershell
Get-Help
```

Shows help info for a specific command:

```powershell
Get-Help Get-Service
```

Displays usage examples for a command:

```powershell
Get-Help Get-Service -Examples
```

---

##  2. Getting Commands and Modules

Lists all available PowerShell commands:

```powershell
Get-Command
```

Shows currently loaded modules:

```powershell
Get-Module
```

Lists all installed PowerShell modules:

```powershell
Get-Module -ListAvailable
```

Loads the Active Directory module:

```powershell
Import-Module ActiveDirectory
```

---

## 🖥️ 3. System Information

Displays the computer name:

```powershell
hostname
```

Shows detailed system info:

```powershell
Get-ComputerInfo
```

Legacy command for system summary:

```powershell
systeminfo
```

Retrieves OS information via WMI:

```powershell
Get-WmiObject win32_operatingsystem
```

Displays system manufacturer, model, and memory info:

```powershell
Get-WmiObject Win32_ComputerSystem
```

Lists all running processes:

```powershell
Get-Process
```

Lists all Windows services:

```powershell
Get-Service
```

---

## 🌐 4. Network Troubleshooting

Pings a remote host:

```powershell
Test-Connection google.com
```

Displays IP address configuration:

```powershell
Get-NetIPAddress
```

Legacy IP configuration command:

```powershell
ipconfig
```

Lists network adapters:

```powershell
Get-NetAdapter
```

Tests DNS resolution:

```powershell
Resolve-DnsName google.com
```

---

## 👥 5. User Management

### 🧍 Local Users

Lists all local users:

```powershell
net user
```

Gets domain user account information:

```powershell
net user username /domain
```

### 🧑‍💼 Active Directory Users (Requires AD Module)

Retrieves a user from Active Directory:

```powershell
Get-ADUser username
```

Retrieves all properties of a user:

```powershell
Get-ADUser username -Properties *
```

Changes the title attribute of a user:

```powershell
Set-ADUser username -Title "Support Technician"
```

Unlocks a locked AD account:

```powershell
Unlock-ADAccount -Identity username
```

Enables a user account:

```powershell
Enable-ADAccount -Identity username
```

Disables a user account:

```powershell
Disable-ADAccount -Identity username
```

Resets a user's password:

```powershell
Set-ADAccountPassword -Identity username -Reset -NewPassword (ConvertTo-SecureString "NewPassword123" -AsPlainText -Force)
```

---

## ☁️ 6. Microsoft 365 (Requires MSOnline or ExchangeOnline Module)

### 🔐 Connect to Services

Connects to Microsoft 365 (MSOnline module):

```powershell
Connect-MsolService
```

Connects to Exchange Online:

```powershell
Connect-ExchangeOnline
```

### 👥 User and Mailbox Management

Lists all Microsoft 365 users:

```powershell
Get-MsolUser
```

Resets a Microsoft 365 user’s password:

```powershell
Set-MsolUserPassword -UserPrincipalName user@domain.com -NewPassword "Password123" -ForceChangePassword $true
```

Lists mailboxes:

```powershell
Get-Mailbox
```

Sets primary and alias email addresses:

```powershell
Set-Mailbox user@domain.com -EmailAddresses "SMTP:user@domain.com","smtp:alias@domain.com"
```

---

## 📁 7. File and Folder Management

Lists files and folders:

```powershell
Get-ChildItem
```

Recursively lists files/folders in a directory:

```powershell
Get-ChildItem -Path "C:\Users" -Recurse
```

Copies a file:

```powershell
Copy-Item -Path "C:\file.txt" -Destination "D:\Backup\file.txt"
```

Moves a file:

```powershell
Move-Item -Path "C:\file.txt" -Destination "D:\file.txt"
```

Deletes a file:

```powershell
Remove-Item -Path "C:\file.txt"
```

Creates a new folder:

```powershell
New-Item -Path "C:\NewFolder" -ItemType Directory
```

---

## ⚙️ 8. Service Management

Gets all services:

```powershell
Get-Service
```

Checks the status of Windows Update service:

```powershell
Get-Service -Name wuauserv
```

Starts a service:

```powershell
Start-Service -Name wuauserv
```

Stops a service:

```powershell
Stop-Service -Name wuauserv
```

Restarts a service:

```powershell
Restart-Service -Name wuauserv
```

---

## 🔄 9. Windows Updates (Requires PSWindowsUpdate Module)

Checks for Windows updates:

```powershell
Get-WindowsUpdate
```

Installs all available updates and restarts automatically:

```powershell
Install-WindowsUpdate -AcceptAll -AutoReboot
```

---

## 📋 10. Event Logs

Shows the latest 20 system log entries:

```powershell
Get-EventLog -LogName System -Newest 20
```

Shows the last 10 application error logs:

```powershell
Get-EventLog -LogName Application -EntryType Error -Newest 10
```

---

## 💽 11. Disk and Storage

Shows drive info and free space:

```powershell
Get-PSDrive
```

Lists volume info:

```powershell
Get-Volume
```

Shows physical disk details:

```powershell
Get-Disk
```

Lists all partitions:

```powershell
Get-Partition
```

---

## 🔧 12. Process Management

Shows all running processes:

```powershell
Get-Process
```

Stops a specific process:

```powershell
Stop-Process -Name "notepad"
```

Starts a program:

```powershell
Start-Process -FilePath "notepad.exe"
```

---

## 🧹 13. Miscellaneous

Clears the PowerShell screen:

```powershell
Clear-Host
```

Shows command history:

```powershell
Get-History
```

Starts recording the session to a log file:

```powershell
Start-Transcript -Path "C:\PowerShellLog.txt"
```

Stops the recording session:

```powershell
Stop-Transcript
```

---

## 🧭 14. Common Aliases

| Alias | Equivalent      |
| ----- | --------------- |
| `ls`  | `Get-ChildItem` |
| `cd`  | `Set-Location`  |
| `pwd` | `Get-Location`  |
| `cp`  | `Copy-Item`     |
| `mv`  | `Move-Item`     |
| `rm`  | `Remove-Item`   |
| `cat` | `Get-Content`   |

---

## ✅ Pro Tip

Use `Tab` to autocomplete and `Ctrl + C` to stop a running command.

---
