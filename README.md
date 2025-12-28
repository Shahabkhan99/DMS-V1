# 📂 DMS Enterprise – User Setup & Operation Guide

**Version:** 1.0 | **Powered by:** SGAI Technology

Welcome to the **Data Management System (DMS)**. This application is designed to securely manage your client database and document archives with support for both local and cloud-based (OneDrive/SharePoint) storage.

---

## 📖 Table of Contents
- [1. Installation & First Run](#1-installation--first-run)
- [2. Initial Setup: Connecting Your Data](#2-initial-setup-connecting-your-data)
- [3. ☁️ Multi-User Setup (OneDrive / SharePoint)](#3-️-how-to-setup-for-multiple-users-onedrive--sharepoint)
- [4. Using the Application](#4-using-the-application)
- [5. Licensing & Activation](#5-licensing--activation)
- [6. Closing the App](#6-closing-the-app)

---

## 1. Installation & First Run

1.  **Download:** Get the latest `DMS_Enterprise.exe` from the Releases section.
    > **Tip:** You can place this file anywhere (Desktop, Documents, etc.). It acts as a standalone portable app.
2.  **Launch:** Double-click `DMS_Enterprise.exe`.
3.  **App Mode:** The application will launch in a secure "App Mode" window (no browser tabs or address bars).
4.  **Trial License:** On the first run, a **Trial License** is automatically generated. You will be taken directly to the "Welcome" or "Login" screen.

---

## 2. Initial Setup: Connecting Your Data

Before using the app, you must define where the database and files will be stored.

### The "Connect Folder" Screen
Upon your first login, you will be prompted to enter a **Shared Folder Path**.

### Option A: Single User (Local Storage)
1.  Create a folder on your computer (e.g., `C:\MyDocuments\DMS_Data`).
2.  Paste that full path into the DMS application.
3.  Click **Connect**.

### System Generation
Once connected, the system automatically generates the following structure in your selected folder:
* `Client_Database.xlsx` (Registry of clients)
* `DMS_Database.xlsx` (Document metadata)
* 📂 `DMS_Files/` (Secure storage for PDF/Images)
* 📂 `Scanned_Ingest/` (Temporary folder for scanner inputs)

---

## 3. ☁️ How to Setup for Multiple Users (OneDrive / SharePoint)

The DMS is designed to work seamlessly with Microsoft OneDrive or SharePoint to allow real-time collaboration.

### ✅ Prerequisite
You must have the **OneDrive** or **SharePoint** desktop app installed, and the target folder must be **synced** to your Windows File Explorer.

### Setup Steps

#### For the Admin (User 1)
1.  Create a folder in your OneDrive/SharePoint named `DMS_Central_Data`.
2.  Open DMS Enterprise.
3.  Paste the **local synced path** to that folder (e.g., `C:\Users\Admin\OneDrive - Company\DMS_Central_Data`).
4.  Let the system generate the database files.

#### For Staff (User 2, 3, etc.)
1.  Ensure the staff member has **Edit permissions** to the shared OneDrive/SharePoint folder.
2.  **Important:** Verify the folder is synced to *their* PC.
3.  Open DMS Enterprise on their computer.
4.  Paste **their specific local path** to the synced folder (e.g., `C:\Users\JohnDoe\OneDrive - Company\DMS_Central_Data`).

**Result:** When User 1 saves a file, it uploads to the cloud and appears instantly for User 2.

---

## 4. Using the Application

### 🔐 Login
* **Default Username:** `admin`
* **Default Password:** `admin123`
    > ⚠️ **Security Warning:** Please create a new admin user and delete this default account immediately after setup via the *User Management* menu.

### 📂 Sidebar Menu
* **👥 Clients:** Manage companies and individuals.
* **📂 DMS Records:** The core document archive.
* **⚙️ Settings:** (Admin Only) System preferences.
* **👥 User Management:** (Admin Only) Manage staff access.

### ⚡ Step-by-Step Workflow

#### Step 1: Add a Client
1.  Navigate to **Clients** > **Add Client**.
2.  Enter the Name (e.g., "Apex Logistics").
3.  Click **Save**. A unique ID (e.g., `CL-001`) is auto-assigned.

#### Step 2: Add a Document
1.  Navigate to **DMS Records** > **Add Document**.
2.  **Scan:** Click `🖨️ Scan` to trigger your Windows scanner (WIA).
3.  **Upload:** Drag and drop a file (PDF, PNG, JPG).
4.  **Tag:** Select the *Client*, *Category* (Invoice, Contract, etc.), and *Department*.
5.  **Save:** Click Save. The file is renamed with a unique ID (e.g., `ALMA-0056`) and moved to the secure folder.

#### Step 3: Retrieve a Document
1.  Navigate to **DMS Records** > **View Database**.
2.  Use the 🔍 **Search** bar (search by Client Name, Ref ID, or Note).
3.  Select the Document ID from the dropdown.
4.  Click **📂 Open** to launch the file immediately.

---

## 5. Licensing & Activation

When your trial expires or you are ready to upgrade:

1.  Click the **ℹ️ License Info** button at the bottom of the sidebar.
2.  Choose your activation method:
    * **📲 WhatsApp:** Scan the QR code to request a renewal key from the Admin team.
    * **🔑 Manual Key:** Paste the key text sent to you into the "Manual Key" tab and click **Activate**.
    * **🔄 Online Check:** If the Admin has updated your license remotely, click **Check Online & Activate**. The app will instantly update your version and expiry date.

---

## 6. Closing the App

**Always** use the specific exit buttons provided in the app:
* **❌ EXIT APP** (Sidebar)
* **🔴 SHUTDOWN SYSTEM** (Login Screen)

**Why?** This ensures the system sends a secure "Disconnect" signal to the server before closing, preventing "ghost" sessions.
