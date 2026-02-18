## 1. Introduction

**HubSpot Ticketing System** is a core component of the Service Hub designed to help teams record, organize, and track customer issues in a shared inbox.

It serves as a central repository for all support requests, ensuring that no customer issue falls through the cracks. Because it is integrated with the HubSpot CRM, agents have a full view of the customer's history, including:

- Contact details (Name, Company, Location).
    
- Past conversations and emails.
    
- Previous ticket history.
    

**Goal:** To prioritize, manage, and resolve tickets efficiently while improving customer satisfaction and agent productivity.

---

## 2. Getting Started & Dashboard

This section covers the initial setup and navigation within a Demo or Live environment.

### The Home Dashboard

The dashboard provides a high-level overview of the support landscape.

- **Ticket Overview:** Displays metrics such as _Total Open Tickets_, _Tickets Closed Today_, and _Average Response Time_.
    
- **Pipelines:** Visual representation of tickets moving through different stages (e.g., New > Waiting on Customer > Closed).
    

### Views & Filtering

Understanding "Views" is critical for managing workflow.

- **All Open Tickets:** A master list of every unresolved issue in the system.
    
- **Unassigned:** Tickets that have come in (via email, form, or chat) but have not yet been picked up by an agent.
    
- **Assigned to Me:** Your personal queue of tickets that you are responsible for resolving.
    

---

## 3. IT Support Technician Workflow

As an IT Support Technician, your primary responsibility is to manage the lifecycle of a ticket from arrival to resolution.

### Step 1: Access & Triage

1. **Sign In:** Log in to the HubSpot portal.
    
2. **Check Unassigned Queue:** Navigate to **Service > Tickets** and select the "Unassigned" view.
    
3. **Assign Ticket:**
    
    - Click on a ticket to preview the issue.
        
    - Change the **Ticket Owner** property to your name. This moves the ticket to your "Assigned to Me" view and prevents other agents from working on it simultaneously.
        

### Step 2: Response & Management

Once a ticket is claimed, you must work within the Service Level Agreement (SLA).

- **Review Context:** Look at the CRM card on the right side of the screen to see who the user is and if they have reported similar issues before.
    
- **Respond:** Use the reply editor to send an email back to the user.
    
    - _Tip: You can use "Snippets" or "Templates" for common answers to save time._
        
- **SLA (Service Level Agreement):**
    
    - Watch for the **SLA Timer** on the ticket. This indicates how much time you have left to send a "First Response" or "Close" the ticket based on company policy (e.g., 4 hours for high priority).
        
- **Update Status:**
    
    - If you are waiting for the user to reply, change the status to **"Waiting on Customer"**.
        
    - If you are actively working on it, change the status to **"In Progress"**.
        

### Step 3: Escalation

If you cannot resolve the issue yourself:

1. **Internal Note:** Add a _Note_ (yellow tab) to the ticket explaining what you have tried so far. This is internal-only and the customer will not see it.
    
2. **Reassign:** Change the **Ticket Owner** to a Tier 2 agent or your manager.
    
3. **Update Status:** Change the ticket status to **"Escalated"** (if available) or leave it as "In Progress."
    

### Step 4: Closing the Ticket

When the issue is resolved:

1. **Final Communication:** Ensure the customer has confirmed the fix.
    
2. **Change Status:** Update the ticket status to **"Closed"**.
    
3. **Ticket Properties:** Fill out any required closing fields (e.g., "Resolution Type" or "Root Cause") to aid in future reporting.
    

---

## 4. Ticket Sources (How Tickets are Created)

Tickets enter the system through multiple channels:

- **Email:** When a user emails the support address (e.g., _support@company.com_), a ticket is auto-created.
    
- **Forms:** Support forms on the company website.
    
- **Manual Creation:** If a user walks up to your desk or calls, you manually click **"Create Ticket"** in the top right corner and log the details.
    