# Wazuh SIEM Implementation

<img src="../../assets/dp.jpeg" alt="Wazuh Logo" width="150" style="display:block;margin:auto;">

---

## 🛡 Project Overview
This project demonstrates the implementation of a **Security Information and Event Management (SIEM)** system using **Wazuh**.  
The goal was to monitor and secure endpoints, detect threats, and generate actionable alerts.

**Key Features:**
- Integration of **Windows and Linux endpoints** with Wazuh agents.
- **Malware detection** via VirusTotal integration.
- **Automated email alerts** based on risk levels.
- Centralized logging for **security analysis and monitoring**.

---

## 🖥 Architecture

### Topology Diagram
![Wazuh Architecture](./images/wazuh_architecture.png)

**Components:**
- **Wazuh Server** – Deployed on WSL Ubuntu. Handles log collection, analysis, and alerting.  
- **Agents** – Windows 11 host, Kali VM, and Ubuntu server configured to send logs to Wazuh server.  
- **Integration** – VirusTotal API used for malware threat detection.  
- **Notifications** – Email alerts triggered for high-risk events.

---

## 📊 Monitoring & Alerts

### Example Alerts Dashboard
![Alerts Dashboard](./images/wazuh_alerts_dashboard.png)

- Logs are categorized by **risk level** (Low, Medium, High).  
- Email notifications are sent automatically when **high-risk threats** are detected.  
- Centralized dashboards allow **real-time monitoring** of security events.

---

## ⚙️ Implementation Details

1. **Wazuh Server Setup**
   - Installed on **Ubuntu WSL**.
   - Configured Elasticsearch, Kibana, and Wazuh API.
2. **Agent Deployment**
   - Windows 11 host and Kali Linux VM connected as agents.
   - Configured log forwarding and monitoring policies.
3. **VirusTotal Integration**
