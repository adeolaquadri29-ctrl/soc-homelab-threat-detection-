🛡️ SOC Home Lab – Threat Detection & Incident Response Architecture

🔹 Overview

This project simulates a real-world Security Operations Center (SOC) environment designed to detect, analyze, and respond to cyber threats.

The lab integrates endpoint monitoring, network intrusion detection, vulnerability assessment, and centralized log analysis using Wazuh SIEM.

🔹 Environment Setup

🛠️ Attacker Machine

* Kali Linux
* Tools:
    * Nmap
    * Hydra
    * Metasploit
    * Nessus

Purpose:
Simulate real-world attacks:

* SSH brute force
* RDP brute force
* Port scanning
* Exploitation

⸻

🖥️ Core Server (Central Node)

* Ubuntu Server
* Hosts:
    * Wazuh Manager (SIEM)
    * Samba AD-DC (Active Directory Domain Controller)

Purpose:

* Centralized log collection and correlation
* Domain authentication and management

⸻

💻 Monitored Endpoints

🪟 Windows Endpoint

* Sysmon installed
* Wazuh Agent installed
* Joined to Samba AD Domain

Function:

* Generates detailed system and security logs
* Forwards logs to Wazuh for analysis

⸻

🐧 Ubuntu Desktop

* Wazuh Agent installed

Hosts:

* Suricata IDS
* Wireshark
* Fail2Ban

Function:

* Network traffic monitoring
* Packet analysis
* Automated attack mitigation

⸻

📊 Monitoring Interface

* Wazuh Dashboard (Tablet Device)

Used for:

* Real-time alert monitoring
* Log analysis
* Threat investigation

⸻

🔹 Data Flow & Detection Pipeline

1. Attack Simulation
    * Kali Linux launches attacks (SSH, RDP, Nmap scans, exploits)
2. Network Monitoring
    * Suricata analyzes traffic
    * Generates alerts for suspicious activity
3. Endpoint Monitoring
    * Sysmon captures Windows events
    * Ubuntu agent collects Linux logs
4. Log Forwarding
    * All logs (Sysmon, Suricata, Ubuntu) are forwarded into Wazuh
5. Central Analysis
    * Wazuh correlates logs and detects threats
    * Alerts are generated based on rules and anomalies
6. Incident Response
    * Fail2Ban blocks malicious IP addresses
7. Visualization
    * Alerts and logs are monitored via Wazuh dashboard

⸻

🔹 Security Capabilities Demonstrated

* SIEM deployment and log centralization
* Network intrusion detection and traffic analysis
* Endpoint monitoring (Windows & Linux)
* Threat detection and alert correlation
* Incident response and automated blocking
* Vulnerability assessment using Nessus

⸻


🔹 Project Evidence

* Screenshots → /screenshots
* logs
* Videos → /videos

⸻

🔹 Skills Demonstrated

* Threat Detection & Analysis
* SIEM Configuration (Wazuh)
* Log Analysis (JSON & Event Logs)
* Incident Response & Mitigation
* Network Security Monitoring
* Vulnerability Assessment

⸻

🔹 Purpose

This project demonstrates the ability to:

* Detect real-world cyber attacks
* Analyze logs and correlate events
* Investigate security alerts
* Respond to incidents effectively

⸻

🔹 Key Takeaway

This SOC lab reflects a practical blue team environment where multiple security tools are integrated to provide end-to-end visibility, detection, and response across both network and endpoint layers.
