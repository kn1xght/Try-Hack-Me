# LINUX FUNDAMENTALS 2 

**Date:** 2025-10-12

---

### Secure Shell (SSH)
Secure Shell (SSH) is simply a protocol that allows encrypted communication between devices.  
Using cryptography, any input we send in human-readable form is encrypted while travelling over a network and then decrypted once it reaches the remote machine.  

---

### Command Arguments and Flags
A majority of commands allow for arguments to be provided. These arguments are identified by a hyphen and a keyword known as a *flag* or *switch*.  
For example, the command `ls` can be extended with the `-a` argument (short for `--all`) to display hidden folders within the working directory.  
To find all available arguments or options for a command, we can use the `--help` flag.  

---

### Manual Pages
Manual pages are an excellent source of information for both system commands and applications available on a Linux machine.  
They can be accessed directly on the system or found online.  
To open this documentation, we use the `man` command followed by the name of the command we want to read about.  
Example: `man ls`  

---

### Commands for Filesystems
| Command | Description |
|----------|-------------|
| `touch` | Create a file |
| `mkdir` | Create a folder |
| `cp` | Copy a file or folder |
| `mv` | Move a file or folder (can also rename a file or folder) |
| `rm` | Remove a file or folder (must use `-R` to remove a directory) |
| `file` | Determine the type of a file |

---

### File and Folder Characteristics
A file or folder can have several characteristics that determine what can be done with it and by whom. These include:  
- **Read**  
- **Write**  
- **Execute**  

One of the great things about Linux is how granular its permissions system is.  
While a user technically owns a file, permissions can also be set so that a group of users has either the same or different access levels to that file — without affecting the owner’s permissions.  

---

### Real-World Example
A system user that runs a web server must have permissions to read and write files to make the web application function effectively.  
However, web hosting companies need to allow their customers to upload their own website files without giving them the same permissions as the webserver system user.  
Otherwise, one compromised account could endanger every other customer on the same server.  

---

### Switching Between Users
Switching between users on a Linux system is straightforward thanks to the `su` command.  
For example, `su username` allows us to switch to another user, and `su -` starts a login shell for that user.

---

### Important Root Directories
- **`/etc`** — One of the most important root directories. It is the common location for storing system files and configurations used by the operating system.  
- **`/var`** — Short for *variable data*, this directory stores data that is frequently accessed or modified by running services and applications (for example, logs and temporary databases).  
- **`/root`** — Unlike `/home`, which contains users’ home directories, `/root` is the home directory for the *root* (system administrator) account.  
- **`/tmp`** — Short for *temporary*, this volatile directory stores data that only needs to be accessed briefly. When the system restarts, its contents are cleared out.  
  For penetration testing, `/tmp` can be a useful place to store enumeration scripts or temporary files.

---

### Takeaway  
In this block, I learned how permissions and directories define the workflow in Linux, especially when it comes to web applications and the importance of properly dividing user access. Understanding who can read, write, or execute certain files is vital for keeping security tight and preventing unnecessary exposure across the system..