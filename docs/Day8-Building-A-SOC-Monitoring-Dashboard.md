# Day 08 – Building a SOC Monitoring Dashboard 

## Objective

The objective of this lab was to build a simple SOC monitoring dashboard in Splunk using Sysmon logs collected from the SOC Home Lab. The dashboard provides a centralized view of key security events and helps visualize system activity in a clear and organized way.



## Dashboard Creation Process

The dashboard was created using the following steps:

1. Executed SPL queries in Splunk Search.
2. Created a new dashboard named SOC Monitoring Dashboard.
3. Added dashboard panels using the search results.
4. Selected the appropriate visualization for each panel.
5. Configured all dashboard panels to display data from the last 24 hours.
6. Saved the completed dashboard.

## Dashboard
![Dashboard](../screenshots/00_dashboard.png)
## Final Dashboard

![SOC Monitoring Dashboard](../screenshots/01_dashboard_overview.png)



## Dashboard Panels

### 1. Total Process Creation Events

Displays the total number of Process Creation (Event ID 1) events collected during the selected time range.

SPL Query
index=main EventCode=1 | stats count

Visualization: Single Value

![Total Process Creation Events](../screenshots/02_total_process_creation_panel.png)



### 2. Total Network Connections

Displays the total number of Network Connection (Event ID 3) events.

SPL Query
index=main EventCode=3 | stats count

Visualization: Single Value

![Total Network Connections](../screenshots/03_total_network_connections_panel.png)



### 3. Total DNS Queries

Displays the total number of DNS Query (Event ID 22) events.

SPL Query
index=main EventCode=22 | stats count

Visualization: Single Value

![Total DNS Queries](../screenshots/04_total_dns_queries_panel.png)



### 4. Top 10 Processes

Displays the most frequently executed processes.

SPL Query
index=main EventCode=1 | top limit=10 Image

Visualization: Bar Chart

![Top 10 Processes](../screenshots/05_top_10_processes_panel.png)



### 5. Top Users

Displays the users with the highest number of process creation events.

SPL Query
index=main EventCode=1 | stats count by User | sort -count

Visualization: Bar Chart

![Top Users](../screenshots/06_top_users_panel.png)



### 6. Latest Process Activity

Displays the latest process execution events including execution time, user, process image, and command line.

SPL Query
index=main EventCode=1 | sort -_time | table _time User Image CommandLine | head 20

Visualization: Table

![Latest Process Activity](../screenshots/07_latest_process_activity_panel.png)



## Key Learning Outcomes

- Created a dashboard in Splunk Enterprise.
- Added multiple dashboard panels.
- Used Single Value, Bar Chart, and Table visualizations.
- Displayed Sysmon events in a centralized dashboard.
- Practiced writing SPL queries for monitoring security events.
