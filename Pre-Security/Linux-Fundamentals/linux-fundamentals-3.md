# LINUX FUNDAMENTALS 3 
**Date:** 2025-10-12 

So far, we have only stored text in files using a combination of the `echo` command and the pipe operators (`>` and `>>`). However, this isn’t an efficient way to handle data when working with files that contain multiple lines or larger amounts of text.

Here we are introduced to **Nano** and the alternative **Vim** text editors.  

To create or edit a file using Nano, simply use: `nano filename`.

Nano has several features that are easy to remember and cover most general tasks you would expect from a text editor, including:  
- Searching for text  
- Copying and pasting  
- Jumping to a specific line number  
- Finding out what line number you are currently on  

To use these features, hold **CTRL** and press the corresponding letter.  
Examples:  
`CTRL + W` (search), `CTRL + K` (cut), `CTRL + U` (paste), `CTRL + C` (show line), `CTRL + X` (exit Nano).  

Vim is a much more advanced text editor. While you’re not expected to know all of its advanced features, it’s helpful to mention it when building Linux proficiency.  

Some of Vim’s benefits, though it takes longer to learn, include:  
- Customizable configuration and key mappings  
- Syntax highlighting  
- Works on nearly all terminals (where Nano may not be installed)  
- Large community resources, cheat sheets, and tutorials  

---

### File Transfers  

A fundamental feature of computing is the ability to transfer files between systems.  

### wget  
`wget` allows downloading files from the web via HTTP/HTTPS, as if accessing them through a browser. Example:  
`wget http://example.com/file.txt`  

### scp (Secure Copy)  
`scp` securely copies files between two computers using SSH for authentication and encryption.  

The command follows a **SOURCE → DESTINATION** model and can be used to:  
- Copy files or directories from your current system to a remote system  
- Copy files or directories from a remote system to your current system  

Examples:  
`scp file.txt user@remote_ip:/home/user/`  
`scp user@remote_ip:/home/user/file.txt /local/folder/`  

---

### Lightweight Web Server with Python  

Ubuntu comes with Python3 pre-installed. Python conveniently provides a lightweight module called **http.server**, which turns your machine into a quick web server to share files.  

To start a simple web server in your current directory:  
`python3 -m http.server 8080`  

Other devices on the same network can then download files using `curl` or `wget`.  

---

### Processes  

Processes are the programs currently running on your machine. They are managed by the kernel, and each process has an ID called a **PID** (Process ID).  

Use `ps` to list processes tied to your current session, showing details such as PID, status, CPU time, and command name.  

`ps aux` shows processes from all users, including those not attached to your session.  

`top` displays real-time statistics for all running processes, updating continuously.  

To terminate a process, use the `kill` command followed by its PID, e.g., `kill 1234`.  

---

### systemd and systemctl  

When a system boots, **systemd** is one of the first processes started. Every subsequent program or service becomes a *child process* of systemd.  

`systemctl` lets us interact with systemd using this format:  
`systemctl [option] [service]`  

Common options include:  
- `systemctl start <service>` – start a service  
- `systemctl stop <service>` – stop a service  
- `systemctl enable <service>` – enable a service to start on boot  
- `systemctl disable <service>` – disable auto-start on boot  

---

### Foreground and Background Processes  

Processes can run either in the foreground (actively in your terminal) or in the background (running silently while you continue using the shell).  

`CTRL + Z` suspends and backgrounds a process.  
Typing `fg` brings that process back to the foreground.  

Example:  
`ping google.com` → press `CTRL+Z` → then type `fg` to resume it.  

---

### Scheduling Tasks with Cron  

Users often want to schedule actions or tasks automatically after boot or at regular intervals. This is handled by the **cron** process via **crontabs**.  

Each line in a crontab follows:  
`MIN HOUR DOM MON DOW CMD`  

| Field | Meaning |
|-------|----------|
| MIN | Minute to execute |
| HOUR | Hour to execute |
| DOM | Day of month |
| MON | Month of year |
| DOW | Day of week |
| CMD | Command to run |

Crontabs also support the wildcard `*` when you don’t care about a specific value, e.g., run something every 12 hours regardless of day or month.  

Edit crontabs with:  
`crontab -e`  

Example entry:  
`0 */12 * * * /home/user/backup.sh` → runs every 12 hours.  

---

### Package Management  

The `apt` command installs and manages software on Ubuntu. It’s part of the APT suite, which handles repositories, dependencies, updates, and removals.  

Example:  
`sudo apt update && sudo apt install nmap`  

`dpkg` can also install packages, but `apt` is generally preferred because it automatically checks repositories for updates whenever the system is upgraded.  

---

### Takeaway  

Grasping broader concepts like editing, managing, and automating within Linux is a rough landscape to navigate, especially for a beginner like me. Even so, it’s easy to see why Linux remains the top choice for developers and cybersecurity professionals — everything about it is built for control, flexibility, and speed.