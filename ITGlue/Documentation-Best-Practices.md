# IT Glue - Documentation Best Practices

## 1. Standard Naming Conventions
- Use consistent and clear naming for devices, users, and assets.
- Examples:
  - **Workstations:** `WS-{Location}-{User}` (e.g., `WS-NYC-JDoe`)
  - **Servers:** `SRV-{Function}-{Location}` (e.g., `SRV-DC1-LON`)
  - **Network Devices:** `NET-{Type}-{Location}` (e.g., `NET-FW-NYC`)

## 2. Consistency Guidelines
- Keep documentation **updated** with timestamps.
- Avoid duplicate entries by **searching before adding** new documentation.
- Use **templates** to ensure consistency across documentation.

## 3. Access Control
- Define who can **view/edit** specific documentation.
- Sensitive information (admin credentials) should be securely stored.

## 4. Tagging & Categorization
- Use **standardized tags** to improve searchability (e.g., `Network`, `Server`, `User Accounts`).
- Group related documentation (e.g., all M365-related docs under `Microsoft 365`).

## 5. What to Document
- **Network Infrastructure:** ISP details, VLANs, Subnets, Firewall rules.
- **Server Information:** OS version, IP addresses, roles, backup schedule.
- **User Accounts:** Email accounts, permissions, assigned devices.
- **Software Licenses:** Product keys, renewal dates, assigned users.

---

# IT Glue - Documentation Templates

## 1. **Network Documentation Template**
```yaml
Client Name: XYZ Company  
Network Diagram: [Attach Image]  
Firewall Configurations:
  - Rules: [List firewall rules]
  - NAT Settings: [Details]
  - VPN Settings: [Details]
Wi-Fi SSIDs & Passwords:
  - Main: [SSID / Password]
  - Guest: [SSID / Password]
Subnets & VLANs:
  - VLAN 10 – Workstations (192.168.10.0/24)
  - VLAN 20 – VoIP (192.168.20.0/24)
ISP & Public IP:
  - ISP Name: [Provider]
  - Static IP: [X.X.X.X]

## 2. **Server Documentation Template**
```yaml
Server Name: [Server Name]  
Role: [Domain Controller / File Server]  
IP Address: [192.168.X.X]  
OS & Version: [Windows Server 2019]  
Admin Credentials: [Stored Securely]  
Backup Schedule: [Nightly at 12 AM]  
Notes: [Additional Information]
```

## 3. **User Account Documentation Template**
```yaml
User Name: [Full Name]  
Department: [Department Name]  
Email: [Email Address]  
Assigned Devices:
  - Laptop: [Device Name]
  - Mobile: [Device Name]
Software Licenses:
  - Microsoft 365: [License Type]
  - Adobe: [Version]
  - Other: [Details]
Notes: [Additional user information]
```

These templates ensure **structured, consistent, and efficient documentation**. Let me know if you need any modifications!
