# 🌍 How a Website Works

Understanding how a website works is one of the first steps in web development. Every time you visit a website, several processes happen behind the scenes to display the webpage in your browser.

---

# 📌 What is a Website?

A website is a collection of web pages that are stored on a **web server** and accessed through the **Internet** using a **web browser**.

Examples:
- Google
- YouTube
- GitHub
- Amazon

---

# 🧩 Main Components

## 1. Client (Browser)

The client is the user's web browser that requests a webpage.

Examples:
- Google Chrome
- Mozilla Firefox
- Microsoft Edge
- Safari

The browser sends a request to the server and displays the webpage.

---

## 2. Internet

The Internet is the network that connects your device to web servers around the world.

---

## 3. DNS (Domain Name System)

Humans remember domain names like:

```
www.google.com
```

Computers understand only IP addresses like:

```
142.250.193.78
```

DNS converts the domain name into its corresponding IP address.

---

## 4. Web Server

A web server stores website files such as:

- HTML
- CSS
- JavaScript
- Images
- Videos

When a browser requests a webpage, the server sends these files back.

Examples of web servers:

- Apache
- Nginx
- IIS

---

## 5. HTTP / HTTPS

HTTP stands for **HyperText Transfer Protocol**.

It is the communication protocol used between the browser and the server.

HTTPS is the secure version of HTTP that encrypts the data being transferred.

---

# 🔄 How a Website Loads

```
User
   │
   ▼
Enter URL
(example.com)
   │
   ▼
DNS finds IP Address
   │
   ▼
Browser sends HTTP Request
   │
   ▼
Web Server receives request
   │
   ▼
Server sends HTML, CSS & JavaScript
   │
   ▼
Browser renders the webpage
```

---

# 🚀 Step-by-Step Process

### Step 1

The user enters a website URL.

Example:

```
https://www.github.com
```

---

### Step 2

The browser contacts the DNS server to find the IP address.

```
github.com
      │
      ▼
140.82.xxx.xxx
```

---

### Step 3

The browser sends an HTTP/HTTPS request to the web server.

```
GET /
```

---

### Step 4

The server processes the request and sends back the required files.

```
HTML

CSS

JavaScript

Images
```

---

### Step 5

The browser reads the HTML file.

It creates the page structure.

---

### Step 6

The browser downloads the CSS file.

CSS styles the webpage.

Examples:

- Colors
- Fonts
- Layout
- Animations

---

### Step 7

The browser downloads JavaScript.

JavaScript adds functionality like:

- Buttons
- Forms
- Popups
- API Calls
- Sliders

---

### Step 8

Finally, the browser combines everything and displays the webpage to the user.

---

# 🎨 Role of HTML, CSS and JavaScript

| Technology | Purpose |
|------------|---------|
| HTML | Structure of the webpage |
| CSS | Styling and layout |
| JavaScript | Interactivity and functionality |

---

# 📦 Static Website

A static website always shows the same content.

Example:

Portfolio website

Flow:

```
Browser
    │
    ▼
Server
    │
    ▼
HTML + CSS + JS
```

---

# ⚡ Dynamic Website

A dynamic website generates content based on user requests.

Examples:

- Instagram
- Facebook
- Amazon
- YouTube

Flow:

```
Browser
    │
    ▼
Backend Server
    │
    ▼
Database
    │
    ▼
Response
```

---

# 🗄️ Database

Dynamic websites store data in databases.

Examples:

- MySQL
- PostgreSQL
- MongoDB

Data stored includes:

- Users
- Passwords (encrypted)
- Posts
- Products
- Orders

---

# 📡 Request and Response

### Request

Sent from the browser to the server.

Example:

```
GET /about
```

### Response

Sent from the server back to the browser.

Example:

```
200 OK
```

---

# 🖼️ Complete Website Flow

```
User
 │
 ▼
Browser
 │
 ▼
DNS
 │
 ▼
Web Server
 │
 ▼
Backend
 │
 ▼
Database
 │
 ▼
Backend
 │
 ▼
Browser
 │
 ▼
User sees the webpage
```

---

# 📚 Key Terms

- Website
- Browser
- Client
- Server
- DNS
- Domain Name
- IP Address
- HTTP
- HTTPS
- HTML
- CSS
- JavaScript
- Backend
- Database

---

# 🎯 Summary

When a user enters a website URL, the browser first finds the server using DNS. It then sends an HTTP/HTTPS request to the server. The server responds with the required files (HTML, CSS, JavaScript, images, or data). Finally, the browser renders these files and displays the webpage. For dynamic websites, the backend communicates with a database before sending the response.

---

⭐ **Learning Status:** Completed ✅