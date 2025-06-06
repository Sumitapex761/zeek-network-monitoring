# Network Security Monitoring Using Zeek IDS

## Project Overview  
This project demonstrates the setup and usage of Zeek, an open-source network security monitoring tool, to capture and analyze network traffic. Zeek generates detailed logs that help in detecting suspicious network activities and enhancing network security.

## Features  
- Passive network traffic monitoring  
- Detection of network anomalies and attacks  
- Detailed logging (connection, DNS, notices, etc.)  
- Customizable policy scripting support  

## Tools & Technologies  
- Zeek (Bro) IDS  
- Linux (Debian/Ubuntu)  
- Shell scripting  

## Installation & Setup  
1. Install Zeek:  
   ```bash
   sudo apt update
   sudo apt install zeek
Configure Zeek to monitor your network interface (e.g., enX0):
Edit /usr/local/zeek/etc/node.cfg:

type=standalone
host=localhost
interface=enX0




Deploy Zeek:
sudo zeekctl deploy


Usage
Zeek logs are stored in /usr/local/zeek/logs/current/

View connection logs:   cat /usr/local/zeek/logs/current/conn.log

Analyze other logs like dns.log, weird.log, notice.log for detailed network events.

Benefits
Real-time network monitoring without interrupting traffic

Useful for network forensics and security incident response

Open source and widely used in cybersecurity industry

Author
Sumit Singh
