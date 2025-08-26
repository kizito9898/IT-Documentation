# Active Directory (PowerShell)

## Overview
PowerShell Active Directory refers to the use of the Active Directory module for Windows PowerShell to manage and automate tasks in Microsoft Active Directory.  

It uses PowerShell commands (cmdlets) to perform operations such as:
- Creating, modifying, and deleting users and computers  
- Managing groups and organizational units  
- Resetting passwords and unlocking accounts  
- Querying Active Directory for information (e.g., last logon times, group membership)  
- Automating bulk changes across multiple objects  

---

## Getting Started
To work with PowerShell in Active Directory, you need to import the module to get the commands for Active Directory automation.  

### Steps:
1. Navigate to the Start Menu → search for **PowerShell**  
2. Right-click and **Run as Administrator**  
3. In PowerShell, run:  
   ```powershell
   Import-Module ActiveDirectory
### Checking Commands

To view available commands:

`Get-Command`

---

## Creating a New Organizational Unit (OU) with PowerShell

You can create a new OU in Active Directory using this cmdlet:

`New-ADOrganizationalUnit -Name "CentralUnit" -Path "DC=Njikasm,DC=com"`

- `-Name` specifies the OU name
    
- `-Path` specifies the domain structure where it will be created
    

`---  Would you like me to also add **examples for creating users and groups** (since they’re often paired with OU creation in Tier 1/2 AD tasks)? That way your Obsidian note will be more complete.`