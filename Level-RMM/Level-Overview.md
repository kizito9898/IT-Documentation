# Level RMM & Automation

## What is Level RMM?
Level is a modern RMM platform that helps IT professionals, MSPs, healthcare and education institutions manage devices remotely.  
![Screenshot](images/screenshot702.jpg)
It is designed with a focus on Automations, Remote Control, patch management, Monitoring & Alerting, Scripting, and Security — all in one platform.  
It keeps it simple and easy to use, saves thousands of hours, and allows management from anywhere in the world.
![Screenshot](images/screenshot703.jpg)

## Key Features
- **Automation**: Level uses automations to handle repetitive tasks quickly and improve operational efficiency.  
![Screenshot](images/screenshot704.jpg)
- **Remote Control**: Gain complete, seamless control over any operating system, all from the convenience of your web browser.  
- **Inventory**: Effortlessly track and monitor every device in your network from anywhere at any time.  
- **Background Management**: Diagnose and troubleshoot problems without disrupting the end-user.  
- **Monitoring & Alerting**: Proactive real-time monitoring with alerting and automatic remediation for increased stability.  
- **Patch Management**: Keep your endpoints up-to-date and protected with streamlined patch management.  
- **Security Features**: Mandatory 2FA, IP restrictions, role-based access control.  
# Getting Started with level

* ### level gives you 14 days free trial to learn everything about it or book a demo. Already signup & getting started.

  **Overview of level dashboard.
  - Devices : This is for all the devices created when you install new agent (Favorites, New devices, Ungrouped & grouped devices)
  - Automations : Supercharge Workflow and handle repetitive tasks.
  - Policies -> Reporting -> Updates -> Alerts.
![Screenshot](images/screenshot799.jpg)
---

**Install new agents on Windows 10 Machine
* click on the Install new agent 
![Screenshot](images/screenshot707.jpg)
* Install new monitoring agent (Select the operating system from the list. Site for Windows macOS, Linux) -> Download Installer or One line Command Using Powershell Command.  
  Run Powershell as an administrator and Run the following Command.
![Screenshot](images/screenshot708.jpg)
![Screenshot](images/screenshot706.jpg)
- Added a new machine to level platform its a new installed Agent.
![Screenshot](images/screenshot705.jpg)
![Screenshot](images/screenshot722.jpg)

## Installing new agent server for my Windows Server 2022. 

  Checked on the Install new agent -> One-Line Command -> Opened the powershell Command.  
* Run powershell as an admin 
![Screenshot](images/screenshot711.jpg)
* Paste the Command line -> Easy Install with my API already there -> click on Install (within Sec) I'm done.  
![Screenshot](images/screenshot712.jpg)
![Screenshot](images/screenshot714.jpg)
* Now I can manage Server 2022 from my level account
---

Add another agent using the Same process on a Windows 11 Device.

* Run powershell as admin -> Run the Script.  
* Once it’s done it immediately appears on the dashboard to manage.  
![Screenshot](images/screenshot716.jpg)
![Screenshot](images/screenshot718.jpg)
![Screenshot](images/screenshot719.jpg)
![Screenshot](images/screenshot720.jpg)

---
Adding a **Linux operating System to my level RMM platform to manage.  

 I used Install new agent, Yes Selecting Linux and Copied the One-line Command to linux (Ubuntu terminal) using Sudo to update and then paste the Command. Easy & Fast.  
 ![Screenshot](images/screenshot724.jpg)
 ![Screenshot](images/screenshot725.jpg)

 I’m controlling 4 devices from one platform.  
![Screenshot](images/screenshot728.jpg)

---
# Grouping

* Grouping is very important to keep the devices you manage structured and easy to run automation on them.  
* Tools to group devices.  
* On the left Side click on ➕ Create a group -> Enter the group name -> Confirm.  
![Screenshot](images/screenshot729.jpg)
* Create a Sub group to Add devices or Categorize the Windows, macOS and Linux.  
![Screenshot](images/screenshot730.jpg)
* Adding Devices to groups -> click on the device -> Navigate to Actions -> Assign to group -> Choose a group -> Then Assign to group.  

# Managing Devices on Level (Devices)

* One of the Key features of level is managing devices, having all the details of a System, from getting the Security Score -> CPU, memory Disk -> Uptime -> IP address.

* System -> gives you everything or information about the operating system.  

* Manage -> Run command like ipconfig /all -> get IP address -> Private IP -> File Explorer (See what’s inside of the device) -> Process, what’s Running in the devices, memory, CPU etc. -> and Sensors.  

* Applications -> displays every application Running on the device.  

* Get updates -> Download & Install Updates from the device & prompts to Reboot device.  

* Monitor -> Monitor the performance of a device (BSOD, CPU monitor, Windows uptime Exceeds 30days) -> check out for warning and patches on the device.  

* Manage -> Select many devices you can Run a shutdown, Restart, Install Updates or Run Scripts.  

# Remote Control using level.io

* #### level provides remote Control & Support for any kind of devices from Windows, MacOS, Linux & Raspberry Pi anytime & Anywhere.  

* Using Remote Control  
  -> Navigate to the machine you want to Remote Into  
  -> Click on the device -> on top Right -> click on the Remote logo -> for remote Control -> Connecting  

* Now in remote Control I’m remoting into the System already.
# Notes

- It’s a P2P Connection meaning all data stays private, and never touch Level Internal Server.  
- By the side, I can easily see the System Information, Run Command, See the C: drive and others. 
- I can Run a short Shut down & Restart.  

- You can easily tap on the on the Devices → All devices → click on the devices → Remote Connection gets initiated.  

- I Remoted into every device.  

- Ubuntu → Remote Control Support is in the works but the terminal works really fine.  

- Windows Server 2022 → Remote Control Support on Server 2022, System Information and also ran terminal Command too.  

- **Reporting**  
  Gain returnable insights about my Endpoints.  

- Shows total devices flagged & maintenance endpoints, OS Distribution and Online devices.  
