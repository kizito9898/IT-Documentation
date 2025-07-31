## IT Troubleshooting & Common Issues

- Troubleshooting steps used to solve IT issues, helping users stay productive whether it’s password reset issue, account lock-out, computer doesn’t work.
- Knowing how to troubleshoot is very important and a success factor in any IT career.
---
## Troubleshooting IT Issues

### Locked Account - User Cannot Log In
- User reached out support that account has been locked and can’t log in.
![Screenshot](images/screenshot447.jpg)
![Screenshot](images/screenshot436.jpg)
- Receive the ticket, head over to **Active Directory Users & Computers**:
  - Find → Type in user log-in name → Account →  
![Screenshot](images/screenshot437.jpg)
  - Unlock account: check the box, then apply and OK.
![Screenshot](images/screenshot438.jpg)
- Confirm: The account has been unlocked.
![Screenshot](images/screenshot440.jpg)
![Screenshot](images/screenshot448.jpg)
![Screenshot](images/screenshot449.jpg)

---
### Password Reset - User Forgot Password
- User needs a password reset and can’t log in.
- Reach out to the user → Verify identity → Ask for user log-in details.
- Navigate to **Active Directory**:
  - Right-click on the domain → Click on *Find*
  - Entire directory → Type the name →
![Screenshot](images/screenshot441.jpg)
  - Right-click → Reset password → Provide a temporary password
  - Check “User must change password at next logon” → OK.
![Screenshot](images/screenshot442.jpg)
![Screenshot](images/screenshot443.jpg)

- User logs in with the new password after changing it.
![Screenshot](images/screenshot444.jpg)
![Screenshot](images/screenshot445.jpg)

---
### Outlook Crashing When Sending Email
- Outlook keeps crashing when opened and trying to send an email.
- Web version works fine.
- Outlook wasn’t properly set up on the user’s workstation:
  - Log out and sign in again.
- Another fix:
  - Check the email and account to see if an account created for emails
  - Go to the search bar and type email & account, add a work or school account. This should fix the problem.
![Screenshot](images/screenshot446.jpg)
---


---
## Unable to Access the Shared Folder

### User: David Miller

- User reported: "Unable to access the shared folder, please provide access."
- Reached out to the user to get a better understanding of the problem.
![Screenshot](images/screenshot519.jpg)
- Asked a few questions such as:
  - "Have you accessed the folder before?"
  - "Which shared folder do you need access to?"
- User replied that he had access before but can't find it now.
- Identified the folder as the Finance network drive.
![Screenshot](images/screenshot520.jpg)
### Resolution Steps

- Reached out to the user to remote in and map the network drive to restore access.
- Navigated to the file server:
  - `This PC > Local Disk C: > FinanceNetworkDrive`
  - Right-click on the folder → Properties → Sharing → Got the network path
- Remoted into the user's computer:
  - Opened File Explorer
  - Right-clicked → Map Network Drive → Entered network path
![Screenshot](images/screenshot516.jpg)
- Email sent to the user to confirm access was restored and the user was satisfied.
![Screenshot](images/screenshot518.jpg)
![Screenshot](images/screenshot515.jpg)

- Updated my ticket note
![Screenshot](images/screenshot521.jpg)
![Screenshot](images/screenshot522.jpg)

---
## Issue: User Unable to Access Team File Share

### User: Rick Benzle

- User reported: "I can access my personal folder, but can't access my team's folder on the file share."
![Screenshot](images/screenshot523.jpg)
- Reached out to the user to confirm access is denied when trying to open the folder.
![Screenshot](images/screenshot529.jpg)
- User replied: "I do get access denied. I contacted HR and told my manager. I need access now."
- Called the manager and got approval (confirmed by me).
![Screenshot](images/screenshot530.jpg)
### Resolution Steps

- Navigated to the target folder on the file server:
  - `\\Server2022\HR \Team Files`
  - Right-clicked the folder → Selected Properties → Navigated to the Security tab
  - Clicked Edit → Added the user's name and granted appropriate permissions
![Screenshot](images/screenshot524.jpg)
  - Clicked Apply and saved changes
![Screenshot](images/screenshot525.jpg)
- Reached out to the user and asked them to check again.
![Screenshot](images/screenshot531.jpg)
- User confirmed access to the team folder.
![Screenshot](images/screenshot526.jpg)
![Screenshot](images/screenshot528.jpg)

- Updated my ticket note and closed the ticket.
![Screenshot](images/screenshot532.jpg)
---
## Outlook Crashes on Launch

