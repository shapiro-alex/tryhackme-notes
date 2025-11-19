# Windows Fundamentals 2

## MSConfig (System Configuration)
- used for advanced troubleshooting  
- helps diagnose startup issues  
- requires administrator rights  
- open with `msconfig`  
- launch via Start menu or Run  

### Tabs
- general: choose startup mode  
- boot: set OS boot options  
- services: shows all system services  
- startup: most management done in Task Manager  
- tools: quick launcher for Windows tools  

## control.exe
- opens Control Panel  

## Computer Management
- open with `compmgmt.msc`  

### System Tools
- task scheduler: runs programs or scripts automatically  
- event viewer: shows system events (error, warning, information, success audit, failure audit)  
- shared folders: view shared folders and active sessions  
- local users and groups: manage local accounts  
- performance monitor (`perfmon`): view performance in real time or logs  
- device manager: manage hardware and drivers  

## Storage
- disk management: manages drives and partitions  
  - create drive  
  - extend or shrink partition  
  - change drive letter  

## Services
- start or stop services  
- view properties  

## WMI Control
- manages WMI  
- used for system management with scripts or PowerShell  
- `WMIC` is deprecated  

---

## System Information (msinfo32)
- open with `msinfo32.exe`  
- shows full system details  
- sections: hardware resources, components, software environment  

### System Summary
- general specs (CPU, model, RAM)  

### Hardware Resources
- low-level hardware data  

### Components
- hardware devices (display, input, etc.)  

### Software Environment
- installed software, drivers, environment variables, network connections  

## Environment Variables
- store OS data: paths, temp folders, processor count, Windows directory  
- view using `msinfo32` or Control Panel  
  - system > advanced system settings > environment variables  

## Search Bar
- bottom search inside System Information  
- example: search “IP address” under Components  

## Resource Monitor (resmon)
- shows detailed CPU, memory, disk, and network usage per process  
- shows file handles and modules used  
- can filter processes, manage services, close hung apps  
- helps find deadlocks and file lock conflicts  
- tabs: CPU, memory, disk, network  
- right panel: real-time graphs  

---

## Windows Registry
- open with `regedt32.exe`  
- central database storing system, user, application, and hardware settings  
- Windows reads it constantly  

### Stores information on
- user profiles  
- installed apps and file types  
- folder and icon settings  
- hardware info  
- past usage  
- tool: `regedit`  

---

## Command Prompt (cmd)
- early OSes were command-line only; GUI came later  
- used for system and network commands  

### Basic Commands
- `hostname` - computer name  
- `whoami` - logged-in user  
- `cls` - clear screen  

### Troubleshooting Commands
- `ipconfig` - network settings  
- `ipconfig /?` - help  
- `netstat` - protocol stats and active TCP connections  
  - parameters include `-a` `-b` `-e` etc.  
- `ipconfig /all` - detailed info  

### net Command
- manages network resources  
- `net` alone shows subcommands  
- `net help` for help  
- examples:  
  - `net help user`  
  - `net help localgroup`  
  - `net help share`  
