
# Network Troubleshooting

A **network** is a group of two or more devices (like computers, servers, printers, or phones) that are connected together to share resources and communicate. Troubleshooting network is essential part of IT support role learning it improves my skills further in networking and troubleshooting steps.

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
![Screenshot](images/screenshot140.jpg)
### Detailed Info
- Type: `ipconfig /all`  
  - Shows detailed info like:
    - MAC address
    - DHCP status
    - DNS suffix
![Screenshot](images/screenshot141.jpg)
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
![Screenshot](images/screenshot142.jpg)
 **Check physical connections**:
   - Is the device connected to Wi-Fi or Ethernet?
   - Is the network cable plugged in properly?
   - Is the switch/router powered and functioning?

. **Run `ipconfig`**:
   - Open Command Prompt and type:
     ```
     ipconfig /all
     ```
   - Check:
     - IPv4 Address
     - Default Gateway
     - DNS Servers
     - Is there an IP or "Media disconnected"?
![Screenshot](images/screenshot505.jpg)
**Run `ping` tests**:

     ```
   - Google DNS (tests internet connectivity):
     ```
     ping 8.8.8.8
     ```

. **Run `nslookup`**:
   - Test DNS resolution:
     ```
     nslookup google.com
     ```
   - If this fails, DNS may be the issue.
![Screenshot](images/screenshot143.jpg)
 **Run `tracert`**:
   - Trace where the connection fails:
     ```
     tracert google.com
     ```
   - Check which hop fails—could indicate a routing or ISP issue.

 **Reset Network Adapter**:
   - Disable/Enable the adapter:
     - Control Panel > Network and Sharing Center > Change Adapter Settings
     - Right-click > Disable > wait > Enable

 **Swap DNS to Google**:
   - Go to: Control Panel > Network Adapter > Properties > IPv4
   - Use custom DNS:
     ```
     Preferred DNS: 8.8.8.8
     Alternate DNS: 8.8.4.4
     ```

 **Update Network/Wi-Fi Drivers**:
   - Go to Device Manager > Network Adapters
   - Right-click the adapter > Update Driver
   - Or download latest from manufacturer’s website

 **Restart Router/Modem**:
   - Power cycle router (off for 30 seconds, then on)
   - Wait for internet light to stabilize
## Network Troubleshooting

### `ipconfig /release`
- This command releases the current IP address assigned to the computer by the DHCP server.
- After running this, the network adapter won't have any IP address assigned.
![Screenshot](images/screenshot467.jpg)
### `ipconfig /renew`
- This command requests a new IP address from the DHCP server.
- Often used after `/release` to refresh the network connection or to fix a bad IP (e.g., 169.xx.x.x).
![Screenshot](images/screenshot468.jpg)
### `ipconfig /flushdns`
- This clears the DNS cache.
- Useful when websites are not loading, wrong sites are loading, or experiencing intermittent network issues.
![Screenshot](images/screenshot490.jpg)
---
### Wi-Fi vs Ethernet

- **Wi-Fi**: Wireless, more convenient, but generally slower and less stable than Ethernet.
- **Ethernet**: Wired connection, faster, more reliable, and better for large transfers or remote work.

---
### IP Addressing

- **Static IP Address**: Manually assigned IP that does not change.  
  - Useful for servers, printers, or devices that need consistent IP addresses.
![Screenshot](images/screenshot506.jpg)
- **Dynamic IP Address**: Automatically assigned by the DHCP server (router).

---
### Email Protocols and Ports

- **SMTP**: Simple Mail Transfer Protocol  
  - Port 25/465 over SSL

- **POP3**: Post Office Protocol Version 3  
  - Port 110/995 over SSL

- **IMAP**: Internet Message Access Protocol  
  - Port 143/993 over SSL
---
## If All Steps Fail What’s Next

12. **Escalate to Network/Admin Team**:
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
## Notes

- IPv4 is most commonly used; IPv6 is newer but not always supported on all systems.
- Google Public DNS: 8.8.8.8 and 8.8.4.4
- Loopback address: 127.0.0.1
