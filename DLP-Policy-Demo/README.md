DLP Policy Simulation – Microsoft Purview
Overview
This project demonstrates how to simulate and test Data Loss Prevention (DLP) policies using Microsoft Purview to detect and prevent sensitive data exfiltration.

Objective
Simulate DLP alerts triggered by attempts to share confidential information via email and cloud storage.

Tools Used

Microsoft Purview DLP

Microsoft 365 Security & Compliance Center

Exchange Online / OneDrive

Sensitive Info Types: Financial Data, Custom Regex Patterns

Steps Taken

Created custom DLP policy in Microsoft Purview.

Defined rules to detect credit card numbers and confidential labels.

Configured rules to trigger alerts and restrict sharing externally.

Sent simulated emails and uploaded test documents containing mock sensitive data.

Reviewed triggered alerts in Microsoft Purview dashboard.

Outcome

Successfully generated DLP alerts.

Verified that external sharing was blocked per policy settings.

Exported audit logs and alerts for documentation.

Takeaway
DLP policies play a vital role in protecting regulated data. Simulating policy behavior helps ensure effectiveness before enforcement.
