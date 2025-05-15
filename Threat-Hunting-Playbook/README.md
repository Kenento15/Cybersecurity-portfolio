# Threat Hunting Playbook

## Objective
This playbook outlines a structured approach to proactively detect advanced threats in an enterprise environment using tools like Splunk, MITRE ATT&CK, and IOC enrichment.

## Tools Used
- Splunk
- MITRE ATT&CK Framework
- Sysmon
- Sigma rules
- PowerShell

## Use Case
**Scenario**: Unusual outbound traffic detected from endpoints.
- **Goal**: Investigate and identify potential C2 communication or data exfiltration.
- **Approach**:
  - Use Splunk to query outbound connections.
  - Filter non-standard ports and large data transfers.
  - Cross-reference with known malicious IPs and domains (IOC feed).
  - Review PowerShell or script execution via Sysmon logs.

## Sample Query (Splunk)
```spl
index=sysmon EventCode=3 (destination_port!=443 AND destination_port!=80)
| stats count by dest_ip, dest_port, process_name, user

## Outcome
- Detected potential beaconing to suspicious IPs.
- Escalated case to Incident Response team.
- Recommendation: Block IPs, isolate host, perform memory analysis.
