# Day 06 – Exploring Sysmon Events with Splunk

## Objective

Practice using SPL (Search Processing Language) to investigate different Sysmon events collected by Splunk.



## 1. Display All Indexed Events

SPL Query
index=main

![](../screenshots/day6/01_all_events.jpg)



## 2. Count Sysmon Event IDs

SPL Query
index=main | stats count by EventCode

![](../screenshots/day6/02_eventcode_count.png)



## 3. Process Creation (Event ID 1)

SPL Query
index=main EventCode=1

![](../screenshots/day6/03_process_creation.png)



## 4. Network Connections (Event ID 3)

SPL Query
index=main EventCode=3

![](../screenshots/day6/04_network_connections.jpg)



## 5. File Creation (Event ID 11)

SPL Query
index=main EventCode=11

![](../screenshots/day6/05_file_create.png)



## 6. DNS Queries (Event ID 22)

SPL Query
index=main EventCode=22


![](../screenshots/day6/06_dns_queries.png)



## What I Learned

- Event ID 1 records process creation.
- Event ID 3 records network connections.
- Event ID 11 records file creation.
- Event ID 22 records DNS queries.
- Using SPL queries makes it easier to investigate endpoint activity in Splunk.
