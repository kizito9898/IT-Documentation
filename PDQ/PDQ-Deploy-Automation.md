# PDQ Deploy

## What is PDQ Deploy?

PDQ Deploy is a remote software deployment tool for Windows environments. It allows you to push software, scripts, patches, and updates to multiple machines simultaneously or on a schedule.

You can see it as your "remote software installer."  
Instead of going from PC to PC, you send out one command and PDQ takes care of the rest.

---

## What Does It Do?

- Silently installs applications (e.g. Chrome, Zoom, Adobe Reader)
- Updates software and deploys custom scripts
- Schedules deployments (e.g. install at night)

---

## Setting up PDQ Deploy on Server 2022 (My Lab Environment)

- My Windows Server 2022 has a static IP.  
  In order to download PDQ, I had to change it to a dynamic IP address.

### Steps:
1. Navigate to **Control Panel** → **Network** → **Change Adapter Settings**
2. Go to PDQ official website
