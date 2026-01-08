# 📂 DMS Enterprise – User Setup & Operation Guide

**Version:** 1.0 | **Powered by:** SGAI Technology

Welcome to the **Data Management System (DMS)**. This application is designed to securely manage your client database and document archives with support for both local and cloud-based (OneDrive/SharePoint) storage.

---

## 📖 Table of Contents
- [1. Installation & First Run](#1-installation--first-run)
- [2. Initial Setup: Connecting Your Data](#2-initial-setup-connecting-your-data)
- [3. ☁️ SharePoint / Multi-User Setup](#3-️-sharepoint--multi-user-setup-admin-guide)
- [4. Using the Application](#4-using-the-application)
- [5. Admin Settings & Configuration](#5-admin-settings--configuration)
- [6. Licensing & Activation](#6-licensing--activation)
- [7. Closing the App](#7-closing-the-app)

---

## 1. Installation & First Run

1.  **Download:** Get the latest `DMS_Enterprise.exe` from the Releases section.
    > **Tip:** You can place this file anywhere (Desktop, Documents, etc.). It acts as a standalone portable app.
2.  **Launch:** Double-click `DMS_Enterprise.exe`.
3.  **App Mode:** The application will launch in a secure "App Mode" window (no browser tabs or address bars).
4.  **Trial License:** On the first run, a **Trial License** is automatically generated. You will be taken directly to the "Welcome" or "Login" screen.
5.  **Download:** [Click here to download DMS_Enterprise.exe (v1.0)](https://drive.google.com/file/d/19_lyyEAs_QWMzAHhEPZODlrh5m8yimXu/view?usp=sharing)

*(Screenshot: The Secure Login Screen)*
![DMS Login Screen](2025-12-28_19-27-26.png)

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

* ![Connect Folder Screen](2025-12-28_19-27-42.png)

---

## 3. ☁️ SharePoint / Multi-User Setup (Admin Guide)

**Objective:** Create a central shared database accessible to all staff via Windows File Explorer.

1.  **Prepare the Cloud Folders:**
   * Create a folder in your **SharePoint** named `DMS_Central_Data`.
   * Right click and make shortcut in **OneDrive** `DMS_Central_Data`.
    
    * **Link** the OneDrive folder to the SharePoint Folder.

2.  **Sync to Local Computer:**
    * Once the link is established, look at the SharePoint header toolbar.
    * Click the **3 dots (...)** to expand the menu.
    * Click **Sync**.

3.  **Verify Connection:**
    * Open your Windows **File Explorer**.
    * You will see a new **Office Building Icon** 🏢 (representing your Organization) appear above "This PC".
    * Open it to confirm the `DMS_Central_Data` folder is visible inside.
    * No need to do or use this folder ... this is for link perpouse only.

4.  **Connect DMS App:**
    * Open the **DMS Enterprise** app.
    * Navigate into the **OneDrive** windows folder in File Explorer and open `DMS_Central_Data` shortcut and copy the address path.
    * Paste this **Shortcut path** into the app's "Shared Folder Path" field (e.g., `C:\Users\Admin\OneDrive - Company\DMS_Central_Data`).
    * Click **Connect**.

5.  **System Generation / Relinking:**
    * **New Setup:** The system will automatically generate the database files (`Client_Database.xlsx`, etc.).
    * **Existing Data:** If you already have a database in that folder, the app will simply **re-link** to it and retrieve your data immediately.

---

## 4. Using the Application

### 🔐 Login
* **Default Username:** `admin`
* **Default Password:** `admin123`
    > ⚠️ **Security Warning:** Please create a new admin user and delete this default account immediately after setup via the *User Management* menu.

### 📂 Sidebar Menu
* **👥 Clients:** Manage companies and individuals.
* **📂 DMS Records:** The core document archive.
* **⚙️ Settings:** (Admin Only) Configure system preferences.
* **👥 User Management:** (Admin Only) Manage staff access.

### ⚡ Step-by-Step Workflow

#### Step 1: Add a Client
1.  Navigate to **Clients** > **Add Client**.
2.  Enter the Name (e.g., "Apex Logistics").
3.  Click **Save**. A unique ID (e.g., `CL-001`) is auto-assigned.

 ![Add Document Screen](2025-12-28_19-28-35.png)

#### Step 2: Add a Document
1.  Navigate to **DMS Records** > **Add Document**.
2.  **Scan:** Click `🖨️ Scan` to trigger your Windows scanner (WIA).
3.  **Upload:** Drag and drop a file (PDF, PNG, JPG).
4.  **Tag:** Select the *Client*, *Category* (Invoice, Contract, etc.), and *Department*.
5.  **Save:** Click Save. The file is renamed with a unique ID (e.g., `SGAI-0056`) and moved to the secure folder.

   ![Add Document Screen](2025-12-28_19-29-10.png)

#### Step 3: Retrieve a Document
1.  Navigate to **DMS Records** > **View Database**.
2.  Use the 🔍 **Search** bar (search by Client Name, Ref ID, or Note).
3.  Select the Document ID from the dropdown.
4.  Click **📂 Open** to launch the file immediately.

 ![Add Document Screen](2025-12-28_19-29-05.png)
 
---

## 5. Admin Settings & Configuration

The **⚙️ Settings** menu is available only to users with the **Admin** role. It allows you to customize the system to fit your workflow.

### 📝 Manage Dropdowns
Customize the lists used when adding documents to ensure consistent tagging.
* **Select List:** Choose "Categories", "Departments", or "Locations".
* **➕ Add:** Create new items (e.g., add "Procurement" to Departments).
* **✏️ Rename:** Fix typos or update names (e.g., change "Rack A" to "Cabinet 1").
* **🗑️ Delete:** Remove unused options from the list.

### 🛠️ System Preferences
* **Document Reference Prefix:** Change the prefix used for generated document IDs.
    * *Default:* `SGAI` (e.g., `SGAI-0001`)
    * *Custom:* Change it to your company code (e.g., `ABCD` -> `ABCD-0001`).

### 🔴 System Reset
* **Disconnect Database:** Unlinks the current shared folder path.
* *Use Case:* Use this if you need to move your database location or switch to a different cloud folder.
* *Warning:* This does not delete your files, but the app will require you to "Connect Folder" again on the next launch.

![Add Document Screen](2025-12-28_19-29-21.png)

---

## 6. Licensing & Activation

When your trial expires or you are ready to upgrade:

1.  Click the **ℹ️ License Info** button at the bottom of the sidebar.
2.  Choose your activation method:
    * **📲 WhatsApp:** Scan the QR code to request a renewal key from the Admin team.
    * **🔑 Manual Key:** Paste the key text sent to you into the "Manual Key" tab and click **Activate**.
    * **🔄 Online Check:** If the Admin has updated your license remotely, click **Check Online & Activate**. The app will instantly update your version and expiry date.

![Add Document Screen](2025-12-28_19-29-39.png)
---

## 7. Closing the App

**Always** use the specific exit buttons provided in the app:
* **❌ EXIT APP** (Sidebar)
* **🔴 SHUTDOWN SYSTEM** (Login Screen)

**Why?** This ensures the system sends a secure "Disconnect" signal to the Kill Task server before closing, preventing "ghost" sessions.

# ☕ Support

If you find this app helpful after the free trial, your support—by purchasing a license or buying me a coffee—is greatly appreciated.
Don't worry, the license is very cheap and the support is very high.

# [![Support via PayPal](https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=NU8U7YL5PR96S)


