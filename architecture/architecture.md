# SOC Home Lab Architecture

This project simulates a real-world Security Operations Center (SOC) environment for threat detection, analysis, and incident response.

---

## 🔹 Overview

The lab is designed to replicate enterprise security monitoring by integrating endpoint monitoring, network intrusion detection, vulnerability scanning, and centralized log analysis using Wazuh SIEM.

---

## 🔹 Components

### 🛠️ Attacker Machine

- **Kali Linux**

  - Tools: Nmap, Hydra, Metasploit, Nessus

  - Purpose: Simulate real-world attacks such as:

    - SSH brute force

    - RDP brute force

    - Port scanning

    - Exploitation

---

### 🖥️ Core Server (Central Node)

- **Ubuntu Server**

  - Hosts:

    - **Wazuh Manager (SIEM)**

    - **Samba AD-DC (Active Directory Domain Controller)**

  - Purpose:

    - Centralized log collection and analysis

    - Domain authentication and management

---

### 💻 Monitored Endpoints

#### 1. Windows Endpoint

- Sysmon installed
- wazuh agent installed

- Connected to Samba AD Domain

- Sends detailed event logs to Wazuh

#### 2. Ubuntu Desktop

- Wazuh Agent installed

- Hosts:

  - **Suricata IDS** (network monitoring)

  - **Wireshark** (packet analysis)

  - **Fail2Ban** (automated response/blocking)

---

### 📊 Monitoring Interface

- **Wazuh Dashboard (Tablet Device)**

  - Used for:

    - Viewing alerts

    - Log analysis

    - Threat investigation

---

## 🔹 Data Flow

1. **Attack Simulation**

   - Kali Linux launches attacks (SSH, RDP, Nmap scans, exploits)

2. **Network Monitoring**

   - Suricata (on Ubuntu Desktop) analyzes network traffic

   - Generates alerts for suspicious activity

3. **Endpoint Monitoring**

   - Sysmon (Windows) generates detailed system logs

   - Ubuntu agent collects Linux logs

4. **Log Forwarding**

   - All logs (Sysmon, Suricata, Ubuntu) are forwarded into Wazuh Manager

5. **Central Analysis**

   - Wazuh processes and correlates logs

   - Detects threats and triggers alerts

6. **Response Mechanism**

   - Fail2Ban blocks malicious IP addresses based on detected attacks

7. **Visualization**

   - Alerts and logs are viewed on the Wazuh dashboard via tablet

---

## 🔹 Security Capabilities Demonstrated

- SIEM configuration and log centralization  

- Network intrusion detection (Suricata)  

- Endpoint monitoring (Sysmon & Wazuh agents)  

- Threat detection and alerting  

- Incident response (Fail2Ban IP blocking)  

- Vulnerability assessment (Nessus on Kali)  

---

## 🔹 Purpose

The goal of this lab is to simulate real-world cyber attacks and demonstrate the ability to:

- Detect malicious activities  

- Analyze logs and alerts  

- Correlate events across systems  

- Respond to security incidents  

---

## 🔹 Key Takeaway

This architecture reflects a practical blue team environment where multiple security tools are integrated to provide visibility, detection, and response across both network and endpoint layers.
