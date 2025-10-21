# PUTTING IT ALL TOGETHER

**Date:** 2025-10-15

---

### Load Balancers

When a website experiences heavy traffic or requires high availability, a single web server may no longer be sufficient.  
A **Load Balancer** distributes traffic across multiple servers to ensure performance and reliability.

### Key Functions
- **Distributes traffic** to multiple backend servers.  
- **Monitors server health** and removes unresponsive servers automatically.  
- **Provides failover** to maintain uptime if one server fails.

### Common Algorithms
| **Algorithm** | **Description** |
|----------------|-----------------|
| **Round-Robin** | Sends each request to servers in sequence. |
| **Weighted** | Sends requests to the least busy server based on current load. |

Load balancers perform **health checks** to verify that servers are functioning correctly. If a server fails to respond, it’s temporarily removed from rotation until it passes again.

---

### CDN (Content Delivery Network)

A **CDN** helps reduce traffic and latency by distributing static files (like **JavaScript**, **CSS**, **images**, and **videos**) across thousands of servers globally.  
When a user requests one of these files, the CDN directs them to the **nearest available server**, reducing loading times and server strain.

---

### Databases

Websites often need to **store and retrieve data**, such as user information or blog posts.  
This is managed through **databases**, which the web server communicates with to perform read/write operations.

Common database systems include:

| **Type** | **Examples** |
|-----------|---------------|
| **Relational** | MySQL, MSSQL, PostgreSQL |
| **NoSQL** | MongoDB, Redis |
| **Flat-file** | Simple text or CSV files |

Databases can scale from simple single-server setups to complex distributed clusters designed for **speed and resilience**.

---

### WAF (Web Application Firewall)

A **Web Application Firewall (WAF)** sits between users and web servers, analyzing requests for suspicious behavior and blocking attacks.  

### Functions of a WAF
- **Detects and blocks** common attacks (SQL injection, XSS, etc.)  
- **Rate-limits** requests to prevent denial-of-service attacks  
- **Validates browser authenticity** to distinguish real users from bots  

If a request seems malicious, it’s **dropped** before it ever reaches the web server.

---

### How Web Servers Work

A **web server** is a software application that listens for incoming connections and delivers content using the **HTTP protocol**.  
Common web server software includes **Apache**, **Nginx**, **IIS**, and **NodeJS**.

Each web server serves files from its **root directory**, which is defined in its configuration. When you make a request, the server retrieves the correct file and sends it back as a response.

---

### Virtual Hosts

Web servers can host multiple websites on a single machine using **Virtual Hosts**.  
These are configuration files that map **hostnames** to specific website directories.

| **Scenario** | **Behavior** |
|---------------|--------------|
| Hostname matches configuration | Correct website is delivered |
| Hostname not found | Default website is shown |

This allows many domains to coexist on one server efficiently.

---

### Static vs Dynamic Content

| **Type** | **Description** | **Examples** |
|-----------|------------------|---------------|
| **Static Content** | Files that never change once uploaded | Images, CSS, JavaScript, fixed HTML |
| **Dynamic Content** | Generated or updated in real-time | Blog posts, user profiles, search results |

Dynamic content is generated in the **Backend** using logic and code, while static content is served directly as-is.  
You can view static content in a page’s source code, but **backend logic** remains hidden — that’s why it’s called “behind the scenes.”

---

### Scripting and Backend Languages

**Backend languages** bring websites to life by enabling interactivity, user management, and database operations.

Common backend languages include:

- **PHP**  
- **Python**  
- **Ruby**  
- **NodeJS (JavaScript runtime)**  
- **Perl**  

These languages handle tasks like processing user input, interacting with APIs, and managing stored data — forming the backbone of modern web applications.

---

### Takeaway

This section ties together the full web architecture — from **DNS and HTTP** to **load balancers**, **CDNs**, and **databases**.  
It highlights how front-end requests travel through multiple layers of optimization, security, and logic before a single webpage appears.  
Understanding this chain reveals not only how websites function but also where vulnerabilities and performance bottlenecks often hide.
