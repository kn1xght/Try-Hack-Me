# WINDOWS FUNDAMENTALS 2  
**Date:** 2025-10-13  

---

### System Configuration (MSConfig)  

The **System Configuration** utility (`msconfig`) is an advanced troubleshooting tool primarily used to diagnose startup issues.  

It includes five main tabs:  
- **General**  
- **Boot**  
- **Services**  
- **Startup**  
- **Tools**  

Microsoft recommends using **Task Manager** (`taskmgr`) to manage startup programs, as MSConfig isn’t intended for enabling or disabling them — it’s strictly for diagnostics.  

---

### Computer Management (compmgmt.msc)  

The **Computer Management** utility consolidates several administrative tools under one interface.  
It’s divided into three main sections:  
- **System Tools**  
- **Storage**  
- **Services and Applications**  

---

### Task Scheduler  

**Task Scheduler** allows users to create and manage automated tasks that the computer executes at defined times or triggers.  
It’s widely used for backups, updates, and routine system maintenance.  

---

### Event Viewer  

**Event Viewer** logs system and application events and helps diagnose errors or security issues.  

It includes three main panes:  
- **Left pane:** Hierarchical tree view of event log categories  
- **Middle pane:** Overview and detailed summaries of selected logs  
- **Right pane:** Action menu for log management  

**Event Types:**  
- Error  
- Warning  
- Information  
- Success Audit  
- Failure Audit  

**Standard Logs (under “Windows Logs”):**  
- Application  
- Security  
- System  
- CustomLog  

Event Viewer is one of the most powerful tools for administrators, especially in troubleshooting system stability and auditing activity.  

---

### Sessions and Performance  

Under the **Sessions** tab, you can see a list of users currently connected to shared resources.  

In **Performance**, you’ll find the **Performance Monitor** (`perfmon`), which tracks real-time system metrics such as CPU, disk, and memory usage.  

---

### Device Manager  

**Device Manager** provides a structured view of the system’s hardware. It allows administrators to view, configure, update, or disable hardware components.  

---

### Storage Management  

Under the **Storage** category, two tools are typically included:  
- **Windows Server Backup**  
- **Disk Management**  

**Disk Management** lets users perform advanced storage tasks such as:  
- Setting up new drives  
- Extending or shrinking partitions  
- Assigning or changing drive letters (e.g., `E:`)  

---

### WMI Control  

**WMI Control** configures and manages the **Windows Management Instrumentation (WMI)** service, which allows remote and local system management via scripting languages like PowerShell or VBScript.  
Modern systems, however, primarily use **PowerShell** for WMI interaction, as it provides far more flexibility and control.  

---

### System Information (msinfo32)  

**System Information** (`msinfo32`) gathers detailed data about the system’s hardware, components, and software environment.  
This tool provides a top-down overview of system configuration, which is especially useful for troubleshooting and diagnostics.  

**Information is categorized into three sections:**  
- **Hardware Resources** — IRQs, DMA channels, and other low-level details  
- **Components** — Hardware devices and driver information  
- **Software Environment** — Installed applications and system processes  

---

### Resource Monitor (resmon)  

**Resource Monitor** (`resmon`) offers a real-time view of system performance.  
It breaks down CPU, memory, disk, and network usage both per-process and in aggregate.  

**The Overview tab includes:**  
- CPU  
- Disk  
- Network  
- Memory  

This tool is particularly helpful for identifying resource bottlenecks or troubleshooting performance issues.  

---

### Command Prompt (cmd.exe)  

While intimidating at first, the **Command Prompt** is a simple yet powerful tool once you understand how to interact with it.  
Before graphical interfaces, the command line was the *only* way to interact with operating systems.  

Common commands include:  
- `hostname` — Displays the computer name.  
- `whoami` — Shows the currently logged-in user.  
- `ipconfig` — Displays network adapter information and IP configuration.  
- `command /?` — Displays the help manual for a specific command.  
- `cls` — Clears the terminal screen.  
- `netstat` — Displays current TCP/IP network connections and statistics.  
- `net help` — Displays help for the `net` command and its subcommands.  

The command line remains one of the most efficient ways to manage Windows systems, especially for networking and troubleshooting.  

---

### Windows Registry (regedit)  

The **Windows Registry** is a hierarchical database that stores configuration information for the operating system, users, applications, and hardware.  

It contains critical data such as:  
- User profiles  
- Installed applications and file associations  
- Folder and icon settings  
- Hardware configuration and driver information  
- Port assignments  

⚠️ **Warning:** Editing the Registry is dangerous if done incorrectly — one wrong change can render a system unstable or unbootable.  

The Registry should only be modified by advanced users or administrators who understand its structure and implications.  

---

### Takeaway  

Building on what I learned in Windows Fundamentals 1, this section helped me dive deeper into the tools that Windows offers. I got to explore utilities I’ve used casually before, such as MSConfig, Event Viewer, and the Registry Editor. I’m now more deeply acquainted with these tools and understand their purpose much better. One thing I noticed missing was dxdiag, which I personally use often to check my hardware and plan future upgrades.