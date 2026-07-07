# 01 - Splunk Enterprise Deployment

## Objective

Deploy Splunk Enterprise as the central SIEM platform for a SOC lab and prepare it to receive logs from monitored endpoints.

This phase documents the initial Splunk setup, access to the web interface, and activation of the receiving port used by Splunk Universal Forwarders.

## Lab Environment

| Machine | Role |
|---|---|
| Ubuntu VM | Splunk Enterprise Server |
| Windows VM | Endpoint / Log Source |
| Kali Linux VM | Attack Machine |

## Lab Architecture

```text
Kali Linux VM
   |
   | Attack Traffic
   v
Windows VM / Linux VM
   |
   | Splunk Universal Forwarder
   | TCP Port 9997
   v
Ubuntu VM
Splunk Enterprise Server
```

## Step 1 - Splunk Enterprise Server Deployment

Splunk Enterprise was deployed on an Ubuntu virtual machine to act as the central SIEM server for the lab.

The server is responsible for receiving, indexing, searching, and analyzing logs collected from monitored endpoints.

## Step 2 - Accessing Splunk Web Interface

After starting Splunk Enterprise, the web interface was accessed from the browser using:

```text
http://<splunk-server-ip>:8000
```

This confirmed that the Splunk Enterprise server was running and reachable from the lab network.

## Step 3 - Enable Receiving on Port 9997

To allow endpoint logs to be forwarded to Splunk, receiving was enabled on TCP port `9997`.

Navigation path used in Splunk:

```text
Settings > Forwarding and receiving > Configure receiving > New Receiving Port
```

Configured port:

```text
9997
```

Port `9997` is used by Splunk Universal Forwarder to send logs from endpoints to the Splunk Enterprise server.

The screenshot below confirms that Splunk Enterprise is listening on port `9997` and that the status is enabled.

![Splunk receiving port 9997 enabled](images/splunk-receiving-port-9997-redacted-v2.png)
