# Incident Response Simulation – Ransomware Attack

## Overview
This project simulates a ransomware attack scenario to demonstrate structured incident response using a simplified playbook and forensic analysis techniques.

## Tools Used
- Splunk (for log analysis)
- Wireshark (network traffic inspection)
- CyberChef (quick analysis)
- Windows 10 VM (compromised host)
- FTK Imager (disk image capture)

## Incident Scenario
A user reported their files were renamed with a `.locked` extension and ransom note appeared on the desktop. Alerts from the SIEM suggested a suspicious PowerShell script was executed.

## Incident Response Phases

### 1. Identification
- Detected unusual network traffic and PowerShell behavior via Splunk.
- Verified IOCs: Suspicious domain, IP, file hash, and registry changes.

### 2. Containment
- Isolated affected endpoint from the network.
- Disabled the affected user’s credentials.

### 3. Eradication
- Located and removed ransomware binaries and malicious scheduled tasks.
- Blocked malicious IP addresses and domains via firewall.

### 4. Recovery
- Restored clean backups to the system.
- Re-enabled user access after system integrity was confirmed.

### 5. Lessons Learned
- Attack vector was an email attachment with macro-enabled Excel file.
- Endpoint lacked up-to-date EDR coverage.
- Need for stronger email filtering and security awareness training.

## Outcome
- Contained and remediated the ransomware incident with minimal business impact.
- Updated IR playbook to address gaps.
- Shared report with leadership and implemented improved detection rules.

## Next Steps
- Conduct tabletop exercises to test response readiness.
- Automate IOC enrichment and alerting for faster triage.
- Enforce strict macro policies in email attachments.

---

