# How to Get Started with Windows Server 2022 (Hands-on)

- **What is Windows Server** 
Windows Server is a special version of Windows made for businesses to help manage computers, users and networks. Unlike Windows 10 or 11, which people use for personal tasks, Windows Server is designed for IT professionals to control and organize company systems.  
Windows Servers (like file, backup, company systems) — IT system. Keeps everything running smoothly.

- Various Versions of Windows Server  
Windows Server 2003, 2008 & R2, 2012 & R2, 2016, 2019 and 2022.

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

---

2. **Open your Workstation and click on Create a New Virtual Machine**
   - Click on Typical *(Recommended)* ➝ Installer disc image file *(Browse the Downloads folder on your PC and click on the ISO file you just downloaded)*  
   - Guest Operating System *(Windows)*  
   - Name the Virtual Machine ➝ Specify Disk capacity *(by default it's 80GB)* ➝ Ready to Create Virtual Machine and Finish

---

- **Once the Virtual Machine is Created**, click on **Edit Virtual Settings** ➝ CD/DVD (SATA) ➝ Use ISO Image file *(Browse to your downloaded ISO file)* and Select and OK

---

3. **Power on the Virtual Machine**
   - During the booting process, quickly press any key to boot from CD or DVD to load the ISO.  
     If you miss it, shut it down and power again. Keep pressing any key to boot.

