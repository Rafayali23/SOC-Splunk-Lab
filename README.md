# SOC Splunk Lab – Windows Security Monitoring & Threat Detection

## Overview
This project is a Security Operations Center (SOC) simulation built using Splunk Enterprise and Windows Event Logs with Sysmon integration. It demonstrates real-world SIEM use cases such as log ingestion, threat detection, authentication monitoring, and endpoint activity analysis.

The goal of this project is to simulate how a SOC analyst monitors a system, detects suspicious activity, and investigates security events using Splunk.

---

## Tools & Technologies Used

- Splunk Enterprise (SIEM Platform)
- Windows Event Logs
- Sysmon (System Monitoring Tool)
- Windows 10/11 Local Machine

---

## Architecture

Windows System → Sysmon / Event Logs → Splunk Enterprise → Dashboard & Alerts

---

## Key Features

- Authentication monitoring (successful and failed logins)
- Brute force detection using failed login attempts
- Endpoint process monitoring using Sysmon
- Log ingestion and indexing into Splunk
- SOC-style dashboard creation and visualization

---

## Detections Implemented

All detection logic is written using Splunk SPL queries and stored in the `/queries` folder.

### Authentication Monitoring
- Failed login detection (EventCode 4625)
- Successful login tracking (EventCode 4624)
- Brute force pattern analysis

### Endpoint Monitoring (Sysmon)
- Process creation monitoring (EventID 1)
- Suspicious process execution tracking
- Host-based activity analysis

---

## Splunk Queries

All SPL queries used in this project are stored in the `/queries` folder for reference.

Key detections include:
- Failed Login Detection
- Successful Login Tracking
- Brute Force Analysis
- Sysmon Process Monitoring

---

## Dashboards

A SOC-style dashboard was created in Splunk Enterprise containing:

- Failed Login Attempts Panel
- Successful Login Monitoring Panel
- Brute Force Detection Panel
- Endpoint Process Activity Dashboard

---

## Screenshots

All screenshots of dashboards, query results, and analysis are available in the `/screenshots` folder.

They include:
- SOC Dashboard Overview
- Failed Login Detection Visualization
- Brute Force Activity Monitoring
- Sysmon Process Activity View

---

## Skills Demonstrated

- SIEM log analysis and correlation
- Threat detection engineering
- SPL (Search Processing Language)
- SOC dashboard creation
- Windows event log monitoring
- Endpoint detection using Sysmon

---

## Future Improvements

- Add real-time alerting for brute force attacks
- Map detections to MITRE ATT&CK framework
- Enable multi-host log ingestion
- Create automated incident alerts
- Integrate email/webhook notifications

---

## Conclusion

This project demonstrates a functional SOC monitoring environment using Splunk Enterprise. It simulates real-world security operations workflows including log ingestion, threat detection, and dashboard visualization. It is designed to showcase practical SOC analyst skills and SIEM usage.

