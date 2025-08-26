## PowerShell

### What is PowerShell?
- A **PowerShell Cmdlet** is a lightweight, single-function command built into PowerShell for performing specific tasks.  
- PowerShell is a **command-line shell** and **scripting language** created by Microsoft.  
- A **shell** means you can type commands (like `ping`, `ipconfig`) but with more advanced capabilities.  
- A **scripting language** means you can write a list of commands in a file (a **script**) so they run automatically instead of typing them one by one.  

### Why Use PowerShell?
- With PowerShell scripting, you can:
  - Perform **Active Directory tasks** → Create, disable, or reset 50 user accounts at once.  
  - Handle **Microsoft 365 / Intune tasks** → Assign licenses, reset passwords, configure settings.  
  - Run **system checks** → Pull logs, check disk space, list installed software on 100 machines.  
  - Enable **automation** → Instead of manually patching machines or running updates, script it once and run it everywhere.  

### Key Notes
- An **alias** in PowerShell is a shortcut or alternate name for a cmdlet or command.  
- You can always **download a higher version of PowerShell** if your current version is outdated. 

# Po

* Go to Microsoft’s official GitHub release page:  
  [https://github.com/powershell/powershell/releases](https://github.com/powershell/powershell/releases)  
  → Under **Assets**, download the **.msi installer** for Windows (x64 bit)  
  → Example: `powershell-7.4.5-win-x64.msi`  
  → Run the installer. ✅  

* PowerShell aims to be **cross-platform**, running on **Windows, macOS, and Linux**.  

* Download **Visual Studio Code** to practice PowerShell fundamentals → linked with PowerShell Core.  

---

## Variables
* A variable is a **named storage location** for data (string, number, object, etc).  
* Always starts with `$` in PowerShell.  
* Think of it as a **container that stores data you can reuse**.  

---

## Alias
* An alias is just a **shortcut (nickname)** for a longer cmdlet, command, or function.  
* It makes typing faster, but the command still runs the **full version** in the background.  

---

## Comparison Operators
* In PowerShell, comparison operators are used to **compare values** (numbers, strings, or objects).  
* They return either **True or False**.  

---

## Arrays
* An array is just a **list of items** stored in a single variable.  
* Instead of having one value, an array can hold **multiple values at once** (numbers, strings, objects, etc).  

---

## Hashtable
* A hashtable uses **specific keys**.  
* It is a **data structure** that stores **key–value pairs**.  


