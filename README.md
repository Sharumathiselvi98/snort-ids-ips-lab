# Snort IDS/IPS Lab

## Overview
Hands-on implementation of Snort as an 
Intrusion Detection and Prevention System 
on Linux. Includes full tutorial with 
screenshots and working rule examples.

## What I Built
- Installed and configured Snort on Ubuntu
- Set HOME_NET to device IP in snort.conf
- Tested configuration in safe test mode
- Wrote custom detection rules covering:
  - ICMP traffic alerts
  - IP filtering (single, range, exclusion)
  - Port filtering (single, range, exclusion)
  - FTP Port 21 detection
- Tested rules across two networked VMs
- Captured real-time alerts in console

## Key Rules Written

# ICMP alert
alert icmp any any <> any any 
(msg: "ICMP alert"; sid:1000001; rev:1)

# FTP port detection  
alert tcp any any <> any 21 
(msg: "FTP Port 21 Detected"; sid:100001; rev:1)

# Exclude specific subnet
alert icmp !10.0.2.4/24 any <> any any 
(msg: "ICMP Outside Subnet"; sid:100001; rev:1)

## Project Files
- snort.html — Full tutorial with screenshots
- /screenshots — All lab evidence

## Skills Demonstrated
- IDS/IPS configuration and rule writing
- Network traffic analysis
- Linux system administration
- Virtual machine internal networking
- Real-time alert monitoring

## Tools Used
- Snort 3
- Ubuntu Linux
- VirtualBox (two VM internal network)
