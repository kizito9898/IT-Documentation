 # IT Troubleshooting 

## 1. Hosts File - Fix Website Access Issues

### GUI Method:
1. Open **File Explorer** and navigate to:
   ```
   C:\Windows\System32\drivers\etc
   ```
2. Right-click **hosts** file → Open with **Notepad (Run as Administrator)**.
3. Remove unwanted entries and **Save**.
4. Restart the browser.

### CMD Method:
```powershell
notepad C:\Windows\System32\drivers\etc\hosts
```
Edit and save the file.

---

## 2. Encryption & BitLocker

### GUI Method:
1. Open **Control Panel > BitLocker Drive Encryption**.
2. Click **Turn on BitLocker** and follow the setup.
3. Save the recovery key in **OneDrive or a USB drive**.

### CMD Method:
```powershell
manage-bde -on C: -password
```

---

## 3. Check Windows Version

### GUI Method:
1. Open **Settings > System > About**.
2. Check **Edition**.

### CMD Method:
```powershell
winver
```

---

## 4. Virus & Malware Removal

### GUI Method:
1. Open **Windows Security > Virus & Threat Protection**.
2. Click **Quick Scan**.

### CMD Method:
```powershell
MpCmdRun -Scan -ScanType 2
```

---

## 5. Fix Internet Connection Issues

### GUI Method:
1. Open **Settings > Network & Internet > Status**.
2. Click **Change Adapter Options**.
3. Right-click **Wi-Fi** → **Disable > Enable**.
4. Click **Network Troubleshooter**.

### CMD Method:
```powershell
ipconfig /release
ipconfig /renew
```

---

## 6. Manage Power Options

### GUI Method:
1. Open **Control Panel > Power Options**.
2. Select **Balanced** or **High Performance**.

### CMD Method:
```powershell
powercfg /setactive SCHEME_MIN
```

---

## 7. Manage Windows Updates

### GUI Method:
1. Open **Settings > Windows Update**.
2. Click **Pause Updates**.

### CMD Method:
```powershell
wuauclt /detectnow
```

---

## 8. Check System Information

### GUI Method:
1. Right-click **Start > System**.
2. Open **Task Manager > Performance Tab**.

### CMD Method:
```powershell
systeminfo
```

---

## 9. Install & Uninstall Applications

### GUI Method:
1. Open **Control Panel > Programs & Features**.
2. Click an app and select **Uninstall**.

### CMD Method:
```powershell
wmic product where name="appname" call uninstall
```

---

## 10. Rename PC & Join a Domain

### GUI Method:
1. Open **Settings > System > About > Rename this PC**.
2. To join a domain: Open **Settings > Accounts > Access Work or School**.

### CMD Method:
```powershell
wmic computersystem where name="%computername%" call rename name="NewPCName"
netdom join %computername% /domain:yourdomain.com /userd:AdminUser /passwordd:*
```

---

## 11. Check Windows Activation

### GUI Method:
1. Open **Settings > System > Activation**.

### CMD Method:
```powershell
slmgr /xpr
```

---

## 12. End Processes

### GUI Method:
1. Press **Ctrl + Shift + Esc** to open **Task Manager**.
2. Right-click a process and select **End Task**.

### CMD Method:
```powershell
taskkill /IM processname.exe /F
```

---

## 13. Check & Fix Disk Errors

### GUI Method:
1. Open **File Explorer > This PC**.
2. Right-click **C: Drive > Properties > Tools > Error Checking > Check**.

### CMD Method:
```powershell
chkdsk C: /f /r
```

---

## 14. Increase Virtual RAM

### GUI Method:
1. Open **Settings > System > About > Advanced System Settings**.
2. Click **Performance Settings > Advanced > Virtual Memory**.
3. Increase the **Page File size**.

### CMD Method:
```powershell
wmic pagefile list /format:list
```

---

## 15. Speed Up a Slow PC

### GUI Method:
1. Open **Task Manager > Startup**.
2. Disable unnecessary startup programs.

### CMD Method:
```powershell
wmic startup where name="appname" call disable
```

---

## 16. Manage Local Users

### GUI Method:
1. Open **Settings > Accounts > Other Users**.
2. Select a user and click **Remove**.

### CMD Method:
```powershell
net user username /delete
```
```
