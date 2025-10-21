# WHAT IS DNS?

**Date:** 2025-10-15

---

### Introduction

The **Domain Name System (DNS)** provides a simple way for us to communicate with devices on the Internet without remembering complex IP addresses.  
Every computer connected to the Internet has a unique identifier called an **IP address**. Instead of remembering something like `104.26.10.229`, you can simply remember `tryhackme.com`.

---

### Top-Level Domain (TLD)

A **Top-Level Domain (TLD)** is the rightmost part of a domain name.  
For example, in `tryhackme.com`, the TLD is `.com`.

There are two main types of TLDs:

- **gTLD (Generic Top-Level Domain):**  
  Historically used to indicate a domain’s purpose — e.g., `.com` for commercial, `.org` for organizations, `.edu` for education, `.gov` for government.
- **ccTLD (Country Code Top-Level Domain):**  
  Used to represent geographic locations — e.g., `.ca` for Canada, `.co.uk` for the United Kingdom, etc.

---

### Second-Level Domain

Using `tryhackme.com` as an example, `.com` is the TLD, and `tryhackme` is the **Second-Level Domain**.  
When registering a domain, the second-level domain:

- Is limited to **63 characters + TLD**
- Can only include **a–z, 0–9, and hyphens**
- **Cannot** start or end with a hyphen
- **Cannot** contain consecutive hyphens

---

### Subdomain

A **subdomain** sits to the left of the Second-Level Domain, separated by a period.  
For example, in `admin.tryhackme.com`, the `admin` part is the subdomain.

Subdomains follow the same restrictions as Second-Level Domains:  
limited to 63 characters, only a–z, 0–9, and hyphens, and no leading/trailing/consecutive hyphens.

---

### DNS Record Types

DNS isn’t just used for websites — it stores many different types of records.  
Below are the most common ones:

| **Record Type** | **Purpose** | **Example** |
|------------------|-------------|--------------|
| **A Record** | Resolves to an **IPv4 address** | `104.26.10.229` |
| **AAAA Record** | Resolves to an **IPv6 address** | `2606:4700:20::681a:be5` |
| **CNAME Record** | Resolves to another **domain name** | `store.tryhackme.com → shops.shopify.com` |
| **MX Record** | Defines **mail servers** for a domain | `alt1.aspmx.l.google.com` (includes a priority value for failover) |
| **TXT Record** | Stores **text-based data** | Used for domain verification, SPF records, or anti-spam purposes |

---

### What Happens When You Make a DNS Request

When you request a domain name, your computer first checks its **local DNS cache** to see if you’ve recently looked it up.  
If not found, it contacts your **Recursive DNS Server** (usually provided by your ISP, though you can choose your own).

1. **Local Cache Check:**  
   Your machine checks for cached results. If found, the process ends here.

2. **Recursive DNS Query:**  
   If not cached locally, your request is sent to a **Recursive DNS Server**.  
   If it’s a popular domain (like Google or Facebook), the answer is often already cached there.

3. **Root Server Query:**  
   If the Recursive Server doesn’t have the answer, it contacts a **Root DNS Server**, which directs it to the correct **TLD Server** (e.g., `.com`).

4. **TLD Server Query:**  
   The TLD Server points to the **Authoritative Name Server** responsible for the domain.

5. **Authoritative Name Server:**  
   This server holds the official DNS records for the domain.  
   For example, `tryhackme.com` uses `kip.ns.cloudflare.com` and `uma.ns.cloudflare.com` as its nameservers.

6. **Response and Caching:**  
   The record is sent back to the Recursive Server, cached locally for future use, and then returned to your device.

All DNS records include a **TTL (Time To Live)** value — the number of seconds a response can be cached before it must be re-queried.

---

### Takeaway
A straightforward but essential topic, DNS finally clicks as the silent backbone that turns names into network routes. It's one of those things I always used but never really thought about. Understanding how the lookup chain works—from cache to root to authoritative server—makes it clear how much happens behind a single web request.