# Day 2 - Event Collection Verification

## Objective

Verify that Sysmon is generating Windows events and ensure Splunk Universal Forwarder is configured to collect them.



## Environment

| Component | Version |
|-----------|---------|
| Windows 11 | 24H2 |
| Splunk Enterprise | 10.4.0 |
| Splunk Universal Forwarder | 10.4.0 |
| Sysmon | Latest |



## Completed Tasks

- Verified Sysmon service is running.
- Confirmed Sysmon Operational log contains Process Creation events.
- Verified Universal Forwarder monitors Microsoft-Windows-Sysmon/Operational.
- Installed Splunk Add-on for Microsoft Windows.
- Tested event search in Splunk.



## Results

✅ Sysmon is generating events.

✅ Universal Forwarder configuration is correct.

❌ Events are not yet appearing inside Splunk Enterprise.

Further troubleshooting is required.



## Skills Learned

- Verifying Windows services.
- Inspecting Windows Event Logs.
- Using wevtutil.
- Using Splunk btool for configuration validation.
- Understanding the Windows data collection pipeline.



## Challenges

- Splunk search returns no events.
- Need to investigate event forwarding between Universal Forwarder and Splunk Enterprise.



## Status

🟡 Data source verified.

Next step:
Troubleshoot why Splunk Enterprise is not indexing forwarded Sysmon events.
