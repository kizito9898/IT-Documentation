## 1. Introduction

**HubSpot Ticketing System** is a core component of the Service Hub designed to help teams record, organize, and track customer issues in a shared inbox.

It serves as a central repository for all support requests, ensuring that no customer issue falls through the cracks. Because it is integrated with the HubSpot CRM, agents have a full view of the customer's history, including:

- Contact details (Name, Company, Location).
    
- Past conversations and emails.
    
- Previous ticket history.
**Goal:** To prioritize, manage, and resolve tickets efficiently while improving customer satisfaction and agent productivity.
![Screenshot](images/screenshot902.jpg)

---
# Communication

- Communication (responding and giving solutions to problems).  
- Using internal notes to document technical steps, actions taken & professional attitude towards ticket priority.  
- Follows Escalation Process → If I can’t resolve it, put in internal notes & escalate to tier 2.  
- Knowledge Base → is very important to search for solutions & contribute to most re-occurring issues and document solutions.  
---
# Creating New Ticket in HubSpot

- Navigate to help desk and click on + to create ticket.  
- Fill in the ticket name → ticket status as New → Ticket description of what the problem is about → then save whether it’s chat, email or phone conversations.  
![Screenshot](images/screenshot905.jpg)
- Priority set → Associate ticket with (the person that called in with the problem) → Companies & create the ticket.  

- Reached out to the client acknowledging that I created a ticket and currently working on it with their ticket reference.  

- I created a template that gets sent to the client when they contact support team so that they know we got the email and working on it, rather than keeping them on loops.  

- Ticket is being set at Waiting on us, or waiting on contact 
![Screenshot](images/screenshot910.jpg)
---
# CIPP Troubleshooting & Support Scenarios

## Case Study 1: Tenant Sync Failure (Error 500)

### 1. Issue Description

**Symptom:** A user reports that specific tenants are missing users in the dashboard, or data is not populating. **Error Message:** The user later confirms receiving an **API Error 500** (Internal Server Error) when trying to load tenant data.
![Screenshot](images/screenshot909.jpg)
### 2. Initial Triage & Investigation

Upon receiving the ticket, the following standard checks were advised:

- **GDAP Relationship Status:** Is the relationship still active in the Microsoft Partner Center?
    
- **Role Mapping:** Are the correct roles (e.g., _Global Reader_, _User Administrator_) mapped to the CIPP security groups?
    
- **Standard Sync:** Has the user attempted a manual "Tenant Sync" within CIPP?
![Screenshot](images/screenshot911.jpg)

When the issue persisted, I requested:

- Specific tenant details (Tenant ID or Name).
    
- Screenshots of the error message to confirm the specific API failure code.
![Screenshot](images/screenshot912.jpg)
### 3. Root Cause Analysis

**Diagnosis:** **Expired GDAP (Granular Delegated Admin Privileges).**

- **Technical Explanation:** CIPP relies on the Microsoft Graph API to fetch user data. When GDAP expires, the Service Principal no longer has permission to read the data. The API call returns a `null` or `403 Forbidden` response, which the CIPP frontend often interprets and displays as a generic "500 Internal Server Error."
    
### 4. Resolution

**Action Taken:** Guided the user to the **Onboarding Wizard** for permission remediation.

- **Step 1:** Navigate to **Tenant Administration** > **Onboarding Wizard**.
    
- **Step 2:** Locate the affected tenant.
    
- **Step 3:** Re-run the **Permissions Check** and **GDAP Check**.
    
- **Step 4:** If prompted, re-consent to the application permissions. This refreshes the Service Principal’s access tokens.
**Outcome:** The "Missing Users" populated immediately after the wizard completed. **Status:** Ticket Closed.
![Screenshot](images/screenshot914.jpg)
![Screenshot](images/screenshot913.jpg)

---
## Case Study 2: System Slowness & Performance

### 1. Issue Description

**Symptom:** The user reports significant lag when navigating menus or loading data. **User Statement:**

> "My account is running slow since I opened/logged into my instance. I have rebooted my PC and the issue still persists."

### 2. Investigation

- **Client-Side Check:** The user rebooted their workstation, ruling out local RAM/CPU issues.
![Screenshot](images/screenshot915.jpg)
### 3. Root Cause Analysis

