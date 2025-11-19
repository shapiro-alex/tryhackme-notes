# Windows Fundamentals Part 3

## Windows Update
- provides Windows and Microsoft product security and feature updates  
- main release day: Patch Tuesday (2nd Tuesday)  
- critical fixes can release anytime  
- open via Settings or Control Panel → Windows Update  
- Windows 10+: updates must install eventually, auto-reboot required  

## Windows Security
- central hub for built-in protection  
- main sections: virus and threat protection, firewall and network protection, app and browser control, device security  
- status icons: green = good, yellow = review, red = urgent  

### Virus and Threat Protection
- scan types: quick, full, custom  
- threat history shows past scans, quarantined items, allowed items  
- settings include: real-time, cloud protection, sample submit, controlled folder access, exclusions  
- updates manage Defender definitions  
- ransomware protection requires real-time + controlled folder access  
- tip: right-click a file → scan with Defender  

---

## Firewall
- controls what traffic is allowed through ports  
- profiles:  
  - domain → workplace networks  
  - private → home/trusted networks  
  - public → default, untrusted networks (airports, cafés)  
- each profile allows enabling/disabling firewall and blocking incoming connections  
- keep firewall on unless you fully know what you're doing  
- advanced settings tool: `wf.msc`  

## App & Browser Control
- SmartScreen protects against phishing, malware, and malicious downloads  
- checks apps and files from the web  
- exploit protection defends against exploit-based attacks  
- keep defaults unless you fully know what you're doing  

## Device Security
- core isolation / memory integrity protects high-security processes from malicious code  
- security processor (TPM) performs cryptographic operations and checks system integrity  

## BitLocker
- full drive encryption for lost or stolen devices  
- strongest when used with TPM hardware  
- TPM securely stores keys and verifies system integrity  
- without TPM, BitLocker uses a removable drive containing the startup key  

---

## Volume Shadow Copy Service (VSS)
- VSS creates system snapshots and restore points  
- shadow copies stored in the `System Volume Information` folder  
- when system protection is on, you can create restore points, restore system, configure settings, delete restore points  
- malware/ransomware often deletes shadow copies, so recovery requires offline or off-site backups  
