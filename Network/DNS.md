# DNS

## What is DNS?

DNS (Domain Name System) is a protocol that translates human-readable domain names (E.g. google.com) into IP addresses (E.g. 142.250.190.78), allowing computers to locate and communicate with each other over the Internet or a private network.

---
## DNS Server

A DNS Server is a computer or network device that stores and manages domain name records and responds to DNS queries by resolving domain names into IP addresses.

---

> **Tip:** Before installing DNS in the server, the server needs to have a static IP address.

- Navigate to the Server Manager → Local Server → on the page that's up → go to `Ethernet0` → click on it → `Ethernet0 Properties`
- Click on **Internet Protocol Version 4 (TCP/IPv4)** → Properties
  - → Use the following IP address (Static IP address)
- Disable **Internet Protocol Version 6 (TCP/IPv6)** and close

---

> If you go back to the Local Server, you will observe the static IP that was just created.
 