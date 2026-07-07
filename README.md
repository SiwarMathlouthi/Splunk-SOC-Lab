# Splunk SOC Lab

## Overview

This repository documents the deployment of a Splunk-based SOC lab used for security monitoring, log analysis, incident detection, and threat investigation.

## Lab Environment

| Machine | Role |
|---|---|
| Ubuntu VM | Splunk Enterprise Server |
| Windows VM | Endpoint / Log Source |
| Kali Linux VM | Attack Machine |

## Project Structure

- `01-Splunk-Deployment` — Splunk Enterprise setup and receiving configuration
- `02-Windows-Log-Monitoring` — Windows log collection
- `03-Sysmon-Integration` — Sysmon telemetry collection
- `04-Brute-Force-Detection` — SSH/RDP brute-force detection
- `05-Splunk-Dashboards` — SOC dashboards
- `06-Threat-Hunting` — SPL-based hunting queries
- `07-Incident-Investigation` — Full incident analysis cases

## Skills Demonstrated

- Splunk Enterprise
- SIEM deployment
- Log collection
- Windows/Linux monitoring
- Security event analysis
- Incident detection
- SOC documentation
