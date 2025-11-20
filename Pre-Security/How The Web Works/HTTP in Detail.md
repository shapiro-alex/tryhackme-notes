# HTTP in Detail

### HTTP (HyperText Transfer Protocol)
- rules for communicating with web servers
- used to load HTML, images, videos, etc.
- created 1989-1991 by Tim-Berners-Lee
- **not encrypted** (data visible)

### HTTPS (HyperText Transfer Protocol Secure)
- encrypted version of HTTP
- prevents others from reading traffic
- verifies you're talking to the real server
- protects against impersonation + sniffing

---

## URLs & HTTP Requests

### What is a URL?
- instruction on **how + where** to access a resource
- parts of a URL:
  - **Scheme**: protocol (http, https, ftp)
  - **User**: optional username:password
  - **Host**: domain or IP
  - **Port**: default 80/443, but can be any 1–65535
  - **Path**: file/location (/view-room)
  - **Query**: extra info (?id=1)
  - **Fragment**: section on page (#task3)

### Making an HTTP Request
- browser sends a **request line** + **headers**
- ends with a **blank line**

#### Example Request
```
GET / HTTP/1.1  
Host: tryhackme.com  
User-Agent: Firefox/87  
Referer: https://tryhackme.com/
```

**Notes**
- GET = method  
- `/` = homepage  
- Host = site  
- User-Agent = browser info  
- Referer = previous page  
- blank line = request finished

---

### Example Response
```
HTTP/1.1 200 OK  
Server: nginx  
Date: Fri, 09 Apr 2021  
Content-Type: text/html  
Content-Length: 98  

<html>…</html>
```

**Notes**
- 200 OK = success  
- Server = server software  
- Date = server time  
- Content-Type = HTML, image, etc  
- Content-Length = response size  
- blank line = headers done  
- body = actual content

---

## HTTP Methods (Short Notes)

### GET
- retrieves information from the server  
- most common method  

### POST
- sends data to the server  
- often creates new records  

### PUT
- sends data to update existing information  

### DELETE
- removes information or records from the server

---

## HTTP Status Codes

### Code Ranges
- **100–199** → Info (rare today)
- **200–299** → Success
- **300–399** → Redirection
- **400–499** → Client errors
- **500–599** → Server errors

---

## Common Codes

### 200 – OK  
request succeeded

### 201 – Created  
resource created (new user, new post)

### 301 – Moved Permanently  
redirect to new location (permanent)

### 302 – Found  
temporary redirect

### 400 – Bad Request  
something wrong or missing in the request

### 401 – Not Authorised  
must log in first

### 403 – Forbidden  
logged in or not — still not allowed

### 404 – Not Found  
resource/page does not exist

### 405 – Method Not Allowed  
wrong method (e.g., GET instead of POST)

### 500 – Internal Server Error  
server crashed or misconfigured

### 503 – Service Unavailable  
server overloaded or under maintenance

---

## HTTP Headers

### Request Headers (client → server)
- **Host** — tells server which site you want (when many are hosted)
- **User-Agent** — your browser + version (helps server format content)
- **Content-Length** — size of data you're sending (e.g., form data)
- **Accept-Encoding** — compression types your browser supports
- **Cookie** — stored data sent with each request (session info, prefs)

---

### Response Headers (server → client)
- **Set-Cookie** — server gives browser new cookie data to store
- **Cache-Control** — how long the browser should cache the response
- **Content-Type** - tells browser what type of file is returned (HTML, JS, image, etc.)
- **Content-Encoding** — compression applied to the response (e.g., gzip)

---

# Cookies

## What Are Cookies?
- small pieces of data stored on your computer
- saved when server sends **Set-Cookie** header
- sent back to server on every future request
- used because **HTTP is stateless**

## What Cookies Are Used For
- remembering who you are (authentication)
- storing settings/preferences
- tracking whether you've visited before
- usually stored as **tokens**, not passwords

## Basic Flow
1. client requests webpage
2. server responds, may include **Set-Cookie**
3. browser stores cookie
4. on every request, browser sends `Cookie:` header
5. server uses cookie to identify the user/session
