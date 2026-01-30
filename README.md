# soc-automation-diagram
# SOC Automation Project (Wazuh + Shuffle + TheHive)

## Overview
This project demonstrates an end-to-end **Security Operations Center (SOC) automation workflow** using **Wazuh**, **Shuffle SOAR**, and **TheHive**.  
The goal is to automate alert ingestion, IOC enrichment, case creation, analyst notification, and response actions to reduce manual effort and improve incident response time.

---

## Architecture
The SOC automation pipeline follows this flow:

1. Windows 11 endpoint generates security events
2. Wazuh Agent forwards events to Wazuh Manager
3. Wazuh Manager sends alerts to Shuffle SOAR
4. Shuffle enriches Indicators of Compromise (IOCs) using external threat intelligence
5. Alerts are forwarded to TheHive for case management
6. Email notifications are sent to the SOC Analyst
7. Analyst reviews the alert and responds
8. Response actions are triggered via Shuffle
9. Wazuh executes automated response actions on the endpoint

---

## Components Used

### Endpoint
- Windows 11 Client
- Wazuh Agent installed for log and security event collection

### SIEM
- Wazuh Manager
- Alert generation and rule-based detection
- Active response capability

### SOAR
- Shuffle
- Alert ingestion from Wazuh
- IOC enrichment
- Workflow automation
- Response orchestration

### Case Management
- TheHive
- Incident and case tracking
- Analyst collaboration

### Notification
- Email integration
- Analyst alerting and response confirmation

---

## Workflow Explanation

### Event Collection
- Wazuh Agent collects logs and security events from the Windows endpoint
- Events are forwarded to the Wazuh Manager

### Alert Generation
- Wazuh Manager analyzes events using rules
- Security alerts are generated and forwarded to Shuffle

### Automation and Enrichment
- Shuffle receives alerts
- Extracts IOCs such as IPs, hashes, and domains
- Enriches IOCs using threat intelligence sources

### Case Creation
- Enriched alerts are sent to TheHive
- A case is automatically created for investigation

### Analyst Interaction
- SOC Analyst receives email notification
- Analyst reviews case details in TheHive
- Analyst decision triggers further actions

### Automated Response
- Shuffle sends response instructions
- Wazuh executes active response actions such as:
  - Blocking IP addresses
  - Isolating endpoints
  - Killing malicious processes

---

## Response Actions Supported
- IP blocking via firewall rules
- Endpoint isolation
- Alert acknowledgment
- Automated remediation using Wazuh active response

---

## Use Cases
- Malware detection and response
- Brute-force attack detection
- Suspicious network activity
- Endpoint compromise investigation
- SOC alert fatigue reduction

---

## Skills Demonstrated
- SIEM implementation and alerting
- SOAR workflow automation
- Incident response orchestration
- Threat intelligence enrichment
- SOC analyst operational flow
- Blue team security operations

---

## Author
Ratnakar  
Cyber Security Enthusiast | SOC | Blue Team | Automation
