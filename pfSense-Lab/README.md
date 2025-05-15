# pfSense Lab – Firewall Rule Configuration for LAN Access Control

## Overview
This lab demonstrates how pfSense can be used to enforce network segmentation and control LAN access by configuring firewall rules that block social media websites.

## Objective
Configure pfSense to:
- Block access to Facebook, Instagram, and LinkedIn from LAN
- Allow general web browsing
- Log and monitor blocked traffic

## Tools Used
- pfSense (virtualized)
- LAN test device (Windows 10 VM)
- DNS Resolver, Firewall Rule Sets, Alias Configuration

## Steps Taken

### 1. Environment Setup
- Installed pfSense in a virtual machine.
- Configured two interfaces: WAN (Internet) and LAN (internal network).
- Connected LAN VM to pfSense LAN interface.

### 2. Create Aliases
- Created an alias group for social media domains:
  - `facebook.com`
  - `instagram.com`
  - `linkedin.com`

### 3. Add Firewall Rules
- Created a LAN rule to block all access to the alias group.
- Positioned the rule above the default allow rule.
- Enabled logging for monitoring.

### 4. Testing and Verification
- Attempted to access blocked domains from the LAN VM.
- Confirmed access was denied (connection timeout or refused).
- Checked pfSense firewall logs to validate rule hits.

## Outcome
- Successfully blocked targeted social media sites.
- Improved understanding of rule priority and firewall logic.
- Practiced log analysis and rule debugging.

## Recommendations
- Extend rules to cover HTTPS SNI filtering for better accuracy.
- Implement VLANs for more granular segmentation.
- Integrate with external logging tools (e.g., Splunk, Graylog).

---

