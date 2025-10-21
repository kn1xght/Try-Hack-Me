# HOW WEBSITES WORK

**Date:** 2025-10-15

---

### Introduction

When you visit a website, your **browser** (like Safari or Google Chrome) sends a **request** to a **web server** asking for information about the page you’re visiting.  
The web server — a dedicated computer somewhere in the world — responds with data that your browser then renders as the web page you see.

---

### Website Components

Websites are made up of two major parts:

| **Component** | **Description** |
|----------------|-----------------|
| **Front End (Client-Side)** | How your browser renders and displays the website. |
| **Back End (Server-Side)** | Handles processing, logic, and responses to client requests. |

---

### Core Web Technologies

| **Technology** | **Purpose** |
|-----------------|-------------|
| **HTML (HyperText Markup Language)** | Defines the structure and content of a web page. |
| **CSS (Cascading Style Sheets)** | Adds styling and layout to make pages visually appealing. |
| **JavaScript (JS)** | Adds interactivity and dynamic functionality to web pages. |

---

### HTML Basics

**HTML** is the standard markup language used to create web pages. Elements (also called **tags**) define the structure and content that browsers display.

### Common HTML Structure

| **Element** | **Purpose** |
|--------------|-------------|
| `<!DOCTYPE html>` | Declares the document as an HTML5 page (ensures consistent rendering across browsers). |
| `<html>` | Root element — all other tags are nested inside. |
| `<head>` | Contains metadata like the page title, links, and scripts. |
| `<body>` | Contains visible content shown in the browser. |
| `<h1>` | Defines a large heading. |
| `<p>` | Defines a paragraph. |

Other useful tags include buttons (`<button>`), images (`<img>`), and lists (`<ul>`, `<ol>`). Each tag has a specific function that contributes to how content appears and behaves.

---

### JavaScript (JS)

**JavaScript** brings interactivity to web pages. It allows elements to respond dynamically to user actions — like changing the color of a button when it’s clicked or displaying animations.

JavaScript can be embedded directly within a page using `<script>` tags, or loaded externally with the `src` attribute:

```html
<script src="/path/to/javascript_file.js"></script>
```

This flexibility makes JavaScript a powerful tool for creating dynamic and responsive user experiences.

---

### Sensitive Data Exposure

**Sensitive Data Exposure** occurs when a website inadvertently exposes confidential information to users — often visible in the **frontend source code**.

Examples of exposed data might include:

- Login credentials left in HTML comments  
- Hidden links to private areas of the site  
- Tokens or API keys in JavaScript files  

Attackers can exploit such information to gain unauthorized access or escalate privileges within a web application.

Whenever testing a web app’s security, **view the page source** first. Unprotected credentials or hidden elements often provide valuable clues for further analysis.

---

### HTML Injection

**HTML Injection** occurs when user input is inserted into a webpage without proper sanitization.  
If the application fails to **filter malicious input**, attackers can inject HTML or JavaScript into the site.

For example:
- A comment box that displays what users type back onto the page.  
- If a user enters `<h1>Hacked!</h1>`, and it appears as a large heading, the site is vulnerable.

This vulnerability exists because the website **trusts user input** and renders it directly into the page without cleaning it.

### Why It Matters
- Attackers can alter the appearance or structure of a page.  
- They can inject scripts that steal cookies, credentials, or data.  
- It breaks the trust between user and website.

### Prevention
- **Never trust user input.**  
- Sanitize all inputs before displaying them.  
- Remove or escape HTML tags in user-submitted content.

---

### Takeaway

This section illustrates how websites function at every layer — from structure to security.  
Understanding the interaction between **frontend (HTML, CSS, JS)** and **backend** systems reveals how easily unfiltered input or exposed data can become security risks.  
Building websites isn’t just about visuals or functionality — it’s about ensuring that every line of code keeps users and data safe.