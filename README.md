# SIEM Detection Rules

A collection of production-ready detection rules for **Splunk**, **Microsoft Sentinel**, and **Google Chronicle**, mapped to the MITRE ATT&CK framework. Built from hands-on experience in security operations within a healthcare environment.

## Repository Structure

```
siem-detection-rules/
├── splunk/
│   ├── credential-attacks.spl
│   ├── lateral-movement.spl
│   ├── persistence.spl
│   ├── data-exfiltration.spl
│   └── ransomware-indicators.spl
├── sentinel/
│   ├── credential-attacks.kql
│   ├── lateral-movement.kql
│   ├── persistence.kql
│   ├── data-exfiltration.kql
│   └── ransomware-indicators.kql
├── chronicle/
│   ├── phishing-detection.yaral
│   └── privilege-escalation.yaral
├── testing/
│   └── sample-log-notes.md
└── README.md
```

## Rule Coverage

| Rule Set | Platform | MITRE Tactic | MITRE Technique |
|---|---|---|---|
| Credential Attacks | Splunk, Sentinel | Credential Access | T1110, T1078 |
| Lateral Movement | Splunk, Sentinel | Lateral Movement | T1021, T1550 |
| Persistence | Splunk, Sentinel | Persistence | T1547, T1053 |
| Data Exfiltration | Splunk, Sentinel | Exfiltration | T1048, T1567 |
| Ransomware Indicators | Splunk, Sentinel | Impact | T1486, T1490 |
| Phishing Detection | Chronicle | Initial Access | T1566 |
| Privilege Escalation | Chronicle | Privilege Escalation | T1068, T1078 |

## Platform Notes

- **Splunk** — Rules use SPL (Search Processing Language). Tested against Windows Security and Sysmon event logs.
- **Microsoft Sentinel** — Rules use KQL (Kusto Query Language). Designed for use with Microsoft Defender and Azure AD log sources.
- **Google Chronicle** — Rules use YARA-L 2.0. Designed for UDM (Unified Data Model) event sources.

## MITRE ATT&CK Navigator

All rules in this repository map to the [MITRE ATT&CK Enterprise Matrix](https://attack.mitre.org/). Technique IDs are referenced in every rule file header.

## Usage

Each rule file contains:
- Rule description and intent
- MITRE ATT&CK mapping
- Log source requirements
- The query / rule
- Tuning notes to reduce false positives

Rules should be reviewed and tuned for your environment before deployment in production.

## Author

**Athulya Preetha Subhash**
Data Security Specialist | MSc Cybersecurity
Dublin, Ireland
[LinkedIn](https://www.linkedin.com/in/athulya-subhash-11106b149/) | [GitHub](https://github.com/athulya99)
