# 🔵 Defensive Security - Blue Team Perspective

## Threat Hunting Methodology

### 1. Hypothesis Generation
- Intelligence-driven hunting
- Anomaly-based hunting
- Indicator-based hunting
- Behavioral analytics

### 2. Data Collection & Analysis
- Log aggregation (SIEM)
- Network traffic analysis
- Endpoint telemetry
- Memory forensics
- File system analysis

### 3. Threat Detection Techniques

#### Network Detection
- Unusual DNS queries
- Suspicious HTTP/HTTPS traffic
- Anomalous data transfers
- C2 beacon identification
- Lateral movement detection

#### Endpoint Detection
- Process creation monitoring
- Registry modifications
- File system changes
- Memory injections
- Privilege escalations

### 4. Incident Response Phases

**Phase 1: Preparation**
- IR team ready
- Playbooks prepared
- Tools available
- Communication channels established

**Phase 2: Identification**
- Alert triage
- Scope determination
- Threat classification
- Impact assessment

**Phase 3: Containment**
- Isolate affected systems
- Block malicious IPs/domains
- Disable compromised accounts
- Network segmentation

**Phase 4: Eradication**
- Remove malware
- Close vulnerabilities
- Patch systems
- Reset credentials

**Phase 5: Recovery**
- Restore from backups
- Verify system integrity
- Monitor for reinfection
- Return to normal operations

**Phase 6: Lessons Learned**
- Post-incident review
- Update procedures
- Document findings
- Improve defenses

## SIEM Detection Rules

### Rule 1: Suspicious PowerShell
Event: PowerShell execution with encoded commands
Condition: CommandLine contains "-enc" OR "-encodedcommand"
Action: Alert + Log + Quarantine
Severity: High
### Rule 2: Lateral Movement
Event: Multiple failed login attempts followed by success
Condition: Failed logins > 5 in 5 minutes, then success
Source: Different IPs
Action: Alert + Block + Investigate
Severity: Critical
### Rule 3: Data Exfiltration
Event: Large data transfer to external IP
Condition: Outbound traffic > 100MB to non-whitelisted IP
Time: Outside business hours
Action: Alert + Block + Capture PCAP
Severity: Critical
## Threat Intelligence Integration
- MISP (Malware Information Sharing Platform)
- STIX/TAXII feeds
- VirusTotal integration
- AlienVault OTX
- Recorded Future

## Blue Team Tools
- Splunk / ELK Stack
- Wireshark / Zeek
- Velociraptor
- OSQuery
- Sysmon
- YARA rules

## Threat Hunting Exercise
Duration: 4 hours
Objective: Hunt for APT activity in network
Dataset: 7 days of logs
Expected findings: C2 beacons, credential dumping
