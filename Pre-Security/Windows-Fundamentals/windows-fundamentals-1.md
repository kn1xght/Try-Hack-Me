# WINDOWS FUNDAMENTALS 1
**Date:** 2025-10-13  

---

### Introduction  

Windows remains the dominant operating system for both personal and corporate use. Because of its popularity, it’s also one of the main targets for hackers and malware authors.

---

### Windows Versions  

**Windows 10/11** comes in two main editions — **Home** and **Pro**. The key difference is that the Pro edition includes **BitLocker**, an encryption feature that protects data in case the device is lost or stolen by locking the drive completely.  

For servers, the current version is **Windows Server 2025**, used across enterprises and datacenters.  

---

### The Windows Desktop Environment (GUI)  

After logging into a Windows system, you’re greeted with the **Graphical User Interface (GUI)** — also known as the **Desktop**. It serves as the user’s main workspace.  

**The GUI typically includes:**  
- Desktop  
- Start Menu  
- Search Box (Cortana)  
- Task View  
- Taskbar  
- Toolbars  
- Notification Area  

The desktop allows users to store and access shortcuts to files, folders, and programs. The look and feel can be customized to suit individual preferences.  

---

### File Systems  

Before NTFS, Windows used **FAT16**, **FAT32** (File Allocation Table), and **HPFS** (High-Performance File System). Today, these are mostly used in portable storage devices such as USB drives and SD cards.  

Modern Windows systems use **NTFS (New Technology File System)** as the default file system.  

### Key Features of NTFS  
- **Journaling:** NTFS keeps a log of changes to files, allowing it to recover automatically after a crash or power loss.  
- **Large File Support:** Handles files larger than 4 GB (unlike FAT).  
- **Fine-grained Permissions:** Control over which users can access or modify files.  
- **Compression and Encryption:** Supports file compression and the **Encrypting File System (EFS)**.  

### NTFS Permissions  
- Read  
- Write  
- Read & Execute  
- List Folder Contents  
- Modify  
- Full Control  

### Alternate Data Streams (ADS)  
NTFS also supports **Alternate Data Streams (ADS)** — hidden file attributes that allow a file to contain multiple streams of data.  
Every file has at least one data stream (`$DATA`), but with ADS, additional hidden data can be attached. Windows Explorer doesn’t display ADS natively, though they can be viewed using PowerShell or third-party tools.  

While ADS can serve legitimate purposes, attackers sometimes abuse it to hide malicious code or data within seemingly harmless files — a reason cybersecurity professionals should understand how it works.  

---

### Critical System Directories  

- **`C:\Windows`** — the main Windows directory that holds the operating system’s files. The environment variable `%windir%` points to this location.  
- **`C:\Windows\System32`** — contains core system files essential for Windows to run. Deleting or altering files here can make the system inoperable.  

These folders can technically exist on a different drive or location, but `C:\Windows` remains the standard path.  

---

### User Accounts and Privileges  

Local Windows systems typically have two account types:  
- **Administrator:** Can make system-wide changes (add/delete users, install software, change settings).  
- **Standard User:** Limited to personal files and cannot perform administrative actions.  

Each user profile contains common folders such as:  
- Desktop  
- Documents  
- Downloads  
- Music  
- Pictures  

To view local users and groups, use the command:  
`lusrmgr.msc`  

Running daily tasks (like browsing or editing documents) under an Administrator account increases the attack surface — malware infections are much easier when elevated privileges are active.  

---

### User Account Control (UAC)  

To mitigate privilege misuse, Microsoft introduced **User Account Control (UAC)**.  
When an administrator logs in, the system doesn’t automatically grant full privileges. Instead, any operation requiring elevated rights triggers a **UAC prompt**, asking for confirmation before proceeding.  

This helps reduce accidental system changes and limits the potential damage from malware running under a user’s context.  

---

### System Configuration and Tools  

The main areas for system configuration are:  
- **Settings menu** — modern interface for most customization.  
- **Control Panel** — legacy interface for advanced system management.  

Useful shortcuts:  
- **Task Manager:** `Ctrl + Shift + Esc` — view and manage active processes and applications.  

---

### Takeaway  

> Even though Windows has always been my operating system of choice, I’ve realized there’s a lot more to it than I thought. I used to think I knew my way around, but that was just the surface. Now I see how deep it really goes. I’m actually motivated to see how efficient I can become as a user and an admin.