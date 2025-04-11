# DHCP

## What is DHCP?

**DHCP (Dynamic Host Configuration Protocol)** is a network protocol that automatically assigns IP addresses and other network settings (such as Subnet Mask, Gateway, and DNS) to devices on a network.

## DHCP Server?
A **DHCP Server** is a device (usually a router or Windows Server) that manages IP address allocation dynamically. Instead of manually assigning static IP addresses to every device, the DHCP server automatically provides them based on predefined rules.

## Installing DHCP Server

1. Go to **Server Manager** → **Manage** (click on it) → **Add Roles & Features**  
2. Before you begin → **Next** → **Role-based or Feature-based Installation** → **Next**  
3. Select **Destination Server** as default → **Next**  
4. Click on **DHCP Server** (Add Features) → **Next** → **Confirmation**  
5. Click **Install**
### Post Installation

- Go to **Flag icon** → **Post-deployment Configuration** → **Complete DHCP Configuration**
# DHCP Pool Configuration

**DHCP Pool – Install Configuration**  
→ Description → Next  
(Select User’s Credentials) and Commit  

**Go to Tools and click on DHCP**

- Create a Scope (A Scope is a range of IP addresses assigned to Computers requesting a dynamic IP address)  
- Right on IPv4 → New Scope → Next → Scope Name (Name whatever Scope)  
  → Add a description → IP address Range  
# DHCP Pool Configuration

**DHCP Pool – Install Configuration**  
→ Description → Next  
(Select User’s Credentials) and Commit  

**Go to Tools and click on DHCP**

- Create a Scope (A Scope is a range of IP addresses assigned to Computers requesting a dynamic IP address)  
- Right on IPv4 → New Scope → Next → Scope Name (Name whatever Scope)  
  → Add a description → IP address Range  
# DHCP Pool Configuration

**DHCP Pool – Install Configuration**  
→ Description → Next  
(Select User’s Credentials) and Commit  

**Go to Tools and click on DHCP**

- Create a Scope (A Scope is a range of IP addresses assigned to Computers requesting a dynamic IP address)  
- Right on IPv4 → New Scope → Next → Scope Name (Name whatever Scope)  
  → Add a description → IP address Range  

# DHCP Pool Configuration

**DHCP Pool – Install Configuration**  
→ Description → Next  
(Select User’s Credentials) and Commit  

**Go to Tools and click on DHCP**

- Create a Scope (A Scope is a range of IP addresses assigned to Computers requesting a dynamic IP address)  
- Right on IPv4 → New Scope → Next → Scope Name (Name whatever Scope)  
  → Add a description → IP address Range 
Start IP address: 192.168.15.20  
End IP address: 192.168.15.70
- It’s going to reserve 50 IP addresses  
- Length (3d) or (16) recommended 24  
- Subnet mask: 255.255.255.0  

**Add Exclusions and Delay**  
- Exclude IP address for existing systems (Ex: IP address for a printer)  
- Type in the Start IP address and End IP address and click add  

**Lease duration**  
(The lease duration specifies how long a client can use an IP address from this Scope)  
Put in Days, Hours & Minutes you want IP address to last on a Computer → Next  

**Note**: For security reasons (Select 4 hours so it changes)



pgsql

CopyEdit