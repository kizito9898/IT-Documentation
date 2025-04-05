# How to Get Started with Windows Server 2022 (Hands-on)

- **What is Windows Server** 
Windows Server is a special version of Windows made for businesses to help manage computers, users and networks. Unlike Windows 10 or 11, which people use for personal tasks, Windows Server is designed for IT professionals to control and organize company systems.  
Windows Servers (like file, backup, company systems) — IT system. Keeps everything running smoothly.

- Various Versions of Windows Server  
Windows Server 2003, 2008 & R2, 2012 & R2, 2016, 2019 and 2022.
![Screenshot](images/screenshot01.jpg)
- **Windows Server Uses**  
Manage users & computers (Active Directory)  
Shares & Security across a folder  
DNS & Other Services - Helps Computers find each other on a Network  
Virtual machines on one server  

- **Network**  
- Active Integration (Remote Desktop Services)  
- Group Policy (GPO): Control Settings for multiple Computers  
- WMI (Windows Management Instrumentation)  
- Firewall Rules and Software Restrictions

# Setting up Windows Server 2022 on a Virtual Machine

1. **Download VirtualBox or VMware Workstation Pro**
   - Download Windows host (for Windows) & Extension Pack
   - Download VMware Workstation Pro on the official website (Browser)
     *(32 or 64bit depending on your computer)*  
   - **Download Windows Server 2022 ISO file** *(Free trial 180 days)*
![Screenshot](images/screenshot02.jpg)
---

2. **Open your Workstation and click on Create a New Virtual Machine**
   - Click on Typical *(Recommended)* ➝ Installer disc image file *(Browse the Downloads folder on your PC and click on the ISO file you just downloaded)*  
   - Guest Operating System *(Windows)*  
   - Name the Virtual Machine ➝ Specify Disk capacity *(by default it's 80GB)* ➝ Ready to Create Virtual Machine and Finish

---

- **Once the Virtual Machine is Created**, click on **Edit Virtual Settings** ➝ CD/DVD (SATA) ➝ Use ISO Image file *(Browse to your downloaded ISO file)* and Select and OK
![Screenshot](images/screenshot54.jpg)
---

3. **Power on the Virtual Machine**
   - During the booting process, quickly press any key to boot from CD or DVD to load the ISO.  
     If you miss it, shut it down and power again. Keep pressing any key to boot.

## Installing Windows Server 2022

- The ISO file will prompt Server operating system setup. Click on **Next** ➝ **Install Now**
- Select the operating system you want to install  
  *(Windows Server 2022 Standard Evaluation - Desktop Experience)* ➝ **Next** ➝ Accept terms & conditions ➝  
  Custom: Install Microsoft Server operating system only ➝  
  Installing Microsoft Server operating system...
![Screenshot](images/screenshot03.jpg)
### After Installing
- **Username**: administrator *(only default)*
- **Password**:  
- **Re-enter Password**

---

### 3. Renaming the Server to Something Simple

- Navigate to **File Explorer** ➝  
  Right click on **This PC** ➝ **Properties** ➝ **Advanced System Settings** ➝  
  Computer Name tab ➝ Click **Change** ➝ Enter new computer name *(e.g., Server2022)* ➝  
  Click **OK** (it will prompt to restart the machine) ➝  
  **Restart Now**
![Screenshot](images/screenshot04.jpg)
---

### 4. Create Active Directory Domain Services

- Navigate to **Server Manager** from the **Start Menu** ➝  
  On the top right, click **Manage** ➝ **Add roles and features**
![Screenshot](images/screenshot05.jpg)
**Before you begin:**
1. Open **Server Manager**.
2. Click **Next**.
3. Select **Role-based or feature-based installation**.
4. Click **Next**.
5. Click on **Active Directory Domain Services**.
6. Click **Add Features**.
7. Click **Next**, then **Install** (wait for it to succeed).
8. Click **Promote this server to a domain controller**.
9. Select **Add a new forest**.
10. Enter the **Root domain name** (e.g., `Njikason.com`).
11. Create a password (e.g., `Password@123`).
12. Click **Next**.
13. Wait for **Prerequisites check**.
14. Click **Install** — it will restart your computer.

> **Note:** Active Directory Users & Computers are now installed in the server.

---

## Creating a Static IP for Server 2022

1. In the search bar, type **Control Panel**.
2. Go to **Network and Internet**.
3. Click **View network status and tasks**.
4. Click **Change adapter settings**.
5. Right-click **Ethernet** > Select **Properties**.
6. Click on **Internet Protocol Version 4 (TCP/IPv4)**.
7. Select **Use the following IP address** and configure the static IP.
![Screenshot](images/screenshot59.jpg)
> In a **corporate environment**, Windows Server usually has a **static IP address**.

---

## VM Network Configuration

- Change the **virtual machine network** from **NAT** to **Host-only** so that the **VM** can talk to each other on the same network.
![Screenshot](images/screenshot06.jpg)

---

## Adding a Computer to a Domain (Windows to a Linux) rules

* To enforce/practice with Windows Server (group policy, Active Directory users & Computers, Troubleshooting Skills )

* If it's a new install, for home lab (Renaming the PC will be easy to remember the Computer)  
Click on the Active File Explorer → Properties → change Settings → Computer name → Rename the Computer → Restart the Computer
![Screenshot](images/screenshot60.jpg)

---

* Navigate to your Control panel → Search & type Control Panel → View network status & tasks → change adapter
Settings → Ethernet → Properties → Disable IPv6 → Click on (TCP/IPv4) → Use the following IP address and click ok  
Use ping command to try and reach your Windows Server
![Screenshot](images/screenshot61.jpg)


---

* **Now join the Computer to the Domain**  
Click on the File Explorer → Right click on This PC → Properties → Domain or Workgroup (Win 11) → Advance Settings (Win10) → member of Domain  
administrator *username* (capitalp123) and password  
The Computer has been joined to the domain

---

* Logged in with the account (username) I created on Active Directory and now i can manage this account, reset password, disable account & apply group policies to the Computer.

---