- User reports: "Outlook crashes when I open it, but the web version works fine."
- Reached out for support, asked the user to connect to their workstation to find the root cause.
![Screenshot](images/screenshot462.jpg)
- Initiated a remote session with the user (email or TeamViewer), watched out for any prompt to connect to their session.
![Screenshot](images/screenshot463.jpg)
### Solution
- Press `Windows + R` → Type `outlook.exe /safe` → Press Enter.
- Outlook opens in **Safe Mode**, indicating the issue is likely due to an **add-in** or **profile**.
- Go to: Outlook → File → Options → Add-Ins → Click "Go" (at the bottom of the window).
- Ask the user which add-ins are unnecessary → Remove them all
![Screenshot](images/screenshot308.jpg)
- User logged off and back in. Outlook seems to be working fine.
## Outlook Issue - Additional Steps
- Also tried to repair Office installation.
- Closed the TeamViewer session → Session ended.
- Sent an email to the user to confirm Outlook is working before closing the ticket.
- Issue resolved.
![Screenshot](images/screenshot464.jpg)
---
## Internet Intermittency Issue
### Reported By: Emma Baker
- User reported having issues with the internet.
- Connection drops or becomes unstable at random times.
### Common Causes Considered
- Weak Wi-Fi signal.
- Faulty Ethernet cable.
- ISP issues.
- Network adapter
- Reached out to user via HaloPSA, trying to get more information before troubleshooting.
![Screenshot](images/screenshot465.jpg)
- User said it’s only affecting her, and she is the only one using the connection.
- Instructed the user to reboot her system (and check any backup app). Sometimes a reboot solves the problem.
![Screenshot](images/screenshot470.jpg)

### User Response

- User confirmed: "Oh! It's working. Looks like it is working now , My system hasn't been rebooted for a while now.
![Screenshot](images/screenshot471.jpg)
- Initiated a remote session and confirmed everything is working fine.
- Thanked the user for being patient throughout the process and documented everything.

### Issue: Help Connection Seems Slow

- User reported help connection seems slow, webpages are taking a long time to load.
- Reached out to the user to ask a few questions to understand more about the problem.
![Screenshot](images/screenshot491.jpg)
- User reported they tried rebooting and still getting slow connection.
- Replied to initiate a remote session and troubleshoot.
![Screenshot](images/screenshot492.jpg)
- Troubleshot the issue, did the following:
  - Recreated the problem
  - `ipconfig /release` & `renew`
![Screenshot](images/screenshot467.jpg)
![Screenshot](images/screenshot468.jpg)
  - Enabled and disabled network adapter
  - Confirmed network signal
  - The user confirmed network strength has improved
![Screenshot](images/screenshot493.jpg)
- Updated the ticket note.
![Screenshot](images/screenshot494.jpg)
---
### Issue: Slow Computer

- User reached out to support about slow computer issue and marked it urgent.
![Screenshot](images/screenshot495.jpg)
- Reached out to the user, empathized, and requested a remote session to take a closer look.
![Screenshot](images/screenshot500.jpg)
- Initiated a remote session with the user (call), remoted into the computer.
![Screenshot](images/screenshot501.jpg)
- Entered the Task Manager:
  - Found background consuming high resource
![Screenshot](images/screenshot496.jpg)
  - Disabled unnecessary startup apps
![Screenshot](images/screenshot498.jpg)
  - Cleaned temporary files on the C: drive
  - Adjust for best performance on the advanced setting on settings
![]
- Ran malware scan and ensured Windows is updated.
![Screenshot](images/screenshot499.jpg)
- Emailed the user and updated my ticket note.
![Screenshot](images/screenshot502.jpg)
![Screenshot](images/screenshot503.jpg)
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
![Screenshot](images/screenshot312.jpg)
---
## Add to Group (Project Design)

- Right-click on the user → Properties → Member Of  
  Search for the group and add the user → Apply
![Screenshot](images/screenshot313.jpg)
---
## Shared Drive Access

- If access is needed to **Project Design**,  
  Add to the corresponding AD group that maps to the share  
  Add to local PC, connect to the system, and map the drive.
![Screenshot](images/screenshot314.jpg)
## Email Group / Teams

- I will go in and add the user to the necessary groups and Microsoft Teams.  
  (To receive emails, onboarding process, and the rest)
---

## Net User  / Domain 

`net user RickB /domain`

- Shows **detailed information** about the domain user 
    
    - Account status (active/locked)
        
    - Group memberships
        
    - Last password change and expiration
![Screenshot](images/screenshot533.jpg)
![Screenshot](images/screenshot534.jpg)
## Microsoft Excel Issues
### Scenario:
User submits a ticket that Excel won’t open or crashes when opening a file.
### Steps:
- Reach out to the user (empathy) → Ask the following:
  - Is it happening with a specific file or all files?
  - Try opening Excel in Safe Mode:  
    Press `Win + R` → Type `excel /safe` → Enter
### Disable Add-ins
- File → Options → Add-ins  
- At the bottom, manage → COM Add-ins → Go → Uncheck all  
- Restart and see if it solves the problem
## Repair Office
- Go to Control Panel → Programs → Installed Apps  
- Find Microsoft 365 or Office → Modify → Quick Repair  
  - If it didn’t solve the issue, do Online Repair
- Install **SARA** Repairs from Microsoft and run a quick repair
