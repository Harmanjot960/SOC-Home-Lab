# SOC Home Lab

A personal Security Operations Center (SOC) home lab built to simulate a centralized Windows monitoring environment using Splunk, Sysmon, Windows Event Logs, and Kali Linux for attack simulation.

The lab provides hands-on experience with endpoint telemetry collection, SIEM operations, security event investigation, threat detection, log analysis, detection development, and SOC monitoring workflows.

---

## Objective

The objective of this project was to build a hands-on SOC monitoring environment capable of collecting endpoint telemetry, centralizing Windows security logs, simulating attacker activity, and performing security investigations using Splunk.

The lab was designed to develop practical skills in:

- SIEM monitoring
- Endpoint visibility
- Windows log analysis
- Attack simulation
- Detection query development
- Security event investigation

---

## Skills & Technologies

![SIEM](https://img.shields.io/badge/SIEM-Splunk-blue)
![Endpoint](https://img.shields.io/badge/Endpoint-Sysmon-orange)
![Windows](https://img.shields.io/badge/OS-Windows-blue)
![Detection](https://img.shields.io/badge/Detection-SPL-green)
![Monitoring](https://img.shields.io/badge/Monitoring-Security%20Logs-purple)
![Attack Simulation](https://img.shields.io/badge/Attack%20Simulation-Kali%20Linux-red)
![IDS](https://img.shields.io/badge/IDS-Suricata-red)

---

## Lab Architecture

```text
Diagram 1 — Endpoint Monitoring & Attack Simulation Workflow

                Kali Linux VM
            (Attack Simulation)
                      │
                      ▼
              Windows Endpoint
              (Monitored Host)
                      │
        ┌─────────────┴─────────────┐
        │                           │
        ▼                           ▼
 Windows Security Logs          Sysmon Telemetry
        │                           │
        └─────────────┬─────────────┘
                      │
                      ▼
          Splunk Universal Forwarder
                      │
                      ▼
              Splunk Enterprise
          (SIEM Detection & Analysis)


─────────────────────────────────────
Diagram 2 — Network Threat Hunting Workflow

             Public PCAP Dataset
                      │
                      ▼
          Wireshark + Suricata IDS
                      │
                      ▼
          Network Traffic Analysis
```

---

## Components

| Component | Purpose |
|-----------|---------|
| Kali Linux Virtual Machine | Attack simulation and detection validation activities |
| Windows Virtual Machine | Endpoint monitoring and investigation environment |
| Sysmon | Detailed endpoint telemetry collection |
| Windows Event Logs | Security and system event collection |
| Splunk Universal Forwarder | Collects and forwards endpoint telemetry |
| Splunk Enterprise | SIEM search, analysis, correlation, and detection development |
| Suricata IDS | Network-based threat detection and alert analysis |

---

## Telemetry Collected

The lab collects Windows security telemetry commonly used for SOC investigations, including:

- Process execution events (Sysmon Event ID 1)
- Network connections (Sysmon Event ID 3)
- File activity (Sysmon Event ID 11)
- Registry activity (Sysmon Event ID 13)
- DNS queries (Sysmon Event ID 22)
- Authentication events (Event ID 4624, 4625, 4672)
- PowerShell Script Block Logging (Event ID 4104)
- SMB access events (Event ID 5140, 5145)

---

## Detection & Investigation Capabilities

The SOC Home Lab supports:

- **Endpoint Monitoring:** Process execution analysis, PowerShell investigation, Sysmon telemetry correlation, and suspicious activity analysis
- **Security Monitoring:** Authentication analysis, RDP brute-force detection, Windows Event Log investigation, and SPL query development
- **Network Analysis:** Traffic analysis, IDS alert investigation using Suricata, IOC validation, and security event correlation
- **Detection Validation:** Controlled attack simulation, simulated security events, and detection query testing

---

## Skills Demonstrated

- **SIEM & Log Analysis:** Splunk monitoring, SPL queries, Windows Event Logs, and security event investigation
- **Endpoint Security:** Sysmon telemetry analysis, process investigation, PowerShell analysis, and threat detection
- **Network Security Monitoring:** PCAP analysis, Suricata IDS alerts, network traffic investigation, and IOC analysis
- **SOC Operations:** Alert triage, attack simulation, detection development, and incident investigation workflows

---

## Related Investigations

The SOC Home Lab environment was used for the following portfolio investigations:

- RDP Brute Force Detection
- PowerShell Post-Compromise Investigation
- Network Threat Hunting Investigation

Additional SOC investigations in the portfolio were completed using security labs and publicly available datasets.

---

## Summary

This SOC Home Lab demonstrates practical experience building and operating a Windows-based monitoring environment, collecting security telemetry, simulating attacker activity, analyzing IDS alerts, investigating suspicious behavior, developing detection queries, and performing SOC analyst workflows using industry-standard security tools.
