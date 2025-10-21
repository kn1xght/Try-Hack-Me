# OSI MODEL

**Date:** 2025-10-14  

---

### Introduction  

The **OSI Model (Open Systems Interconnection Model)** is a foundational concept in networking.  
It provides a framework that defines how all networked devices send, receive, and interpret data.  

The main benefit of this model is that devices with different functions and designs can still communicate effectively.  
When data is transmitted across a network that follows the uniformity of the OSI model, it can be understood by all devices involved.  

At every layer that data travels through, specific processes occur and additional information is added to the data.  

---

### The Seven Layers  

1. **Physical**  
2. **Data Link**  
3. **Network**  
4. **Transport**  
5. **Session**  
6. **Presentation**  
7. **Application**  

---

### Physical Layer  

This layer references the **physical components** of networking hardware.  
Devices use electrical signals to transfer data between each other in a binary numbering system (1s and 0s).  

---

### Data Link Layer  

The **Data Link Layer** focuses on the **physical addressing** of transmissions.  
It receives a packet from the Network Layer (which includes the IP address of the destination) and adds the **MAC (Media Access Control)** address of the receiving endpoint.  

Inside every network-enabled computer is a **Network Interface Card (NIC)** that has a unique MAC address used to identify it.  
It’s also the Data Link Layer’s job to present the data in a format suitable for transmission.  

---

### Network Layer  

The **Network Layer** is where the routing and reassembly of data take place — turning small chunks into larger, complete data sets.  
Routing determines the most optimal path for data to travel based on factors such as:  
- Shortest path (fewest devices between source and destination)  
- Reliability (whether packets are often lost along that path)  
- Speed (for example, fiber is faster than copper)  

Common routing protocols include **OSPF (Open Shortest Path First)** and **RIP (Routing Information Protocol)**.  

---

### Transport Layer  

The **Transport Layer** ensures reliable transmission of data across a network.  
It uses one of two key protocols:  

- **TCP (Transmission Control Protocol):**  
  Reliable and connection-oriented. Keeps a consistent connection between devices while data is sent and includes **error checking** to guarantee accurate delivery and reassembly.  
  Used in situations like file sharing, web browsing, and email.  

- **UDP (User Datagram Protocol):**  
  Connectionless and faster, but lacks error checking and reliability features. Data is sent regardless of whether it arrives.  
  Used in time-sensitive applications such as streaming and gaming.  

---

### Session Layer  

The **Session Layer** establishes, manages, and terminates connections (sessions) between computers.  
When a connection is opened, a session is created — and as long as that connection stays active, so does the session.  
This layer also handles session recovery through **checkpoints**, ensuring only the most recent data needs to be resent if a failure occurs.  
Sessions are unique, meaning data can only travel within its own session and not across others.  

---

### Presentation Layer  

The **Presentation Layer** is responsible for **standardizing and translating data** between systems.  
Because different applications may represent data differently, this layer ensures that information sent from one system can be understood by another.  
It acts as a translator between the Application Layer and the rest of the OSI stack.  

---

### Application Layer  

The **Application Layer** defines how users interact with data.  
It includes the software and protocols that allow applications like email clients, browsers, and file transfer tools (e.g., FileZilla) to communicate.  
Common protocols include:  
- **DNS (Domain Name System):** Translates human-readable domain names into IP addresses.  

---

### Takeaway  
 
The OSI Model was pretty straightforward in how it’s structured, the role it plays, and how it functions. Still, understanding how data moves through a network gives valuable insight into how attacks happen — and, more importantly, how we can prevent them.