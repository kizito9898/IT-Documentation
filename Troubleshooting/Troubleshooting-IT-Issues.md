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
## Shared Folder Access Issues

### User Can't Access Team Folder on File Share
- User raised a ticket: "I can access my personal folder but can't access my team's folder on our file share."
- Reached out to get more information on the name and path of the team folder the user is trying to access.
![Screenshot](images/screenshot454.jpg)
- Got a response: The user needs access to the **F: drive** (department folder).
- Replied back: “I need approval and will request for one immediately.”
![Screenshot](images/screenshot455.jpg)
- Confirm access approval via **finance department manager** (keep the approval document).
### Granting Access via File Server
- Identify the security group via **File Server**:
  - Right-click the shared folder → Properties → Security tab → Note the group name.
![Screenshot](images/screenshot482.jpg)
- Open **Active Directory Users & Computers**, search the user (e.g., Rick Berkle):
  - Right-click → Properties → Go to the *Member Of* tab → Add to the security group.
![Screenshot](images/screenshot511.jpg)
- Reached out to the user to try logging off and back in.
![Screenshot](images/screenshot488.jpg)
- Access confirmed by the user.
![Screenshot]
---
## Unable to Access the Shared Folder

- User reported: "Unable to access the shared folder, please provide access."
- Reached out to the user:
  - Ask a couple of questions to know if they had access to the folder before, the folder name, and the full directory path if available.
## HR Folder Access Issue

### Access Denied Error
- User reported: Access denied when trying to open the HR folder. The user needs access.
- Replied back and reached out to the **HR department**, seeking approval to grant access to **David Miller** to access HR folders.
- Sent an email: He has been added (**NTFS permissions**) to access the folder.
- User confirms access and everything is fine.
- Updated the ticket notes and closed the ticket.
---
## Outlook Crashes on Launch

### Description
- User reports: "Outlook crashes when I open it, but the web version works fine."
- Reached out for support, asked the user to connect to their workstation to find the root cause.
- Initiated a remote session with the user (email or TeamViewer), watched out for any prompt to connect to their session.
---
### Solution
- Press `Windows + R` → Type `outlook.exe /safe` → Press Enter.
- Outlook opens in **Safe Mode**, indicating the issue is likely due to an **add-in** or **profile**.
- Go to: Outlook → File → Options → Add-Ins → Click "Go" (at the bottom of the window).
- Ask the user which add-ins are unnecessary → Remove them all.
- User logged off and back in. Outlook seems to be working fine.
## Outlook Issue - Additional Steps

- Also tried to repair Office installation.
- Closed the TeamViewer session → Session ended.
- Sent an email to the user to confirm Outlook is working before closing the ticket.
- Issue resolved.
---
## Internet Intermittency Issue
### Reported By: Emma Baker
- User reported having issues with the internet.
- Connection drops or becomes unstable at random times.
### Common Causes Considered
- Weak Wi-Fi signal.
- Faulty Ethernet cable.
- ISP issues.
- Network adapter.
### Troubleshooting Steps

- Reached out to user via HaloPSA, trying to get more information before troubleshooting.
- User said it’s only affecting her, and she is the only one using the connection.
- Instructed the user to reboot her system (and check any backup app). Sometimes a reboot solves the problem.
- To isolate the problem, instructed her to try connecting with her phone. 
  - If it works fine, then it's the computer.
  - If not, then it's the internet service.

- User reported still not working after reboot.

- Since I couldn’t remote in, I had to guide the user through some simple network commands.

### Steps Provided to User

1. On your keyboard, press `Windows + R`.
2. Then type `cmd` and press Enter.
3. In the command prompt, type:
   - `ipconfig /release`
   - `ipconfig /renew`
This should correct and assign a new IP address.
4. Close out of the Command Prompt.
5. Please test in the web browser and see if you can access the internet.
### User Response

- User confirmed: "Oh! It's working. Looks like it was not working before because the IP address was not valid."
6. Asked the user to reboot the computer and verify everything is working fine.
7. Initiated a remote session and confirmed everything is working fine.
8. Thanked the user for being patient throughout the process and documented everything.

### Issue: Help Connection Seems Slow

- User reported help connection seems slow, webpages are taking a long time to load.
- Reached out to the user to ask a few questions to understand more about the problem.
- User reported they tried rebooting and still getting slow connection.
- Replied to initiate a remote session and troubleshoot.
- Troubleshot the issue, did the following:
  - Recreated the problem
  - `ipconfig /release` & `renew`
  - Enabled and disabled network adapter
  - Confirmed network signal
  - The group user confirmed
- Updated the ticket note.

---
### Issue: Slow Computer

- User reached out to support about slow computer issue and marked it urgent.
- Reached out to the user, empathized, and requested a remote session to take a closer look.
- Initiated a remote session with the user (call), remoted into the computer.
- Entered the Task Manager:
  - Found background consuming high resource
  - Disabled unnecessary startup apps
  - Cleaned temporary files on the C: drive
- Ran malware scan and ensured Windows is updated.
- Emailed the user and updated my ticket note.

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
