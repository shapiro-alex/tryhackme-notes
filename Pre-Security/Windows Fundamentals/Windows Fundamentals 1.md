# Windows Fundamentals 1

## File System
- Windows uses NTFS  
- FAT still used on USB drives and SD cards  
- NTFS supports journaling, large files, permissions, compression, EFS  

### NTFS Permissions
- types: full control, modify, read and write, read and execute, list folder contents  
- view with: properties > security tab  

### Alternate Data Streams (ADS)
- NTFS supports multiple data streams  
- sometimes used to hide data  
- Windows Explorer does not show ADS  
- PowerShell can view ADS  
- internet downloads store metadata in ADS  

## System Folders
- `C:\Windows` is the main OS folder  
- referenced using `%windir%`  
- environment variables store OS info  
- `System32` contains critical OS files  
- many tools are located in `System32`  

## Windows User Accounts
- two types: Administrator and Standard User  
- Admin: system changes, install programs, add or remove users  
- Standard: modify own files only  

## Viewing and Managing Accounts
- open Start > other users  
- change account type in user settings  

## User Profiles
- stored in `C:\Users\username`  
- created on first login  
- common folders: Desktop, Documents, Downloads, Music, Pictures  

## Local Users and Groups
- open with `lusrmgr.msc`  
- contains users and groups  
- users inherit group permissions  

## User Account Control (UAC)
- many home users run as local admins  
- malware executed by admin can make system changes  
- UAC requires confirmation for elevated tasks  
- built in admin account is not affected  
- standard users see shield icons  
- UAC prompts for admin credentials  
