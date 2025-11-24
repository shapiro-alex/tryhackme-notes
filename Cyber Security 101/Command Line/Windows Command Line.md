# Windows Command Line

## Basic System Information
`ver` - determine OS version  
`systeminfo` - list various info about system  

## Network Troubleshooting
`ipconfig` - check network information  
`ipconfig /all` - more information  
`ping` - sends test packets to another device to check if it’s reachable and how long the response takes  
`tracert` - shows the path your packets take to reach a target device  
`nslookup` - looks up a domain and shows its IP address  
`netstat` – shows active network connections and listening ports  
  - `-a` displays all established connections and listening ports  
  - `-b` shows the program associated with each listening port and established connection  
  - `-o` reveals the process ID (PID) associated with the connection  
  - `-n` uses a numerical form for addresses and port numbers  
  - `netstat -abon` combines all four options to show programs, PIDs, ports, and numeric addresses  
