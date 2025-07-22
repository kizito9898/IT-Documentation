## RDP (Remote Desktop Protocol) & TeamViewer

### What is Remote IT Support?

- Remote IT support is the process where IT professionals connect to a user's computer or system over the internet or network to:
  - Troubleshoot issues
  - Install software
  - Configure settings
  - Provide technical assistance without being physically present
---
### Remote Support Tools

- **TeamViewer** and **AnyDesk** are tools used in IT to remote into and manage user computers.
---
### Setting up TeamViewer

- Installing TeamViewer (desktop client) on:
  - Host machine
  - Windows 11 (running in VMware Pro)
---
### Enabling Remote Desktop on Windows 11

1. Go to **This PC**
2. Right-click → **Properties**
3. Scroll down to **Remote Settings**
4. Log in with admin rights
5. Enable remote support and turn it on.
---
### Downloading TeamViewer

- Go to the TeamViewer website → Download the free version
- Install TeamViewer → Sign up using support email → Download & sign in with email
---
### Testing Remote Support with TeamViewer

- Already downloaded TeamViewer on the host machine
- On my lab for Windows 11:
  - I downloaded TeamViewer (free version)
  - Selected **Receive Support**
  - Downloaded **QuickSupport**
  - Opened **TeamViewer Receive Support**
## Providing Remote Support via TeamViewer

### Assisting a User with TeamViewer

- As an IT Support, it is essential to know how to guide a user to download and install TeamViewer or open it if it’s already installed.
---
### Creating a Session from the Host Machine

- On my host machine, I created a session → `134 938 340`
- The user needs to type in the session code to connect remotely  
  or share their ID and password from TeamViewer to the support technician.
---
### File Transfer & Remote Control

- I connected to the Windows 11 machine.
- From the top menu → **File & Extras**, I can move files from my PC to the remote computer.
---
### Basic Network Troubleshooting

- Performed:
  - `ipconfig /all` on the remote computer
  - Ping test → `ping 8.8.8.8`
---
### Example IT Tasks

- I can troubleshoot:
  - Printer issues (spooler queues, install software, etc.)
  - Network/device configuration
---
### Ending a Session

- To close the session, click on **End Session**
- You can also search devices, groups, and contacts to connect to.
---
### Joining with Session Code (From User Side)

- The user adds the given session code
- Verify the user (on the user side)
- Now I have control. Same thing applies after session closes.

---

### File Transfer Logs

- On the client machine, you can see the files transferred over during the session.
