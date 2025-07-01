# yoyoyoyo


# 🖥️ Windows Client OS Administration (Module 1)

## 📋 Project Description

This project focuses on mastering core administrative tasks within a Windows 10 desktop environment in a local virtual lab. It demonstrates user and group management, NTFS file and folder permissions, and fundamental disk management operations — all critical skills for aspiring IT Technicians.

---

## 🧰 Tools & Environments

- **Virtualization Software**: VirtualBox  
- **Operating System**: Windows 10 (Client Edition)

---

## 🗂️ Project Structure

### ✅ Part 1: User and Local Group Management (GUI & CLI)

#### 👤 Creating Users (GUI)
- Created `standarduser1` (Standard) and `adminuser1` (Administrator) using **Computer Management**.
<p align="center">
  <img src="https://i.imgur.com/iEaVij4.png" width="80%" alt="Creating Standard User"/>
  <br />

- `adminuser1` was added to the **Administrators** group.

<p align="center">
  <img src="https://i.imgur.com/Ru8leT0.png" width="80%" alt="Creating Admin User"/>
  <br />
  
  <img src="https://i.imgur.com/fCyxhtM.png" width="80%" alt="Adding Admin User to Group"/>
</p>

#### 🔐 User Permissions Testing
- **Standard user** was prompted with UAC when attempting administrative tasks.

<p align="center">
  <img src="https://i.imgur.com/HumZ3OV.png" width="80%" alt="User Login Options"/>
  <br />
  <img src="https://i.imgur.com/rkFaNEy.png" width="80%" alt="Standard User UAC Prompt"/>
  <br />
  <img src="https://i.imgur.com/pChFZZF.png" width="80%" alt="Admin User UAC Prompt"/>
</p>

- **Administrator user** had full access without UAC interruption.

<p align="center">
  <img src="https://i.imgur.com/7xGKL1C.png" width="80%" alt="User Login Options"/>
  <br />
  <img src="https://i.imgur.com/pChFZZF.png" width="80%" alt="Admin User UAC Prompt"/>
</p>

#### 💻 Command-Line Management
- Used `net user` and `net localgroup` for:
  - Creating users
  - Adding/removing users from groups
  - Deleting accounts

<p align="center">
  <img src="https://i.imgur.com/zeyya4j.png" width="80%" alt="CMD Group Management"/>
</p>

---

### 🔐 Part 2: NTFS File and Folder Permissions

#### 📁 Folder Structure
- Created a main folder: `SharedData`
  - Subfolders: `Public`, `Private`

<p align="center">
  <img src="https://i.imgur.com/wTgTful.png" width="80%" alt="SharedData Folder Structure"/>
</p>

#### 🛠️ Setting NTFS Permissions
- Gave `standarduser1` **Modify & Write** permissions on `SharedData`.
- Assigned `adminuser1` **Full Control** on `Private`, and **disabled inheritance** to restrict `standarduser1`.

<p align="center">
  <img src="https://i.imgur.com/8F6OcMb.png" width="80%" alt="Setting SharedData Permissions"/>
  <br />
  <img src="https://i.imgur.com/PqMYQyW.png" width="80%" alt="Disabling Inheritance on Private Folder"/>
</p>

#### 🔍 Testing Access
- `standarduser1`:
  - ✅ Access to `Public`
  - ❌ Denied access to `Private`
- `adminuser1`:
  - ✅ Full access to both

<p align="center">
  <img src="https://i.imgur.com/MhGqm9u.png" width="80%" alt="Access Denied to Private Folder"/>
  <br />
  <img src="https://i.imgur.com/50q25Q2.png" width="80%" alt="Admin User Full Access"/>
</p>

---

### 💾 Part 3: Disk Management

#### ➕ Adding & Initializing a New Disk
- Attached a new virtual hard disk using VirtualBox.
- Initialized the disk in **Disk Management**.

<p align="center">
  <img src="https://i.imgur.com/hxc6UFi.png" width="80%" alt="Unallocated New Disk"/>
</p>

#### 📁 Creating and Formatting Volumes
- Created a **Simple Volume (E:)**.
- Successfully formatted the volume.

<p align="center">
  <img src="https://i.imgur.com/HDiFJ8c.png" width="80%" alt="New Data Volume Created"/>
</p>

#### 🔻 Shrinking Volumes
- Shrunk the primary `C:` drive to free up unallocated space.

<p align="center">
  <img src="https://i.imgur.com/GnPljSt.png" width="80%" alt="Shrink C Drive Dialog"/>
  <br />
  <img src="https://i.imgur.com/X1jQXRA.png" width="80%" alt="Shrunk C Drive"/>
</p>

---

## 📌 Key Takeaways

- Mastered local user/group management via GUI and CLI.
- Practiced NTFS permission assignment and inheritance control.
- Performed basic disk operations: initializing, formatting, and resizing volumes.

---

## 📷 Screenshots

All demonstrations are supported with screenshots for verification and educational reference. Scroll through the above sections or refer to the `images/` folder (if cloned locally).

---

## 🚀 Future Enhancements

- Integrate PowerShell automation for user/group management and permission configuration.
- Explore BitLocker and encryption settings.
- Expand to multi-user scenarios and remote administration.

---

