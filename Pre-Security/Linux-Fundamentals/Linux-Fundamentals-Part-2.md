# Linux Fundamentals Part 2

## Summary
Permissions, switching users, common directories, SSH access, command flags, manual pages, and basic file operations.

## Permissions
- `ls -l` shows permissions of all files in a directory  
- example: `ls -lh`

## Switching Users
- `su` - switch user  
- starts a shell similar to user  
- new session begins in home directory

## Common Directories
- `/etc` - one of the most important directories  
- `/var` - variable data, frequently accessed or written by services and apps  
- `/var/log` - log data not tied to a specific user  
- `/root` - home for root user  
- `/tmp` - temporary files, used once or twice  

## SSH Access
- SSH is Secure Shell  
- encrypted protocol between devices  
- data is encrypted during travel and decrypted on arrival  
- login example:  
  - `ssh user@ip`  
  - `ssh tryhackme@10.201.47.65`

## Flags and Switches
- commands allow arguments  
- identified by a hyphen and keyword  
- example:  
  - `ls` - list contents  
  - `ls -a` - list all, including hidden  

## Help and Manuals
- `command --help` shows options and descriptions  
- `man` - manual command  
- `man <command>` - fetch documentation  
- example: `man ls`

## File Operations
- `touch` - create file  
- `mkdir` - create folder  
- `cp` - copy  
- `mv` - move  
- `rm` - remove file  
- `rm -r` - remove directory
