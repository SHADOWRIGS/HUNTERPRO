# 🔴 Defensive Security - Red Team Perspective

## Advanced Persistent Threat (APT) Techniques

### 1. Persistence Mechanisms
- Registry Run Keys
- Scheduled Tasks
- WMI Event Subscriptions
- DLL Hijacking
- Service Creation

### 2. Lateral Movement
- Pass-the-Hash (PtH)
- Pass-the-Ticket (PtT)
- Remote Desktop Protocol (RDP)
- WinRM / PSRemoting
- SMB exploitation

### 3. Credential Harvesting
- Mimikatz techniques
- LSASS dumping
- SAM database extraction
- Cached credentials
- Kerberos ticket extraction

### 4. Defense Evasion
- Process injection
- DLL injection
- Process hollowing
- Reflective DLL loading
- Obfuscation techniques

### 5. Command & Control (C2)
- DNS tunneling
- HTTPS beaconing
- Domain fronting
- Fast flux networks
- Encrypted channels

## Red Team Tools
- Cobalt Strike
- Empire/Starkiller
- Metasploit Framework
- BloodHound
- Mimikatz

## APT Simulation Exercise
Goal: Simulate APT29 (Cozy Bear) tactics
Target: Corporate network
Duration: 48 hours
Objective: Establish persistence, exfiltrate data

## Detection Indicators
- Unusual network traffic patterns
- Suspicious PowerShell executions
- Abnormal authentication attempts
- New scheduled tasks
- Unauthorized service creations
