# WINDOWS FUNDAMENTALS 3

**Date:** 2025-10-13  

Windows Update is a Microsoft service that delivers security patches, feature updates, and system improvements for Windows and other Microsoft products like Microsoft Defender. Updates are usually released on the second Tuesday of each month — commonly known as *Patch Tuesday*. However, critical patches may be pushed outside of this schedule if the issue is urgent and requires immediate attention.

---

### Windows Security

Windows Security is the central location for managing the tools that protect your device and data. It provides a unified interface for all key security settings, making it easier to monitor your system’s health and respond to potential threats.

It consists of the following modules:
- Virus & Threat Protection
- Firewall & Network Protection
- App & Browser Control
- Device Security

Color indicators show the current protection status:
- 🟢 Green — Your device is protected, and no action is required.
- 🟡 Yellow — There’s a security recommendation that needs your review.
- 🔴 Immediate attention is required to resolve a serious issue.

---

### Virus & Threat Protection

This section is divided into two main parts:
- **Current threats** — Displays any active or recently detected issues.
- **Virus & threat protection settings** — Allows configuration of scan types, exclusions, and protection options.

**Scan options include:**
- **Quick scan:** Checks folders where threats are commonly found.
- **Full scan:** Scans all files and running programs on your device; may take over an hour.
- **Custom scan:** Lets you choose which files and directories to scan.

**Threat history** helps track what the antivirus has detected:
- **Last scan:** Displays when and how your last scan was performed.
- **Quarantined threats:** Threats isolated and prevented from running; removed periodically.
- **Allowed threats:** Items flagged as threats but manually allowed by the user.

Only allow a flagged file to run if you are absolutely sure it’s safe.

**Manage Settings options:**
- **Real-time protection:** Stops malware from executing.
- **Cloud-delivered protection:** Uses Microsoft’s cloud to improve detection speed and accuracy.
- **Automatic sample submission:** Sends suspicious files to Microsoft for deeper analysis.
- **Controlled folder access:** Protects key system areas from unauthorized modification.
- **Exclusions:** Skips scanning of specified files or directories.
- **Notifications:** Displays critical alerts and system health messages.

Excluding files may leave your system vulnerable; use this only if necessary.

**Ransomware protection** depends on *Controlled Folder Access*, which requires *Real-time Protection* to be active.

---

### Windows Firewall

Network traffic moves in and out of your device through communication ports. The **Windows Defender Firewall** acts like a security guard standing at these ports — inspecting what enters and leaves, blocking anything unauthorized.

**Firewall profiles:**
- **Domain:** Used when connected to an authenticated domain network.
- **Private:** Intended for trusted networks like your home or office.
- **Public:** The default profile for untrusted networks such as cafés or airports.

Unless you know exactly what you’re doing, keep your Windows Firewall enabled. Disabling it exposes your system to potential attacks.

To open Windows Defender Firewall directly, use:
`wf.msc`

---

### Microsoft Defender SmartScreen

**Microsoft Defender SmartScreen** helps protect against phishing, malware, and the downloading of unsafe files or applications. It operates across two domains:
- **Exploit Protection:** Shields the system from common vulnerability exploitation.
- **Check Apps and Files:** Scans downloaded content to detect malicious behavior.

---

### Trusted Platform Module (TPM)

The **Trusted Platform Module (TPM)** is a hardware-based security component — a chip designed to handle cryptographic operations securely. It stores encryption keys, digital certificates, and integrity measurements in an isolated, tamper-resistant environment. This makes it nearly impossible for malware to extract sensitive information directly from it.

---

### BitLocker Drive Encryption

**BitLocker** is a full-disk encryption feature built into Windows that protects data from theft or exposure if a device is lost or stolen. It integrates tightly with TPM, offering the strongest protection when a TPM 1.2 or newer chip is present.

Devices without a TPM can still use BitLocker by:
- Using a **startup key** stored on a removable drive.
- Using a **password**, though this is less secure since it’s vulnerable to brute-force attacks. (Password-based encryption is disabled by default.)

---

### Volume Shadow Copy Service (VSS)

The **Volume Shadow Copy Service (VSS)** coordinates the creation of consistent point-in-time snapshots — also known as *restore points*. These snapshots allow system restoration without interrupting active processes.

When System Protection is enabled, you can:
- Create a restore point manually.
- Perform a system restore.
- Configure restore settings.
- Delete previous restore points.

VSS is a critical part of Windows recovery infrastructure, ensuring system stability after major updates or malware removal.

---

### Living Off The Land (LOTL)

Attackers often exploit legitimate Windows tools to remain undetected — a technique known as **Living Off The Land (LOTL)**. Tools such as PowerShell, WMI, `net`, and `cmd` can be used maliciously while appearing as normal activity. Understanding how these tools function helps identify when they’re being abused.

---

### Additional Security Layers

Windows includes several advanced protections that work together:
- **Windows Defender Antivirus:** Core protection against malware.
- **Firewall and Network Isolation:** Monitors inbound and outbound traffic.
- **SmartScreen:** Prevents dangerous downloads and phishing.
- **BitLocker and TPM:** Hardware-backed encryption and secure boot.
- **VSS Restore Points:** Enables recovery from damage or corruption.

Together, these components make Windows a layered and resilient operating system that balances usability with security.

---

### Takeaway

Wrapping up the Windows Fundamentals series, this section helped me see how Windows ties its security and recovery mechanisms together. I learned about tools like Windows Defender, BitLocker, TPM, and Volume Shadow Copy, which made it clear that Windows security isn’t just about antivirus software — it’s a system of connected layers working to protect data, prevent breaches, and enable recovery when things go wrong. It also reminded me how important it is to keep Windows updated — updates don’t just add features, they often deliver critical security patches that keep everything running safely.