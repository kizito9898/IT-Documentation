## PowerShell

### What is PowerShell?
- A **PowerShell Cmdlet** is a lightweight, single-function command built into PowerShell for performing specific tasks.  
- PowerShell is a **command-line shell** and **scripting language** created by Microsoft.  
- A **shell** means you can type commands (like `ping`, `ipconfig`) but with more advanced capabilities.  
- A **scripting language** means you can write a list of commands in a file (a **script**) so they run automatically instead of typing them one by one.  
![Screenshot](images/screenshot549.jpg)
### Why Use PowerShell?
- With PowerShell scripting, you can:
  - Perform **Active Directory tasks** → Create, disable, or reset 50 user accounts at once.  
  - Handle **Microsoft 365 / Intune tasks** → Assign licenses, reset passwords, configure settings.  
  - Run **system checks** → Pull logs, check disk space, list installed software on 100 machines.  
  - Enable **automation** → Instead of manually patching machines or running updates, script it once and run it everywhere. # Downloading Powershell 7.4.5 

* Go to Microsoft’s official GitHub release page:  
  [https://github.com/powershell/powershell/releases](https://github.com/powershell/powershell/releases)  
  → Under **Assets**, download the **.msi installer** for Windows (x64 bit)  
  → Example: `powershell-7.4.5-win-x64.msi`  
  → Run the installer. ✅  
![Screenshot](images/screenshot550.jpg)
* PowerShell aims to be **cross-platform**, running on **Windows, macOS, and Linux**.  

* Download **Visual Studio Code** to practice PowerShell fundamentals → linked with PowerShell Core.  
![Screenshot](images/screenshot556.jpg)

### Notes
- You can always **download a higher version of PowerShell** if your current version is outdated.

## Variables
* A variable is a **named storage location** for data (string, number, object, etc).  
* Always starts with `$` in PowerShell.  
* Think of it as a **container that stores data you can reuse**.  
![Screenshot](images/screenshot558.jpg)
![Screenshot](images/screenshot559.jpg)
## Alias
* An alias is just a **shortcut (nickname)** for a longer cmdlet, command, or function.  
* It makes typing faster, but the command still runs the **full version** in the background.
![Screenshot](images/screenshot614.jpg)
## Comparison Operators
* In PowerShell, comparison operators are used to **compare values** (numbers, strings, or objects).
![Screenshot](images/screenshot560.jpg)
* They return either **True or False**.  
## Arrays
* An array is just a **list of items** stored in a single variable.  
* Instead of having one value, an array can hold **multiple values at once** (numbers, strings, objects, etc).  
## Hashtable
* A hashtable uses **specific keys**.  
* It is a **data structure** that stores **key–value pairs**.  
## Hashtable Example

`$fellowshipData = @{     Key1 = "Item1"     Key2 = "Item2" }`

A **hashtable** in PowerShell stores data as **key-value pairs**. Keys must be unique, and you can retrieve values by referencing their keys.
## Functions in PowerShell

A **function** in PowerShell is a reusable block of code that you define once and call multiple times.

### Syntax

`function Get-Greeting {     param([string]$Name)     "Hello, $Name! Welcome to PowerShell." }`

### Usage

`Get-Greeting -Name "Kizito"`

Functions help you **avoid repeating long scripts** and make your automation modular.

---

## Using the Ping Command

PowerShell allows you to test network connectivity using `Test-Connection` (instead of legacy `ping`).

`Test-Connection google.com -Count 4`

This sends ICMP echo requests and returns the response time, similar to `ping`.

---
## Creating a New File in PowerShell

`New-Item -Path "C:\Users\User\example.txt" -ItemType File`

Creates a blank text file in the specified path.

- `-Path` specifies the location.
    
- `-ItemType File` ensures it's a file (not folder).

---
## Creating and Saving Command Output to a File

### Example: Save Ping Results

`Test-Connection google.com -Count 4 | Out-File "C:\Users\User\PingResults.txt"`

- `Out-File` saves the output of a command into a text file.
    
- Useful for logging troubleshooting steps.
---
## Delete a File in PowerShell

`Remove-Item -Path "C:\Users\User\example.txt"`

- Deletes the specified file.
    
- Add `-Force` if the file is hidden or read-only.
    
- Add `-Recurse` if deleting a folder with contents.
### Aliases vs Full Cmdlets

- Always prefer **full cmdlets** in scripts (`Remove-Item` instead of `rm`) for readability.
    
- Aliases are good for typing faster interactively.
    
### Cmdlet Naming Convention

PowerShell follows **Verb-Noun** convention:

- `Get-Process`
    
- `Start-Service`
    
- `Stop-Computer`
    

Use `Get-Verb` to see approved verbs.

### Help System

You can always check help:

`Get-Help New-Item -Examples`

### Piping & Redirection

- `|` sends the output of one command into another.
    
- Example:
    

`Get-Process | Sort-Object CPU -Descending | Select-Object -First 5`

Shows top 5 processes by CPU usage.

### Error Handling

Use `Try { } Catch { }` for handling errors gracefully.

`Try {     Get-Item "C:\NonExistentFile.txt" } Catch {     Write-Output "File not found!" }`

--



