# Linux Fundamentals Part 2

## Summary
SSH access, flags and switches, help manuals, file operations, permissions, switching users, and common directories.

## SSH Access
- SSH = Secure Shell  
- encrypted protocol between devices  
- input is encrypted during travel and decrypted on the remote machine  
- login format: `ssh user@ip`  
- example: `ssh tryhackme@10.201.47.65`

## Flags and Switches
- commands allow arguments  
- identified by a hyphen and keyword  
- examples:  
  - `ls` - lists the current directory  
  - `ls -a` - lists all files including hidden  

## Help and Manuals
- `command --help` - list options and descriptions  
- `man` - manual command  
- `man <command>` - show documentation  
- example: `man ls`

## File Operations
- `touch` - create file  
- `mkdir` - create folder  
- `cp` - copy  
- `mv` - move  
- `rm` - remove file  
- `rm -r` - remove directory  

## Permissions
- `ls -l` - show file permissions  
- example: `ls -lh`

## Switching Users
- `su` - switch user  
- starts a shell similar to the user you switch to  
- new session begins in home directory  

## Common Directories
- `/etc` - one of the most important system directories  
- `/var` - variable data frequently accessed or written by services and applications  
- `/var/log` - log data not tied to a specific user  
- `/root` - home directory for the root user  
- `/tmp` - temporary files used once or twice
