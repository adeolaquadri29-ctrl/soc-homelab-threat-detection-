🛡️ SOC Home Lab – Threat Detection & Incident Response

🔹 Overview

This project simulates a real-world Security Operations Center (SOC) environment designed to detect, analyze, and respond to cyber threats.

The lab integrates endpoint monitoring, network intrusion detection, vulnerability assessment, and centralized log analysis using Wazuh SIEM.

⸻

🔹 Lab Architecture

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

⸻

💻 Monitored Endpoints

🪟 Windows Endpoint

* Sysmon installed
* Wazuh Agent installed
* Joined to Samba AD Domain

🐧 Ubuntu Desktop

* Wazuh Agent installed
* Hosts:
    * Suricata IDS
    * Wireshark
    * Fail2Ban

⸻

📊 Monitoring Interface

* Wazuh Dashboard (Tablet Device)

⸻

🔹 Attack Simulation & Detection Workflow

1. Attacker machine (Kali Linux) initiates attack (Hydra, Nmap, Metasploit)
2. Suricata detects suspicious network traffic
3. Sysmon logs endpoint activity
4. Logs are forwarded into Wazuh
5. Wazuh correlates events and generates alerts
6. Fail2Ban blocks attacker IP
7. Alerts are analyzed via Wazuh dashboard

⸻

🔹 Detection Evidence

🔐 SSH Brute Force Detection

🌐 Nmap Scan Detection

🖥️ Sysmon Log Analysis

🔹 Case Studies

🔐 SSH Brute Force Attack

* Attack Tool: Hydra
* Detection: Multiple failed login attempts detected in Wazuh
* Logs: Sysmon + auth logs analyzed
* Response: Fail2Ban blocked attacker IP

⸻

🖥️ RDP Brute Force Attack

* Detection: Wazuh alert triggered from Windows logs
* Analysis: Event logs showed repeated login attempts
* Response: IP blocked and activity contained

⸻

🌐 Nmap Port Scan Detection

* Tool: Nmap
* Detection: Suricata generated scan alerts
* Correlation: Alerts forwarded to Wazuh for analysis

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

* Screenshots
* Videos 

⸻

🔹 Skills Demonstrated

* Threat Detection & Analysis
* SIEM Configuration (Wazuh)
* Log Analysis (JSON & Event Logs)
* Incident Response & Mitigation
* Network Security Monitoring
* Vulnerability Assessment

⸻

🔹 About Me

Transitioned from the Nigeria Police Force into cybersecurity, bringing strong investigative and incident response skills into SOC operations.

Completed the Cisco Networking Academy Junior Cybersecurity Analyst career path with hands-on SOC lab experience.

⸻

🔹 Key Takeaway

This project demonstrates the ability to simulate real-world cyber attacks, detect threats across network and endpoint layers, and respond effectively using integrated security tools in a SOC environment.
