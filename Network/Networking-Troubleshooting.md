
# Network Troubleshooting

A **network** is a group of two or more devices (like computers, servers, printers, or phones) that are connected together to share resources and communicate.

---

## How to Diagnose Issues for Network Troubleshooting

### What is Ping and How to Ping a Network

- **Ping** is a command used to check if your computer can communicate with another device (like a website or a router).

#### Steps:
1. Open **Command Prompt** (Press `Windows + R`, type `cmd` and press Enter).
2. Common ping tests to check network connectivity:
   - `ping google.com` or `ping 8.8.8.8`
   - `ping [your default gateway]` (to reach your router)
   - `ping 127.0.0.1` (Check your computer’s network loopback)
![Screenshot](images/screenshot138.jpg)

---

## Tracert (Trace Route)

- `tracert` (short for **trace route**) shows the path that data takes from your computer to a destination, like reaching a particular website.
#### Steps:
1. Open **Command Prompt**.
2. Type: `tracert google.com`
![Screenshot](images/screenshot139.jpg)
- It shows a list of hops (routers) the data passes through.
- If a website is slow or not loading, `tracert` shows **where the slowdown is happening**.
---
# What is ipconfig and How to Use it for Network Troubleshooting

**ipconfig** is a Windows command that shows your computer’s network settings, such as:
- IP address
- Subnet mask
- DNS server
- Default gateway
## How to Use ipconfig

### Basic Command
- Open **Command Prompt**.
- Type: `ipconfig`  
  - This shows your basic IP information.
!
### Detailed Info
- Type: `ipconfig /all`  
  - Shows detailed info like:
    - MAC address
    - DHCP status
    - DNS suffix

---

## Troubleshooting APIPA (Automatic Private IP Address)

- If your IP address falls within the range:
  - `169.254.1.0` to `169.254.254.255`  
  - This is called an **APIPA address**, which means **no internet access**.

### Solution
1. Run command: `ipconfig /release`
2. Then: `ipconfig /renew`  
   → This will request a new IP address from the router.

---

## Disable & Enable Network Adapter (Reset a Network Adapter)

1. Go to **Search** and type: `Control Panel`
2. Navigate to:  
   `Network & Internet` → `Network & Sharing Center` →  
   `Change adapter settings`
3. Right-click your Wi-Fi or Ethernet adapter.
4. Click **Disable**
5. Wait a few seconds, then click **Enable** again.



6. **Ask the user**:
   - Is the issue only affecting them or multiple people?

2. **Check physical connections**:
   - Is the device connected to Wi-Fi or Ethernet?
   - Is the network cable plugged in properly?
   - Is the switch/router powered and functioning?

3. **Run `ipconfig`**:
   - Open Command Prompt and type:
     ```
     ipconfig /all
     ```
   - Check:
     - IPv4 Address
     - Default Gateway
     - DNS Servers
     - Is there an IP or "Media disconnected"?

4. **Run `ping` tests**:
   - Loopback (tests local stack):
     ```
     ping 127.0.0.1
     ```
   - Default Gateway:
     ```
     ping [Gateway IP]
     ```
   - Google DNS (tests internet connectivity):
     ```
     ping 8.8.8.8
     ```

5. **Run `nslookup`**:
   - Test DNS resolution:
     ```
     nslookup google.com
     ```
   - If this fails, DNS may be the issue.

6. **Run `tracert`**:
   - Trace where the connection fails:
     ```
     tracert google.com
     ```
   - Check which hop fails—could indicate a routing or ISP issue.

7. **Reset Network Adapter**:
   - Disable/Enable the adapter:
     - Control Panel > Network and Sharing Center > Change Adapter Settings
     - Right-click > Disable > wait > Enable

8. **Swap DNS to Google**:
   - Go to: Control Panel > Network Adapter > Properties > IPv4
   - Use custom DNS:
     ```
     Preferred DNS: 8.8.8.8
     Alternate DNS: 8.8.4.4
     ```

9. **Update Network/Wi-Fi Drivers**:
   - Go to Device Manager > Network Adapters
   - Right-click the adapter > Update Driver
   - Or download latest from manufacturer’s website

10. **Restart Router/Modem**:
   - Power cycle router (off for 30 seconds, then on)
   - Wait for internet light to stabilize

---

## If All Steps Fail — What’s Next?

11. **Check if it’s a system-wide issue**:
   - Are other users affected?
   - If yes, possible **ISP or network hardware failure**
   - Check ISP status page or escalate to network team

12. **Try static IP configuration**:
   - Manually set IP address, Gateway, and DNS
   - If it works, the issue might be with the DHCP server

13. **Safe Mode with Networking**:
   - Boot into Safe Mode
   - If network works, the issue could be a:
     - Firewall
     - Antivirus
     - Third-party app conflict

14. **Check for ARP conflicts / MAC filtering**:
   - Run:
     ```
     arp -a
     ```
   - Look for duplicate IPs or MAC filtering on router

15. **Try alternate network**:
   - Connect to mobile hotspot or another Wi-Fi
   - If successful, issue is likely with original network

16. **Check Event Viewer**:
   - Go to: Event Viewer > Windows Logs > System
   - Filter for logs related to:
     - DHCP
     - DNS
     - Network Adapter
     - TCP/IP

17. **Escalate to Network/Admin Team**:
   - Provide:
     - Results of ping, ipconfig, tracert, nslookup
     - Event log info
     - All steps already taken

18. **Document Everything**:
   - In your ticketing system:
     - What was reported
     - What tests you ran
     - Results of each test
     - Final decision (resolved/escalated)
     - Attach screenshots or logs if needed

---
## Tools Used

- `ipconfig`
- `ping`
- `tracert`
- `nslookup`
- Event Viewer
- Device Manager
- Network Adapter settings

---
## Notes

- IPv4 is most commonly used; IPv6 is newer but not always supported on all systems.
- Google Public DNS: 8.8.8.8 and 8.8.4.4
- Loopback address: 127.0.0.1
