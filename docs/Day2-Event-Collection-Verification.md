# Day 2 - Event Collection Verification

## Objective

Verify that Sysmon is generating Windows events and confirm that Splunk Universal Forwarder is configured to collect and forward those events to Splunk Enterprise.




## Completed Tasks

- Verified that the Sysmon service is running.
- Confirmed that Sysmon Operational logs are being generated.
- Verified Universal Forwarder WinEventLog configuration.
- Installed Splunk Add-on for Microsoft Windows.
- Searched for incoming events in Splunk Enterprise.
- Identified that Windows events were not yet being indexed.



## Skills Gained

- Verifying Windows services.
- Inspecting Sysmon Operational Event Logs.
- Validating Splunk Universal Forwarder configuration.
- Installing Splunk Add-ons.
- Troubleshooting Windows Event Log ingestion.



## Challenges

Although Sysmon events were successfully generated and the Universal Forwarder configuration appeared correct, no events were indexed inside Splunk Enterprise. Further troubleshooting is required to determine the cause of the ingestion issue.



## Lessons Learned

I learned how to verify each stage of the Windows event collection pipeline instead of assuming the issue was caused by Sysmon itself. I also gained experience validating services, event logs, and Splunk configurations during troubleshooting.



## Status

🟡 In Progress



## Next Step

Investigate why Splunk Enterprise is not indexing Windows events despite the Universal Forwarder and Sysmon being correctly configured.



## Screenshots

### 1. Sysmon Service Running

![Sysmon Running](../screenshots/day2/01_sysmon_service_running.png)



### 2. Sysmon Operational Events

![Sysmon Events](../screenshots/day2/02_sysmon_events_Verified.png)



### 3. Universal Forwarder WinEventLog Configuration

![Forwarder Configuration](../screenshots/day2/03_forwarder_input_configuration.png)



### 4. Splunk Search (No Results)

![Splunk Search](../screenshots/day2/04_no_events_in_splunk.png)



### 5. Splunk Add-on for Microsoft Windows Installed

![Splunk Add-on](../screenshots/day2/05_windows_addon_installed.png)
