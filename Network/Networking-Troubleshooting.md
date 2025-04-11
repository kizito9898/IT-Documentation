# Network Troubleshooting Guide for IT Support

## Initial Troubleshooting Checklist

1. **Ask the user**:
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
