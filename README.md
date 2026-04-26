# SIEM Lab Setup With Wazuh

This project is a home lab SIEM setup using Wazuh for security monitoring and log analysis.

---

## Objective
To build a basic SIEM environment for:
- Log collection and monitoring
- Security event detection
- Simulating attack scenarios (future updates)

---

## Tools Used
- Wazuh (SIEM platform)
- Wazuh Agent (endpoint monitoring)
- Wazuh Server / Manager
- Agent Endpoint
- Virtual Lab Environment

---

## Architecture
See `/architecture` folder for full system diagram.

Flow:
Endpoint (Ubuntu) → Wazuh Agent → Wazuh Server (Debian) → Alerts & Log Analysis

---

## Wazuh Basic Command 
- Check Wazuh Manager status (Debian)
```bash
sudo systemctl status wazuh-manager
```
- Check Wazuh Agent status (Ubuntu)
```bash
sudo systemctl status wazuh-agent
```
- List connected agents (Debian)
```bash
sudo /var/ossec/bin/agent_control -l
```
Expected Output
```bash
Active ubuntu-agent
```
- View real-time alerts (MOST IMPORTANT)
```bash
sudo tail -f /var/ossec/logs/alerts/alerts.log
```
- View Manager Logs
```bash
sudo tail -f /var/ossec/logs/ossec.log
```
- Restart Service
  Manager (Debian)
```bash
sudo systemctl restart wazuh-manager
```
  Agent (Ubuntu)
```bash
sudo systemctl restart wazuh-agent
```

---

## Current Status
🚧 Setup not started yet.

Planned:
- Install Wazuh
- Configure agent & server
- Build SIEM lab environment

Last updated: 25 April 2026

---

## Future Improvements
- Add Elasticsearch / OpenSearch integration
- Improve visualization dashboard
- Add more detection rules

---

## 📸 Screenshots
(To be added)

---

## 📖 Notes
This is a personal cybersecurity learning project for SOC/SIEM practice.
