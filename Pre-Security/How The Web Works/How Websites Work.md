# How Websites Work

## What Happens When You Visit a Website
- your browser sends a request to a **web server**
- server responds with data the browser uses to display the page
- a web server is just a computer handling these requests

## Two Parts of a Website

## Front End (Client-Side)
- what the browser renders
- HTML, CSS, JavaScript

## Back End (Server-Side)
- server processes requests
- returns data to the browser

## Core Idea
- browser makes request -> server sends response -> browser shows page

---

## Website Languages
- **HTML** -> structure
- **CSS** -> styling
- **JavaScript** -> interactivity

## HTML Basics
- HTML = language websites are written in
- pages built with **elements (tags)**

## Standard HTML Structure
- `<!DOCTYPE html>` -> tells browser to use HTML5
- `<html>` -> root element
- `<head>` -> page info (title, metadata)
- `<body>` -> content shown in browser
- `<h1>` -> heading
- `<p>` - paragraph

## Tag Attributes
- **class** -> used for styling (not unique)
- **id** -> unique identifier for element
- **src** -> used on images for file location
- elements can have multiple attributes

## Viewing HTML
- right-click -> "View Page Source" (Chrome)
- Safari -> "Show Page Source"

--

## JavaScript Basics
- JS adds **interactivity** to web pages
- HTML = structure, JS = functionality
- allows real-time updates (change text, colors, animations, etc.)

## How JS Is Included
- inside `<script>` tags
- or external file:
  `<script src="/path/file.js"></script>`

## Simple Example
- change element with id **demo**:
  `document.getElementById("demo").innerHTML = "Hack the Planet";`

## Events
- HTML elements can trigger JS with events (onclick, onhover, etc.)
- example:
  - `<button onclick='document.getElementById("demo").innerHTML="Button Clicked";'>Click Me!</button>`
- events can also be defined *inside* JS instead of inline

---

## Sensitive Data Exposure
- happens when websites expose **clear-text sensitive info** in frontend code
- HTML/JS source may contain credentials, debugging info, hidden links, etc.
- attackers can view page source to find:
  - commented-out passwords
  - admin URLs
  - API keys
  - test accounts

## Why It's Dangerous
- exposed data can let attackers access other parts of the site
- credentials may work on login pages or backend systems

## What To Do When Assessing
- always check **View Page Source**
- inspect HTML + JS for:
  - comments
  - unused code
  - hidden fields
  - leaked keys or tokens
 
---

## HTML Injection
- happens when **unfiltered user input** is shown on the page
- attacker can inject **HTML or JavaScript** into output
- caused by missing/weak **input sanitisation**

## Why It Happens
- website uses user input directly in HTML/JS
- browser renders input as real HTML

## Risks
- attacker changes page appearance
- can run client-side JS
- can lead to more serious client-side attacks

## Prevention
- never trust user input
- sanitise: remove/escape HTML tags before using input
