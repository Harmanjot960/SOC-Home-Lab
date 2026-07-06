# SOC Home Lab

## Objective

This project documents the setup of a personal Security Operations Center (SOC) home lab built to simulate a real-world monitoring environment. The lab was designed to collect endpoint telemetry, centralize logs, and support hands-on security investigations using Splunk as the SIEM platform.

---

## Lab Architecture

```text
Windows 10 Virtual Machine
          │
          ▼
       Sysmon
(System Activity Monitoring)
          │
          ▼
 Windows Event Logs
          │
          ▼
Splunk Universal Forwarder
          │
          ▼
   Splunk Enterprise
(Log Collection & Analysis)
```

---

## Components

- Windows 10 Virtual Machine
- Sysmon (Microsoft Sysinternals)
- Splunk Universal Forwarder
- Splunk Enterprise

---

## Telemetry Collected

The lab captures and analyzes several sources of endpoint telemetry, including:

- Process Creation (Sysmon Event ID 1)
- Network Connections (Sysmon Event ID 3)
- File Creation Events
- Windows Security Events (4624, 4625, etc.)
- System and Application Logs

---

## Data Flow

1. User activity is generated on the Windows endpoint.
2. Sysmon records detailed endpoint telemetry.
3. Windows Event Logs store security and system events.
4. Splunk Universal Forwarder forwards the logs to Splunk Enterprise.
5. Splunk indexes the data for investigation and analysis.

---

## Investigation Capabilities

This lab provides the foundation for investigating common security incidents, including:

- Phishing attacks
- PowerShell-based attacks
- Brute-force authentication attempts
- Botnet activity
- Windows endpoint investigations

---

## Skills Demonstrated

- SIEM log analysis using Splunk
- SPL (Search Processing Language)
- Endpoint monitoring with Sysmon
- Windows Event Log analysis
- Log collection and forwarding
- Threat detection and investigation
- Incident response fundamentals

---
## Related Projects

This home lab provides the logging and monitoring environment used throughout the investigation projects in this portfolio:

- SOC Project 1 – Phishing Investigation
- SOC Project 2 – PowerShell Attack Investigation
- SOC Project 3 – Brute Force Detection
- SOC Project 4 – Botnet Investigation
- SOC Project 5 – End-to-End Incident Response
- 
---

## Summary

This SOC Home Lab demonstrates the deployment of a centralized logging environment for Windows endpoint monitoring using Splunk and Sysmon. It showcases hands-on experience with log collection, threat detection, security monitoring, and incident investigation in a simulated SOC environment.
