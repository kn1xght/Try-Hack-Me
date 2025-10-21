# HTTP IN DETAIL

**Date:** 2025-10-15

---

### Introduction

The **HyperText Transfer Protocol (HTTP)** is the foundation of data communication on the web.  
Developed by **Tim Berners-Lee and his team between 1989–1991**, HTTP defines how web clients (like browsers) and web servers communicate to transfer data — whether that’s **HTML**, **images**, **videos**, or other media types.

---

### What Is HTTPS?

**HTTPS (HyperText Transfer Protocol Secure)** is the encrypted version of HTTP.  
While HTTP sends data in clear text, HTTPS uses encryption (typically via **TLS/SSL**) to:

- Prevent eavesdropping on transmitted data  
- Authenticate that you’re communicating with the **correct web server** and not an imposter  
- Protect data integrity and privacy during transfer

---

### URLs (Uniform Resource Locators)

A **URL** provides a standardized way to locate and access resources on the internet.  
It acts as an instruction for how to reach a specific file or service.

#### Components of a URL

| **Component** | **Description** | **Example** |
|----------------|-----------------|--------------|
| **Scheme** | Protocol used to access the resource | `http`, `https`, `ftp` |
| **User** | Credentials for services requiring authentication | `user:pass@host.com` |
| **Host** | Domain name or IP address of the target server | `tryhackme.com` |
| **Port** | Network port used to connect (default: 80 for HTTP, 443 for HTTPS) | `:443` |
| **Path** | Location of the resource on the server | `/images/logo.png` |
| **Query String** | Extra parameters sent to the resource | `/blog?id=1` |
| **Fragment** | Reference to a specific part of the page | `/guide#section2` |

---

### Making a Request

Every time you visit a website, your browser sends a **request** to a web server and receives a **response** back.

A simple HTTP request could be as short as:

```
GET / HTTP/1.1
```

However, real-world requests include **headers** — extra lines of information that tell the server about the client and the nature of the request.

### Example Request

```
GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referer: https://tryhackme.com/
```

**Explanation:**
1. `GET / HTTP/1.1` — Requesting the home page using HTTP version 1.1  
2. `Host:` — Specifies the domain being requested  
3. `User-Agent:` — Identifies the browser and version  
4. `Referer:` — Indicates the page that linked to this one  
5. A blank line signals the **end of the request**

---

### Example Response

```
HTTP/1.1 200 OK
Server: nginx/1.15.8
Date: Fri, 09 Apr 2021 13:34:03 GMT
Content-Type: text/html
Content-Length: 98

<html>
<head>
    <title>TryHackMe</title>
</head>
<body>
    Welcome To TryHackMe.com
</body>
</html>
```

**Explanation:**
1. `HTTP/1.1 200 OK` — Protocol version + **status code** (success)  
2. `Server:` — The web server software and version  
3. `Date:` — Timestamp of the response  
4. `Content-Type:` — Type of content being sent (HTML, image, video, etc.)  
5. `Content-Length:` — Size of the response body in bytes  
6. Blank line — Marks end of headers  
7. Remaining lines — The **actual data** (HTML of the homepage)

---

### HTTP Methods

HTTP methods define the action a client wants to perform.  
Here are the most common ones:

| **Method** | **Purpose** |
|-------------|-------------|
| **GET** | Retrieve data from the web server |
| **POST** | Submit data to create new records |
| **PUT** | Update existing information |
| **DELETE** | Remove information from the server |

---

### HTTP Status Codes

Status codes indicate how the server responded to a client’s request.

| **Range** | **Category** | **Meaning** |
|------------|---------------|--------------|
| 100–199 | **Informational** | Request received; continue sending data |
| 200–299 | **Success** | Request completed successfully |
| 300–399 | **Redirection** | Client should look elsewhere for the resource |
| 400–499 | **Client Errors** | Issue with the client’s request |
| 500–599 | **Server Errors** | Problem on the server side |

### Common HTTP Status Codes

| **Code** | **Meaning** |
|-----------|-------------|
| **200** | OK — Request succeeded |
| **201** | Created — Resource created successfully |
| **301** | Moved Permanently — Resource moved to new location |
| **302** | Found — Temporary redirect |
| **400** | Bad Request — Invalid or missing parameters |
| **401** | Unauthorized — Authentication required |
| **403** | Forbidden — Access denied |
| **404** | Not Found — Resource doesn’t exist |
| **405** | Method Not Allowed — Wrong HTTP method used |
| **500** | Internal Server Error — Generic server failure |
| **503** | Service Unavailable — Server overloaded or under maintenance |

---

### Headers

Headers are **key-value pairs** sent with HTTP requests and responses to provide context, control caching, manage sessions, and more.

### Common Request Headers

| **Header** | **Purpose** |
|-------------|-------------|
| **Host** | Specifies which domain is being requested |
| **User-Agent** | Identifies the browser or client software |
| **Content-Length** | Specifies the size of data being sent to the server |
| **Accept-Encoding** | Lists compression methods supported by the client |
| **Cookie** | Sends stored session data back to the server |

### Common Response Headers

| **Header** | **Purpose** |
|-------------|-------------|
| **Set-Cookie** | Sends cookie data to be stored on the client |
| **Cache-Control** | Defines how long content should be cached |
| **Content-Type** | Declares the data format (HTML, JSON, PDF, etc.) |
| **Content-Encoding** | Specifies compression method used |

---

### Cookies

**Cookies** are small pieces of data stored on your device, sent by a web server via the `Set-Cookie` header.  
Since HTTP is **stateless**, cookies provide a way to maintain session data between requests.

They can store:

- **Authentication tokens**
- **User preferences**
- **Session identifiers**

Cookies are typically encrypted tokens rather than human-readable data, ensuring privacy and preventing direct access to sensitive information.

---

### Takeaway

This module makes it clear that **HTTP** isn’t just “how websites load” — it’s a structured language for communication between clients and servers.  
Understanding **methods, headers, and status codes** gives insight into how every browser action, API call, or login request actually travels across the web.  
It’s the silent protocol that powers the modern internet, one request and response at a time.