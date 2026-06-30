# Day 1 - Environment Setup

## Objective

Build the foundation of a Security Operations Center (SOC) Home Lab by installing and configuring the core infrastructure.



## Environment

| Component | Version |
|-----------|---------|
| Operating System | Windows 11 |
| Splunk Enterprise | 10.4.0 |
| Splunk Universal Forwarder | 10.4.0 |
| Sysmon | Latest Version |



## Completed Tasks

- Installed Splunk Enterprise.
- Installed Splunk Universal Forwarder.
- Installed Microsoft Sysmon.
- Installed Sysmon configuration.
- Enabled Splunk receiving port (9997).
- Configured Universal Forwarder to communicate with Splunk Enterprise.



## Skills Learned

- Installing SIEM software.
- Configuring Splunk services.
- Understanding Universal Forwarder architecture.
- Windows Event Collection fundamentals.



## Challenges

- Universal Forwarder authentication.
- Configuring forwarding to localhost.
- Troubleshooting Windows Event Log ingestion.



## Status

🟡 Environment successfully deployed.

Next step:
Configure Windows Event Log ingestion and verify Sysmon events inside Splunk.
