# Printer Setup on Server 2022

Printers are often set up on servers in business environments for centralized management. It allows IT administrators to manage all network printers from a single location, monitor them, and troubleshoot issues.

---
## Setting up a Print Server on Windows Server

1. Open **Server Manager**
2. Go to **Add roles & features**
3. Select **Role-based or feature-based installation**
4. Choose the **Server**
5. Under **Server Roles**, select:
   - **Print and Document Services**
6. Add required features
7. Under **Role Services**, select:
   - **Print Server**
8. Confirm and Install

---
## On the Server Manager:

Navigate to:  
**Tools → Print Management → Print Servers → Server 2022 (Local)**
### Components:
- **Drivers**:  
  Software that allows the server to communicate with different printer models.
- **Forms**:  
  Predefined paper sizes and layouts (e.g. A4, A3).
- **Ports**:  
  Lists printer ports, which determine how printers connect to the server.
- **Printers**:  
  This section displays all installed and shared printers, including their status (Online, Offline, or Experiencing Errors).
