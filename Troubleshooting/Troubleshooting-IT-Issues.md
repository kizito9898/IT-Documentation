## IT Troubleshooting & Common Issues

- Troubleshooting steps used to solve IT issues, helping users stay productive whether it’s password reset issue, account lock-out, computer doesn’t work.
- Knowing how to troubleshoot is very important and a success factor in any IT career.
---
## Troubleshooting IT Issues

### Locked Account - User Cannot Log In
- User enabled support that account has been locked and can’t log in.
- Receive the ticket, head over to **Active Directory Users & Computers**:
  - Find → Type in user log-in name → Account →  
  - Unlock account: check the box, then apply and OK.
- Confirm: The account has been unlocked.
---
### Password Reset - User Forgot Password
- User needs a password reset and can’t log in.
- Reach out to the user → Verify identity → Ask for user log-in details.
- Navigate to **Active Directory**:
  - Right-click on the domain → Click on *Find*
  - Entire directory → Type the name →  
  - Right-click → Reset password → Provide a temporary password
  - Check “User must change password at next logon” → OK.
- User logs in with the new password after changing it.
---
### Outlook Crashing When Sending Email
- Outlook keeps crashing when opened and trying to send an email.
- Web version works fine.
- Outlook wasn’t properly set up on the user’s workstation:
  - Log out and sign in again.
- Another fix:
  - Check the email and account to see if the account is configured properly.

## New Hire Set-up

### Scenario:
HR Manager submits a ticket asking IT to provision a new user who starts next Monday.
### Steps:
- Open **Active Directory Users & Computers (ADUC)** →  
  Right-click the appropriate OU (New User)

- Enter first name, last name  
  Username (First name with last name)  
  Set user must change password at next login  
  Click Finish
---
## Add to Group (Project Design)

- Right-click on the user → Properties → Member Of  
  Search for the group and add the user → Apply
---
## Shared Drive Access

- If access is needed to **Project Design**,  
  Add to the corresponding AD group that maps to the share  
  Add to local PC, connect to the system, and map the drive.
## Email Group / Teams

- I will go in and add the user to the necessary groups and Microsoft Teams.  
  (To receive emails, onboarding process, and the rest)
---
## Microsoft Excel Issues
### Scenario:
User submits a ticket that Excel won’t open or crashes when opening a file.
### Steps:
- Reach out to the user (empathy) → Ask the following:
  - Is it happening with a specific file or all files?
  - Try opening Excel in Safe Mode:  
    Press `Win + R` → Type `excel /safe` → Enter
---
### Disable Add-ins
- File → Options → Add-ins  
- At the bottom, manage → COM Add-ins → Go → Uncheck all  
- Restart and see if it solves the problem
---
## Repair Office
- Go to Control Panel → Programs → Installed Apps  
- Find Microsoft 365 or Office → Modify → Quick Repair  
  - If it didn’t solve the issue, do Online Repair
- Install **SARA** Repairs from Microsoft and run a quick repair
