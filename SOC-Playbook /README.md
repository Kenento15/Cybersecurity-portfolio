# SOC Playbook

This SOC Playbook outlines the procedures and workflows for handling various types of security incidents within a Security Operations Center (SOC). It is designed to standardize response actions and ensure consistency, speed, and efficiency.

---

## Objectives

- Standardize incident response processes across the SOC.
- Provide Tier 1 and Tier 2 analysts with step-by-step procedures.
- Reduce MTTR (Mean Time to Respond) through repeatable workflows.

---

## Sample Playbook Workflows

### 1. **Phishing Email Detection**
- **Detection Source:** Email security gateway / user report
- **Triage Steps:**
  - Analyze email headers and content
  - Check URLs against threat intel feeds
  - Examine attachments in a sandbox
- **Response Actions:**
  - Quarantine email
  - Notify user
  - Add IOCs to denylist
  - Escalate if multiple users impacted

---

### 2. **Malware Detected on Endpoint**
- **Detection Source:** EDR alert (e.g., CrowdStrike, SentinelOne)
- **Triage Steps:**
  - Review file hash and process tree
  - Determine scope: single endpoint or lateral movement?
- **Response Actions:**
  - Isolate endpoint
  - Initiate full scan and remove malware
  - Collect memory dump (if needed)
  - Reimage (if critical)

---

### 3. **Suspicious Login Activity**
- **Detection Source:** SIEM alert / identity provider logs
- **Triage Steps:**
  - Verify login time, location, device fingerprint
  - Review user behavior for anomalies
- **Response Actions:**
  - Force logout / password reset
  - Disable account temporarily
  - Investigate further and monitor for persistence

---

## Tools Used
- Splunk / QRadar / Microsoft Sentinel
- CrowdStrike / Defender ATP
- Email security gateways
- PowerShell & Python for automation

---

## Outcome
Established repeatable incident response templates to reduce time-to-containment and minimize alert fatigue.
