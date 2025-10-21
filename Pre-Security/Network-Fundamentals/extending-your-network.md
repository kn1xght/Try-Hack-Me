# EXTENDING YOUR NETWORK
**Date:** 2025-10-15

---

### Introduction

Port forwarding is an essential component in connecting applications and services to the Internet. 
Without it, applications such as web servers are only available to devices within the same local network.

Port forwarding is configured at the **router** of a network.

A **firewall** is a device responsible for determining what traffic is allowed to enter and exit a network.  
Think of it as border control for your network.

---

### Firewall Rules

An administrator can configure a firewall to permit or deny traffic based on several factors:

- **Source:** Where the traffic originates from.  
  Has the firewall been told to accept or deny traffic from a specific network?

- **Destination:** Where the traffic is going.  
  Has the firewall been told to accept or deny traffic destined for a specific network?

- **Port:** The destination port of the traffic.  
  Has the firewall been told to accept or deny traffic destined for specific ports (e.g., port 80)?

- **Protocol:** The protocol used (TCP, UDP, or both).  
  Has the firewall been told to accept or deny traffic based on the protocol type?

---

### Types of Firewalls

Firewalls come in many forms — from dedicated hardware used in enterprise networks  
to home routers and software-based solutions like **Snort**.

| **Type** | **Description** |
|-----------|-----------------|
| **Stateful Firewall** | Inspects the entire connection rather than individual packets. Determines behavior dynamically. Consumes more resources but makes smarter decisions.
| **Stateless Firewall** | Uses static rules to evaluate individual packets. Lightweight and fast, but less intelligent — only as good as the rules configured. |

Example: Stateless firewalls are effective when handling large amounts of traffic, such as during a **DDoS attack**.

---

### Virtual Private Networks (VPNs)

A **Virtual Private Network (VPN)** allows devices on separate networks to communicate securely  
by creating a **dedicated tunnel** over the Internet. Devices inside this tunnel form their own private network.

---

### Benefits of VPNs

- **Global Connectivity:** Connects networks in different geographical locations.  
- **Privacy:** Prevents data interception.  
- **Anonymity:** Conceals user identity and IP address.

---

### VPN Technologies

| **Technology** | **Description** |
|-----------------|-----------------|
| **PPP (Point-to-Point Protocol)** | Used by PPTP to provide authentication and encryption. Uses private keys and public certificates. Non-routable by itself. |
| **PPTP (Point-to-Point Tunneling Protocol)** | Encapsulates PPP data to allow transmission over the Internet. Easy to configure, widely supported, but weakly encrypted. |
| **IPSec (Internet Protocol Security)** | Encrypts data using the IP framework. Complex to set up but highly secure and widely supported. |

---

### Takeaway
A short summary on network extension, covering the fundamental knowledge behind everyday services like VPNs and firewalls — how they work, when to use them, and why they matter. Nothing new learned, but a solid reminder of the basics, which is never a bad thing, considering how vital these services are in the IT fields.