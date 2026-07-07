# 01 - Splunk Enterprise Deployment

## Objective

Deploy Splunk Enterprise as the central SIEM platform for a SOC lab.

The goal of this phase is to prepare Splunk to receive logs from monitored endpoints such as Windows and Linux machines.

## Lab Architecture

```text
Kali Linux VM
   |
   | Attack Traffic
   v
Windows VM / Linux VM
   |
   | Splunk Universal Forwarder
   | Port 9997
   v
Ubuntu VM
Splunk Enterprise Server

