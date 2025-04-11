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