**Diagnosis:** **Azure Function "Cold Starts."**

- **Technical Explanation:** CIPP is built on a "Serverless" architecture using **Azure Functions**. To save costs, Azure "spins down" (turns off) the backend resources when they are not being used.
    
    - **Cold Start:** When a user logs in after a period of inactivity (e.g., first thing in the morning), Azure must physically "spin up" the server to process the request. This can cause a 10–30 second delay on the first few clicks.
        
    - **Warm State:** Once the server is running, subsequent clicks are fast.
![Screenshot](images/screenshot916.jpg)
### 4. Resolution

**Action Taken:** Educated the user on Azure hosting behavior.

- **Explanation:** "Since CIPP is a self-hosted app on Azure, what you are experiencing is likely a 'Cold Start.' The backend goes to sleep to save you money on hosting costs. The initial slowness is the system waking up."
    
- **Verification:** Asked the user to click through 3–4 menus rapidly. The user confirmed that after the initial lag, the speed returned to normal.
    
- **Outcome:** Issue resolved by user education; no technical fix required.


## Case Study 3: Sponsorship Access & GitHub Linking (403 Errors)

### 1. Issue Description

**Symptom:** A managed service provider (MSP) sponsored the CIPP project using their corporate GitHub Organization account but could not access the "Sponsor-Only" features or deployment portal. **User Statement:** _"I just sponsored. This is my username for GitHub. Add a manual to log into the management portal."_
![Screenshot](images/screenshot917.jpg)
### 2. Investigation & Constraint

- **Constraint:** The CIPP management portal uses GitHub OAuth for authentication.
    
- **The Problem:** You cannot "log in" as a GitHub Organization (e.g., `@MyMSPCompany`). You must log in as an individual user (e.g., `@JohnDuprey9898`).
    
