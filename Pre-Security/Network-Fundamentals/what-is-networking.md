# WHAT IS NETWORKING? 

**Date:** 2025-10-14

---

### Introduction to Networks  

Networks are simply things that are connected.

Networks can be found in all walks of life:  
- A city's public transportation system  
- Infrastructure such as the national power grid for electricity  
- Meeting and greeting your neighbors  
- Postal systems for sending letters and parcels  

In computing, a network can be formed by anywhere from two devices to billions.  

The Internet is one giant network that consists of many smaller networks within itself.  

---

### A Brief History of the Internet  

The first iteration of the Internet was created through the **ARPANET** project in the late 1960s. This project was funded by the United States Department of Defense and was the first documented network in action.  

The Internet as we know it was later developed by **Tim Berners-Lee** with the creation of the **World Wide Web (WWW)**.  

---

### Types of Networks  

A network can be one of two types:  
- **Private Network**  
- **Public Network**  

To communicate and maintain order, devices must be both identifying and identifiable on a network.  

These identifiers are:  
- An **IP Address**  
- A **Media Access Control (MAC) Address** — think of this as being similar to a serial number.  

---

### IP Addresses  

An **IP (Internet Protocol) address** is used to identify a host on a network for a period of time. That same IP address can later be associated with another device without the address itself changing.  

Example: `192.168.1.1` — each section is called an **octet**, and this example has four octets.  

IP addresses can change from device to device but cannot be active simultaneously more than once within the same network.  

A **public address** is used to identify a device on the Internet, whereas a **private address** is used to identify a device among others within a local network.  

Two devices can use their private IP addresses to communicate with each other. However, any data sent to the Internet from either of these devices will be identified by the same public IP address. Public IP addresses are assigned by your **Internet Service Provider (ISP)**.  

---

### MAC Addresses  

A **MAC address** is a twelve-character hexadecimal number (a base sixteen numbering system used in computing to represent numbers) split into pairs and separated by colons.  

The first six characters represent the company that made the network interface, while the last six form a unique identifier for the specific device.  

An interesting fact about MAC addresses is that they can be faked or "spoofed." Spoofing occurs when a networked device pretends to identify as another by imitating its MAC address.  

---

### IPv4 and IPv6  

So far, we have only discussed one version of the Internet Protocol addressing scheme known as **IPv4**, which uses a numbering system of 2³² IP addresses (4.29 billion).  

**IPv6** is a newer iteration of the Internet Protocol addressing scheme designed to tackle this limitation. It supports up to 2¹²⁸ IP addresses (over 340 trillion) and not only resolves the shortage of IPv4 addresses but also improves efficiency through newer methodologies.  

---

### Ping and ICMP  

**Ping** is one of the most fundamental network tools available to us.  

Ping uses **ICMP (Internet Control Message Protocol)** packets to determine the performance of a connection between devices — for example, whether the connection exists and how reliable it is.  

---

### Takeaway  

This introductory lesson on networking was a surprisingly easy read, considering how complex and abstract it’s usually explained. I now see how devices find and communicate with each other using IP and MAC addresses, the key differences between IPv4 and IPv6, and how ICMP keeps that communication running smoothly. Since the network is where everyone connects and everything happens, it’s easy to see why this is such important foundational knowledge for anyone in cybersecurity.