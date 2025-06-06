# Network Security Monitoring Using Zeek IDS
HERE IS THE SETUP

### 1️⃣ Update & Install Dependencies

sudo apt update && sudo apt upgrade -y
sudo apt install cmake make gcc g++ flex bison libpcap-dev libssl-dev python3-dev swig zlib1g-dev curl -y

2️⃣ Download & Install Zeek
cd ~
curl -L -O https://download.zeek.org/zeek-6.0.1.tar.gz
tar -xvzf zeek-6.0.1.tar.gz
cd zeek-6.0.1
./configure
make -j$(nproc)
sudo make install

3️⃣ Add Zeek to PATH
echo 'export PATH=/usr/local/zeek/bin:$PATH' >> ~/.bashrc
source ~/.bashrc

4️⃣ Configure Interface

sudo nano /usr/local/zeek/etc/node.cfg
Example:- 
[zeek]
type=standalone
host=localhost
interface=enX0  # Replace with your actual interface

5️⃣ Deploy Zeek
sudo zeekctl deploy
6️⃣ Check Status
sudo zeekctl status

7️⃣ View Logs
cd /usr/local/zeek/logs/current
ls
cat conn.log | head

📊 Features
Lightweight IDS using Zeek

Logs: DNS, DHCP, Connections, Notices, Telemetry

Realtime monitoring on AWS EC2

🧠 Interview Lines
"I built a lightweight intrusion detection system using Zeek IDS on an AWS EC2 instance. It logs and monitors real-time network traffic like DNS, DHCP, and suspicious connections, helping in proactive threat detection."

📌 Tools Used
🖥️ Zeek 6.0.1

☁️ AWS EC2 (Debian)

🔒 Linux Networking (tcp/udp/icmp monitoring)

📄 Log analysis via CLI



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
