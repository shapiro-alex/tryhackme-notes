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

## File and Disk Management  
`cd` – change directory  
  - `..` – go up one level  

`dir` – view child directories  
  - `/a` – displays hidden and system files as well  
  - `/s` – displays files in current dir and all subdirs  

`tree` – visually represent the child directories and subdirectories  
`mkdir` - make a directory  
`rmdir` - remove a directory  
`type` - view a file  
`copy` - copy a file  
`move` - move a file  
`del` `erase` - delete a file  

## Process Management
`tasklist` – list running processes  
  - `/FI "imagename eq name.exe"` – filter by image name  

`taskkill` – terminate a process  
  - `/PID` – specify the process ID to kill  

## Additional Useful Commands  
`chkdsk` – checks the file system and disk volumes for errors and bad sectors  
`driverquery` – displays a list of installed device drivers  
`sfc /scannow` – scans system files for corruption and repairs them  

## Help and Output Navigation  
`command /?` – display help page for most commands  
`more file.txt` – display text files one page at a time  
`some_command | more` – pipe long output to view it page by page  

## Shutdown Commands
`shutdown /r` – restart the system  
`shutdown /a` – abort a scheduled shutdown  
