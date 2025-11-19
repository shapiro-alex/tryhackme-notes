# Linux Fundamentals Part 3

## Summary
Text editors, useful utilities, processes, system management, automation, packages, and log locations.

## Terminal Text Editors
- `nano` - file editor  
  - `nano filename` - edit file  
- `vim` - advanced text editor  

## Useful Utilities
- `wget` - download from web using HTTP  
- `scp` - secure copy between two computers  
  - IP of remote system  
  - user on remote system  
  - file on local system  
  - name to store file on remote system  
- `python3 -m http.server` - start simple web server  

## Processes
- programs running on the machine  
- managed by the kernel  
- each process has a PID  
- `ps` - list processes  
- `ps aux` - system processes  
- `top` - realtime stats  

### Killing Processes
- `kill PID` - end a process  
- SIGTERM - cleanup before stopping  
- SIGKILL - force kill  
- SIGSTOP - stop or suspend  

## PID and Systemd
- PID 1 - starts at boot, manages other processes  
- systemd - one of the first processes started  
  - other programs run as child processes of systemd  

## systemctl
- used to interact with systemd services  
- format: `systemctl [option] [service]`  
- example: `systemctl start apache2`  
- options:  
  - start  
  - stop  
  - enable  
  - disable  

## Automation
- `crontab -e` - manage crontabs  

## Package Management
- `apt` - package management software  

## Logs
- `/var/log` - main log directory  
  - access logs  
  - error logs  
- system logs - auth attempts and OS activity
