# SOC Detection Queries (Splunk SIEM Lab)

This project contains Splunk queries used for SOC-style monitoring using Windows Event Logs and Sysmon.

```spl
index=main (EventCode=4625 OR EventID=4625)
| stats count by Account_Name, host
| sort -count

index=main (EventCode=4624 OR EventID=4624)
| stats count by Account_Name, host
| sort -count

index=main (EventCode=4625 OR EventID=4625)
| stats count by Account_Name, host

index=main (EventID=1 OR EventCode=1)
| stats count by Image, host
| sort -count

index=main
| stats count by sourcetype