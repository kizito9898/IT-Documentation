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
##  Steps:
1. Navigate to the Start Menu → search for **PowerShell**  
2. Right-click and **Run as Administrator**  
3. In PowerShell, run:  
   Import-Module Active Directory
4. Get-Command  (shows Different command to use) to run scripts.
## Creating a New Organizational Unit (OU) with PowerShell

You can create a new OU in Active Directory using this cmdlet:

`New-ADOrganizationalUnit -Name "CentralUnit" -Path "DC=Njikasm,DC=com"`

- `-Name` specifies the OU name
    
- `-Path` specifies the domain structure where it will be create
# Creating More OUs with PowerShell

* Creating Sub OUs inside Central Unit with PowerShell

* Using PowerShell, I created a New User account in Active Directory  
  Using the Cmdlet:

```
```powershell
New-ADUser -Name "Harry Potter" -SamAccountName "hpotter" -UserPrincipalName "hpotter@Njikason.com" -Path "OU=Gryffindor, OU=Student, OU=CentralUnit, DC=Njikason, DC=com" -AccountPassword (ConvertTo-SecureString "Capitolp123" -AsPlainText -Force) -Enabled $true -ChangePasswordAtLogon $true
```
- Created another User account (Hermione Granger) using the same script.
---
# Get-ADUser

- `Get-ADUser` is used to retrieve information about a User account in Active Directory (AD) and also properties like email, groups, account information.
---
# Adding Email Address to a User

- Adding email address to the user Harry Potter on PowerShell:
    
`Set-ADUser -Identity "hpotter" -Email "harry.potter@njikason.com" -OfficePhone "800-555-7777"`

---
- ## Disable account with PowerShell:
    
`Set-ADUser -Identity "hgranger" -Enabled $false`

- ## To enable the account again:
    

`Set-ADUser -Identity "hgranger" -Enabled $true`


# Resetting Password with PowerShell on Active Directory

* Navigate to PowerShell and type:

```powershell
Set-ADAccountPassword -Identity "hpotter" -Reset -NewPassword (ConvertTo-SecureString "Capitolp123" -AsPlainText -Force)

```

- Then prompt for the user to change their password at the next logon:
    

`Set-ADUser -Identity "hpotter" -ChangePasswordAtLogon $true`

The password has been changed.

---
# Unlocking a User Account in Active Directory

- Navigate to PowerShell → open as Administrator → type:
    
`Unlock-ADAccount -Identity "hpotter" Unlock-ADAccount -Identity "hgranger"`

---
# Creating a Group (Security Group) Using PowerShell

- In PowerShell type:
`Add-ADGroupMember -Identity "Quidditch Players" -Members "hgranger"`
---
# Creating Another User with PowerShell

- Created another user account **Ron Weasley** using PowerShell and added to Gryffindor group OU with created password


# Automation in powershell:

### Automation in powershell is the process of writing Scripts to perform repetitive IT tasks without manual efforts. Instead of clicking through GUI (Active Directory users & Computers) you use powershell Cmdlets to Script the process once and re-use it many times.

 As other Learning administration, makes it easy to get work done faster, avoid repetitive task which leads to burn-out.
 
 Powershell can interact with active Directory, Azure, Office 365 SQL, VMware, AWS etc.

 ## Creating a new student account using Automation in powershell.
 
 My Current setup: Directory Setup OU = CastelData, Under it
 
I Want to Run an Automation Script that Creates multiple Organizational Unit (OU) for Slytherin, Ravenclaw and Hupplepuff. -> Each OU will have its student as the Script will Create new Users as well.

 What This Script Does
   - breaks up the OU Creation under
   OU = Student, OU = centralUnit, DC = Njikason, DC = Com.

1. if not, it Creates it

2. Loops through each house (Gryffindor, Slytherin, Ravenclaw, Hupplepuff)

3. Creates Students in each OU with:
   - SamAccountName = first initial + last name (Eg: hpotter, dmalfoy)
   - UPN / Email = Same format + @Mydomain.com
   - Default Password: Welcome123! (forces password change at logon)

* After running the Script, my Active-Directory looks like this. Newly Created accounts.
* To Test it Even further, I logged in as Draco malfoy, changed the new password. Account is ready.

 Creating new Users with CSV-driven automation in powershell
* What is a CSV file for AD User Creation
   - CSV (Comma-Separated Values) is a simple text file where data is arranged in columns separated by commas.
* Each row in the CSV = One User you want to Create. -> Each Column (header) = a property for the User account (Eg Name, Username, Password, OU)

This file is a blueprint for Powershell. Instead of Creating Users one by one, you load the CSV, loop through each row and Powershell Creates the account Automatically.

