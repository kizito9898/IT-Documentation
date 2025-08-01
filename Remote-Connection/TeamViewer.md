
### What is Remote IT Support?

- Remote IT support is the process where IT professionals connect to a user's computer or system over the internet or network to
![Screenshot](images/screenshot336.jpg)
  - Troubleshoot issues
  - Install software
  - Configure settings
  - Provide technical assistance without being physically present.
---
### Remote Support Tools

- **TeamViewer** and **AnyDesk** are tools used in IT to remote into and manage user computers.
---
### Setting up TeamViewer

- Installing TeamViewer (desktop client) on:
![Screenshot](images/screenshot337.jpg)
![Screenshot](images/screenshot338.jpg)

  - Host machine
  - Windows 11 (running in VMware Pro)
![Screenshot](images/screenshot339.jpg)
---
### Enabling Remote Desktop on Windows 11

1. Go to **This PC**
2. Right-click → **Properties**
3. Scroll down to **Remote Settings**
4. Log in with admin rights
5. Enable remote support and turn it on.
![Screenshot](images/screenshot335.jpg)
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

- As an IT Support, it is essential to know how to guide a user to download and install TeamViewer or open it if it’s already installed.
---
### Creating a Session from the Host Machine

- On my host machine, I created a session → `114 161 080`
![Screenshot](images/screenshot340.jpg)
- The user needs to type in the session code to connect remotely  
  or share their ID and password from TeamViewer to the support technician.
![Screenshot](images/screenshot341.jpg)
Now both my windows 10 and 11 from my lab are connected, while windows 10 is the host and 11 the guest.

---
### File Transfer & Remote Control

- I connected to the Windows 11 machine.
- From the top menu → **File & Extras**, I can move files from my PC to the remote computer.
![Screenshot](images/screenshot342.jpg)
![Screenshot](images/screenshot343.jpg)
![Screenshot](images/screenshot351.jpg)

---
### Basic Network Troubleshooting

- Performed:
  - `ipconfig /all` on the remote computer
  - Ping test → `ping 8.8.8.8`
![Screenshot](images/screenshot344.jpg)
---
### Example IT Tasks

- I can troubleshoot:
  - Printer issues (spooler queues, install software, etc.)
  - Network/device configuration
![Screenshot](images/screenshot345.jpg)
![Screenshot](images/screenshot346.jpg)

---
### Ending a Session

- To close the session, click on **End Session**
- You can also search devices, groups, and contacts to connect to.
![Screenshot](images/screenshot347.jpg)
---
### Joining with Session Code (From User Side)

- The user adds the given session code
- Verify the user (on the user side)
- Now I have control. Same thing applies after session closes
- On the client machine, you can see the files transferred over during the session.
![Screenshot](images/screenshot348.jpg)
![Screenshot](images/screenshot349.jpg)
![Screenshot](images/screenshot350.jpg)
