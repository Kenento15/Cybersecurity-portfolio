# Insider Threat Simulation – Abnormal User Behavior

## Overview
This simulation project focuses on detecting insider threats by monitoring anomalous behavior using SIEM tools and log analysis.

## Objective
Identify and respond to suspicious internal user activities such as off-hours access, mass file downloads, and privilege misuse.

## Tools Used
- SIEM: Splunk / Microsoft Sentinel  
- Audit Logs: Windows Event Viewer, Azure AD, SharePoint  
- Threat Framework: MITRE ATT&CK – T1086, T1059, T1078

## Steps Taken
1. Collected user activity logs from endpoints, file servers, and Azure AD.
2. Used KQL/Splunk queries to detect anomalies:
   - Multiple login attempts from different locations
   - Large downloads of internal documents
   - Usage of PowerShell by non-admin accounts
3. Correlated logs across systems to identify behavioral patterns.
4. Simulated user behavior for validation.

## Outcome
- Detected unusual behavior patterns linked to data exfiltration attempts.
- Created a case in the SIEM and initiated incident workflow.
- Recommended privilege revocation and deeper forensic review.

## Takeaway
Regular insider threat simulations strengthen detection capabilities and help refine access policies and user behavior baselines.
