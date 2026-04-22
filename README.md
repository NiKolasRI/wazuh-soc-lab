
# 🛡️ Wazuh SOC Lab – Real-World Security Monitoring

## 📌 Description

This project simulates a real-world Security Operations Center (SOC) using Wazuh SIEM.

The lab includes endpoint monitoring, attack simulation, threat detection, and security event analysis, replicating real SOC workflows.

---

## 🧱 Architecture

* 🖥️ Wazuh Server (SIEM)
* 💻 Ubuntu Client (monitored endpoint)
* 🧪 Kali Linux (attacker machine)

---

## 🚨 Simulated Attacks

The following attack scenarios were executed to generate real security events:

*  SSH brute force attack
*  Privilege escalation (sudo access)
*  File Integrity Monitoring (FIM) alerts
*  Suspicious user creation

---

## 🔍 Detection Capabilities

Wazuh was configured to detect:

* Multiple failed SSH login attempts
* Unauthorized privilege escalation
* Changes in critical system files
* Suspicious system activity

---

## 🧠 MITRE ATT&CK Mapping

* **T1110 – Brute Force**
* **T1078 – Valid Accounts**
* **T1068 – Privilege Escalation**

---

## 🧪 Example Attack

### SSH Brute Force

```bash
hydra -l root -P rockyou.txt ssh://<IP_VICTIMA>
```

📌 This attack generates multiple failed login attempts detected by Wazuh.

---

## 📸 Evidence

Screenshots of alerts and dashboard:

<img width="814" height="369" alt="Captura de pantalla 2026-04-22 142752" src="https://github.com/user-attachments/assets/3b645022-e843-47f5-8aef-a59e268c6061" />


---

## 🧾 Incident Report

An incident report was created for the SSH brute force attack:

* Detection of repeated failed login attempts
* Identification of attacker IP
* Analysis of logs and alerts
* Response actions applied

(See `/reports/incident-ssh-bruteforce.md`)

---

## ⚙️ Setup Summary

### Install Wazuh Agent

```bash
curl -sO https://packages.wazuh.com/4.x/wazuh-agent.sh
sudo bash wazuh-agent.sh -a <IP_WAZUH>
```

### Start Agent

```bash
sudo systemctl start wazuh-agent
sudo systemctl enable wazuh-agent
```

---

## 🎯 Skills Demonstrated

* SIEM configuration (Wazuh)
* Threat detection and analysis
* Log monitoring and investigation
* Incident response basics
* Security event correlation

---

## 🧠 What I Learned

* How to deploy and configure Wazuh agents
* How to simulate real cyberattacks
* How to detect and analyze security events
* How a SOC environment operates

---

## 🚀 Future Improvements

* Integration with Suricata (IDS)
* Advanced threat detection rules
* Automated incident response
* Monitoring of web server logs

---

## 👨‍💻 Author

Cybersecurity student focused on Blue Team and SOC operations.
