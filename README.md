# SOC Home Lab

## Objective

This project documents the setup of a personal Security Operations Center (SOC) home lab built to simulate a centralized Windows monitoring environment. The lab was designed to collect endpoint telemetry, centralize security logs, and provide hands-on experience with SIEM monitoring and log analysis using Splunk as the primary platform.

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

* Windows 10 Virtual Machine
* Sysmon (Microsoft Sysinternals)
* Windows Event Logs
* Splunk Universal Forwarder
* Splunk Enterprise

---

## Telemetry Collected

The lab collects and analyzes multiple sources of Windows endpoint telemetry, including:

* Process Creation (Sysmon Event ID 1)
* Network Connections (Sysmon Event ID 3)
* File Creation Events
* Windows Security Events (4624, 4625, etc.)
* System and Application Logs

---

## Data Flow

1. User activity occurs on the Windows endpoint.
2. Sysmon records detailed endpoint telemetry.
3. Windows Event Logs store security and system events.
4. Splunk Universal Forwarder forwards collected logs to Splunk Enterprise.
5. Splunk indexes the data for searching, monitoring, and analysis.

---

## Monitoring and Analysis Capabilities

This lab provides a foundation for analyzing Windows endpoint activity, including:

* Process execution monitoring
* PowerShell activity analysis
* Network connection monitoring
* Authentication event analysis
* Suspicious endpoint behavior investigation
* SPL query development

---

## Skills Demonstrated

* SIEM log analysis using Splunk
* SPL (Search Processing Language)
* Endpoint monitoring with Sysmon
* Windows Event Log analysis
* Log collection and forwarding
* Security monitoring
* Threat detection fundamentals

---

## Related Projects

This home lab demonstrates the SOC monitoring environment and SIEM skills used alongside my investigation projects.

Investigation case studies are documented separately in the SOC Investigation Portfolio repository and may use controlled training environments, public datasets, and Windows Event Log (`.evtx`) analysis.

---

## Summary

This SOC Home Lab demonstrates the deployment of a centralized Windows logging and monitoring environment using Splunk, Sysmon, and the Splunk Universal Forwarder.

The project showcases practical experience with endpoint telemetry collection, SIEM operations, SPL queries, dashboard creation, and security monitoring in a simulated SOC environment.