- **Error:** The system saw the Organization as the sponsor, but the individual user (`JohnDuprey9898) had no entitlement linked, resulting in a **403 Forbidden** error.
    
![Screenshot](images/screenshot918.jpg)
### 3. Resolution

**Action Taken:**

- **Manual Linking:** Accessed the backend entitlement database and manually linked the user’s personal GitHub username (`JohnDuprey9898`) to the corporate Organization's Sponsor ID.
    
- **User Instruction:** Replied to the ticket instructing the user to log out and log back in. The system now recognizes their personal account as a valid seat under the corporate sponsorship.
    
- **Status:** Ticket Closed.
![Screenshot](images/screenshot919.jpg)
---

## Case Study 4 : "Out of Date" Warning After Update

### 1. Issue Description

**Symptom:** The user performed a CIPP update via the backend, but the dashboard continued to display a red banner saying "Version Out of Date." **User Statement:** _"I updated my CIPP. It is showing it is out of date. How can I resolve this?"_

### 2. Root Cause Analysis

**Diagnosis:** **Aggressive Browser Caching.** CIPP (v7+) relies heavily on client-side JavaScript. When the backend updates, the user's browser (Chrome/Edge) often holds onto the _old_ version of the `.js` and `.css` files to speed up loading. The browser essentially "thinks" it is still running the old version, even though the server is updated.
![Screenshot](images/screenshot920.jpg)

### 3. Resolution

**Action Taken:**

- **Hard Reload Instruction:** Instructed the user that a standard "Refresh" button click is insufficient.
    
    - **Chrome/Edge:** Press `F12` to open Developer Tools -> Right-click the Refresh icon -> Select **"Empty Cache and Hard Reload"**.
        ![Screenshot](images/screenshot921.jpg)
    - **Firefox:** Click the padlock icon -> Clear Cookies and Site Data.
        
- **Expectation Setting:** Noted that in rare cases involving Azure CDNs, global propagation can take up to 48 hours, but the "Hard Reload" usually fixes it instantly.
    
- **Result:** User confirmed the banner disappeared.
![Screenshot](images/screenshot922.jpg)
---
## Case Study 5: Tenant Access Denied (Invalid Grant)

### 1. Issue Description

**Symptom:** A user could manage most clients but was locked out of one specific tenant. **Error Code:** The user provided a screenshot showing an **Invalid Grant (AADSTS50076)** error when trying to perform actions.

![Screenshot](images/screenshot923.jpg)
### 2. Initial Investigation

**Troubleshooting Steps Provided:**

1. **Refresh:** Instructed the user to manually trigger a Tenant Refresh from CIPP.
    
2. **Permissions Check:** Asked the user to verify their CIPP application permissions.
    
3. **GDAP Verification:** Checked the GDAP relationship status in the Partner Center.
    
4. **Access Check:** Ran the "Permissions Check" tool within CIPP.
    
![Screenshot](images/screenshot924.jpg)
### 3. Root Cause Analysis

**Diagnosis:** **Expired or Revoked Refresh Token.** The "Invalid Grant" error typically indicates one of three things:

1. The user's password was changed recently.
    
2. The user's account is blocked by a Conditional Access policy (e.g., an MFA challenge).
    
3. The admin consent (GDAP permissions) was revoked or expired.
![Screenshot](images/screenshot930.jpg)
### 4. Resolution

**Action Taken:**

- **Generate New Relationship:** Instructed the user to create a new GDAP relationship using a template that specifically includes **write permissions** (e.g., _Exchange Administrator_ + _User Administrator_).
    
- **Result:** The user confirmed access was restored immediately after recreating the relationship with the correct permissions.
![Screenshot](images/screenshot925.jpg)

![Screenshot](images/screenshot926.jpg)
## Case Study 7: "Access Denied" on Initial Setup (SWA vs. IAM Roles)

### 1. Issue Description

**Symptom:** A user (or myself) completed the deployment of a self-hosted CIPP instance. Upon navigating to the CIPP URL to log in for the first time, they received an **Access Denied** screen. **User Statement:** _"I have added the 'Contributor' role to my account in Azure, but I am still locked out."_
![Screenshot](images/screenshot936.jpg)
### 2. Investigation & Misconfiguration

- **User's Action:** The user followed the "Managed Identity" documentation (which tells you to give the _Function App_ contributor rights) and incorrectly applied that logic to _themselves_. They assigned their personal user account the **Contributor** role on the Resource Group IAM.
    
- **The Problem:** Azure IAM roles (Owner/Contributor) control access to the _Azure Portal resources_, not the CIPP Application itself.
    
- **Root Cause:** CIPP uses **Azure Static Web Apps (SWA)** for authentication. Access to the dashboard is controlled specifically through the **SWA Role Management** blade, not the general Subscription/Resource Group IAM.
    
![Screenshot](images/screenshot944.jpg)
![Screenshot](images/screenshot945.jpg)
### 3. Resolution

**Action Taken:** Referenced the official documentation on **Adding Users and Managing Roles**. To resolve the "Access Denied" error, we must generate an invite link from the Static Web App.

**Steps to Fix:**

1. **Navigate to Azure Portal:** Open the Resource Group hosting CIPP.
    
2. **Select Static Web App:** Click on the resource named `CIPP-SWA-xxxx` (not the Function App).
    
3. **Role Management:** In the left menu, select **Role Management** (sometimes listed under _Settings_).
    
4. **Invite User:**
    
    - Click **Invite User**.
        
    - **Deployment Environment:** `default`
        
    - **Role:** Type `superadmin` (or `admin`).
        
    - **Expiration:** Select an expiration time for the link.
        
5. **Generate & Accept:** Click **Generate**. Copy the link provided and paste it into the browser.
    
6. **Auth:** Sign in with the Microsoft 365 account.
![Screenshot](images/screenshot938.jpg)
The client replied to the email
![Screenshot](images/s)

## What if I get errors while managing my tenants in CPP?

### 1. Perform a CPP Permissions Refresh

a. Navigate to:

   **Settings → CPP → Application Settings**
b. Click on the **Tenants** tab.
c. Click the blue **Refresh** button in the **Actions** column for the relevant tenant. 

---
### 2. Perform Permissions Check 

a. Navigate to:
   **Settings → Application Settings** 
b. Select **Perform Permissions Check**.

---  
### 3. Conduct GDAP Check

a. Navigate to:
   **CPP → Application Settings → GDAP Check**  
b. After completing the Permissions Check, perform the **GDAP Check**.

---
### 4. Perform Access Check
a. Navigate to:
   **CPP → Application Settings → Access Check**
b. Select the relevant tenant and click **Run Access Check**.

Complete all checks for effective troubleshooting.

