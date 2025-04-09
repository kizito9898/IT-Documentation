# Map Drive

## How to map a drive (Share Drive Permissions) - Home Lab

A mapped drive or shared folder is a network location assigned a drive letter on a computer, allowing users to access files and folders on a remote server as if they were stored locally.

---

## Steps to Create a Shared Folder

1. Go to **Start menu** → Search for **Server Manager**
2. Navigate to **File and Storage Services**
3. Tap on **Shares** → **New Share**
4. Choose **SMB Share - Quick** → Click on it and click **Next**
5. Select **Share location** → Click **Next**
6. Enter **Share name** (e.g., `HR` or `Sales`) → Click **Next**
7. Configure **Other Settings** → Click **Next**
8. Set **Permissions** → Confirm and click **Create**

---

## Access the Shared Folder

1. Go to **File Explorer** → **This PC** → **Local Disk (C:)**
2. Check under **HR Folders** (This is the shared folder we just created)

---

## Note

- Typically in a work environment, shared folders are assigned to a **group**.
- Only group members are allowed to access that folder.
- These groups are created in **Active Directory Users and Computers** (Group type: *Security*) to be able to access the files.
