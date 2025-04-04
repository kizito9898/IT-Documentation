# PowerShell Cheat Sheet for IT Support (Beginner Friendly)

---

## 1. Getting Help

- `Get-Help`  
  Displays help about PowerShell commands.

- `Get-Help Get-Service`  
  Shows help info for the `Get-Service` command.

- `Get-Help Get-Service -Examples`  
  Shows usage examples.

---

## 2. Getting Commands and Modules

- `Get-Command`  
  Lists all available PowerShell commands.

- `Get-Module`  
  Shows currently loaded modules.

- `Get-Module -ListAvailable`  
  Lists all installed PowerShell modules.

- `Import-Module ActiveDirectory`  
  Loads the Active Directory module.

---

## 3. System Information

- `hostname`  
  Displays the computer name.

- `Get-ComputerInfo`  
  Displays detailed system information.

- `systeminfo`  
  Legacy command for system summary.

- `Get-WmiObject win32_operatingsystem`  
  Retrieves OS info using WMI.

- `Get-WmiObject Win32_ComputerSystem`  
  Shows memory, manufacturer, and model.

- `Get-Process`  
  Lists running processes.

- `Get-Service`  
  Lists all services and their statuses.

---

## 4. Network Troubleshooting

- `Test-Connection google.com`  
  Sends a ping to google.com.

- `Get-NetIPAddress`  
  Displays IP address info.

- `ipconfig`  
  Legacy command to show network info.

- `Get-NetAdapter`  
  Shows network adapter configuration.

- `Resolve-DnsName google.com`  
  Tests DNS resolution.

---

## 5. Users and Active Directory

### Local Users

- `net user`  
  Lists local user accounts.

- `net user username /domain`  
  Gets domain user account info.

### Active Directory (requires AD module)

- `Get-ADUser username`  
  Retrieves user object from AD.

- `Get-ADUser username -Properties *`  
  Shows all AD attributes of the user.

- `Set-ADUser username -Title "Support Technician"`  
  Updates the user's job title.

- `Unlock-ADAccount -Identity username`  
  Unlocks a locked-out user account.

- `Enable-ADAccount -Identity username`  
  Enables a user account.

- `Disable-ADAccount -Identity username`  
  Disables a user account.

- `Set-ADAccountPassword -Identity username -Reset -NewPassword (ConvertTo-SecureString "NewPassword123" -AsPlainText -Force)`  
  Resets the user’s password.

---

## 6. Microsoft 365 (Requires MSOnline or ExchangeOnline Module)

### Connect to Microsoft 365

- `Connect-MsolService`  
  Signs in to Microsoft 365 via MSOnline.

- `Connect-ExchangeOnline`  
  Connects to Exchange Online.

### User Management

- `Get-MsolUser`  
  Lists all Microsoft 365 users.

- `Set-MsolUserPassword -UserPrincipalName user@domain.com -NewPassword "Password123" -ForceChangePassword $true`  
  Resets a user’s password.

- `Get-Mailbox`  
  Lists all mailboxes.

- `Set-Mailbox user@domain.com -EmailAddresses "SMTP:user@domain.com","smtp:alias@domain.com"`  
  Sets primary and alias email addresses.

---

## 7. File and Folder Management

- `Get-ChildItem`  
  Lists files and folders (like `ls`).

- `Get-ChildItem -Path "C:\Users" -Recurse`  
  Recursively lists files/folders.

- `Copy-Item -Path "C:\file.txt" -Destination "D:\Backup\file.txt"`  
  Copies a file.

- `Move-Item -Path "C:\file.txt" -Destination "D:\file.txt"`  
  Moves or renames a file.

- `Remove-Item -Path "C:\file.txt"`  
  Deletes a file.

- `New-Item -Path "C:\NewFolder" -ItemType Directory`  
  Creates a new folder.

---

## 8. Service Management

- `Get-Service`  
  Lists all Windows services.

- `Get-Service -Name wuauserv`  
  Shows Windows Update service status.

- `Start-Service -Name wuauserv`  
  Starts a service.

- `Stop-Service -Name wuauserv`  
  Stops a service.

- `Restart-Service -Name wuauserv`  
  Restarts a service.

---

## 9. Windows Updates (Requires PSWindowsUpdate Module)

- `Get-WindowsUpdate`  
  Checks for available updates.

- `Install-WindowsUpdate -AcceptAll -AutoReboot`  
  Installs all updates and reboots if needed.

---

## 10. Event Logs

- `Get-EventLog -LogName System -Newest 20`  
  Displays the last 20 system logs.

- `Get-EventLog -LogName Application -EntryType Error -Newest 10`  
  Shows the last 10 application errors.

---

## 11. Disk and Storage Info

- `Get-PSDrive`  
  Lists drives and free space.

- `Get-Volume`  
  Displays volume info.

- `Get-Disk`  
  Shows physical disk details.

- `Get-Partition`  
  Lists partitions on all disks.

---

## 12. Process Management

- `Get-Process`  
  Shows all running processes.

- `Stop-Process -Name "notepad"`  
  Kills a process by name.

- `Start-Process -FilePath "notepad.exe"`  
  Launches a program.

---

## 13. Miscellaneous Useful Commands

- `Clear-Host`  
  Clears the terminal screen.

- `Get-History`  
  Shows previously used commands.

- `Start-Transcript -Path "C:\PowerShellLog.txt"`  
  Starts recording your PowerShell session.

- `Stop-Transcript`  
  Stops session recording.

---

## 14. Common Aliases

| Alias | Command         |
| ----- | --------------- |
| `ls`  | `Get-ChildItem` |
| `cd`  | `Set-Location`  |
| `pwd` | `Get-Location`  |
| `cp`  | `Copy-Item`     |
| `mv`  | `Move-Item`     |
| `rm`  | `Remove-Item`   |
| `cat` | `Get-Content`   |

---

## Pro Tip

Use `Tab` to autocomplete command names and parameters, and `Ctrl + C` to stop a running command.

