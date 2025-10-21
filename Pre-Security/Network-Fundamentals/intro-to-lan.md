# INTRODUCTION TO LAN

**Date:** 2025-10-14

---

### Network Topologies  

### Star Topology  
In a **Star Topology**, devices are individually connected to a central networking device such as a **switch** or **hub**.  
This is the most commonly used topology today due to its **reliability** and **scalability**, despite higher setup costs.

### Bus Topology  
A **Bus Topology** relies on a single connection known as a **backbone cable**.  
All data destined for each device travels along this shared cable, making it **cost-efficient** and **easy to set up**, but also prone to **bottlenecks** if multiple devices transmit data simultaneously.  
Because the connection is shared, performance can degrade quickly under heavy load.

### Ring Topology  
In a **Ring Topology**, devices are connected directly to each other in a circular loop.  
This design requires minimal cabling and less dependence on dedicated hardware compared to a star topology.  
However, data can only travel in one direction, making it less efficient — packets may need to pass through several devices before reaching their destination.  
A single fault, such as a broken cable or failed device, can bring down the entire network.

---

### What is a Switch?  

A **switch** is a dedicated network device designed to connect multiple other devices (computers, printers, etc.) using Ethernet.  

Switches can support multiple ports — typically 4, 8, 16, 24, 32, or 64 — allowing many devices to connect simultaneously.  

Switches are much more efficient than hubs or repeaters because they keep track of which device is connected to which port.  
When a packet is received, instead of broadcasting it to every port like a hub would, the switch sends it only to the intended destination, reducing unnecessary network traffic.  

Switches and routers can also be connected to one another, increasing **redundancy** and **reliability** by providing multiple paths for data to travel.

---

### What is a Router?  

A **router** connects different networks and directs data between them — a process known as **routing**.  
Routing establishes a path that data can follow between networks to ensure successful delivery.  

---

### Subnetting  

**Subnetting** is the process of splitting a network into smaller, more manageable sub-networks (subnets).  
This is done by dividing the number of available hosts within the network, using a **subnet mask** (represented as four bytes or 32 bits).  

Subnets use IP addresses in three main ways:  
- **Network Address** — identifies the start of the network.  
- **Host Address** — identifies individual devices on the subnet.  
- **Default Gateway** — identifies the device capable of sending data outside the subnet (to other networks).  

**Benefits of Subnetting:**  
- Improved **efficiency**  
- Enhanced **security**  
- Greater **control** over traffic management  

---

### Address Resolution Protocol (ARP)  

The **Address Resolution Protocol (ARP)** allows devices to associate their **MAC address** with an **IP address** on a network.  
This enables devices to identify each other for communication.  

Each device maintains an **ARP cache**, a small ledger storing known IP-to-MAC address mappings.  

ARP uses two types of messages to perform this mapping:  
- **ARP Request** — a broadcast asking for the MAC address associated with a specific IP address.  
- **ARP Reply** — the response providing the requested MAC address.  

---

### Dynamic Host Configuration Protocol (DHCP)  

IP addresses can be assigned **manually** (static addressing) or **automatically** using a **DHCP (Dynamic Host Configuration Protocol)** server.  

DHCP automates IP assignment through the following steps:  
1. **DHCP Discover** — the client broadcasts a request to find available DHCP servers.  
2. **DHCP Offer** — the server responds with an available IP address.  
3. **DHCP Request** — the client requests to use the offered address.  
4. **DHCP ACK** — the server acknowledges the request and finalizes the lease, allowing the client to use that IP address.  

This process simplifies network configuration and ensures that IP addresses are efficiently distributed and managed.

---

### Takeaway  

I really like how this topic reinforces the idea that trial and error is still what drives optimization — the best way to find what works is to test and refine, just like we did with network topologies. Beyond that, it was interesting to realize that, beneath all the hardware and protocols, networks were designed to communicate much like humans do — even though human communication will always remain the most complex skill we can develop, given how many variables it accounts for in every interaction.