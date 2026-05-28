#  Setup Guide - Multi-Endpoint SIEM Lab

##  Lab Environment
| Machine | OS | Role | Hostname |
|---|---|---|---|
| Kali Linux | Kali | Splunk Server | - |
| Windows 11 | Win 11 | Endpoint 1 | shinejasonenock |
| Windows 10 | Win 10 | Endpoint 2 | DESKTOP-OAIVT6V |

## Step 1: Install Splunk Enterprise on Kali Linux
- Download Splunk from splunk.com
- Install and start Splunk service
- Open browser → go to http://localhost:8000
- Login with admin credentials

## Step 2: Install Universal Forwarder on Windows 11
- Download Splunk Universal Forwarder
- Install on Windows 11 (hostname: shinejasonenock)
- Enter Splunk server IP and port 9997
- Forwarder sends Windows logs to Splunk

## Step 3: Install Universal Forwarder on Windows 10
- Same steps as Windows 11
- Hostname: DESKTOP-OAIVT6V
- Point to same Splunk server IP and port 9997

## Step 4: Configure Receiving Port in Splunk
- Login to Splunk Web
- Settings → Forwarding and Receiving
- Add port 9997 as receiving port

## Step 5: Verify Logs in Splunk
- Go to Search and Reporting
- Search: index=* host=*
- Confirm logs from both Windows machines
