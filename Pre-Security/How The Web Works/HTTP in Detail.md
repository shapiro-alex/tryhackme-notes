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
