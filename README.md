# Elevate-Labs-Cybersecurity-Tasks
# 🛡️ Cybersecurity Internship – Task 1: Local Network Port Scanning

This repository contains my work for **Task 1** of the Cybersecurity Internship program. The task focused on performing a local network scan to discover open ports and analyze network exposure and associated risks using tools like **Nmap** and **Wireshark** in a **VMware + Kali Linux** environment.

---

## 📄 Objective
Learn and apply basic network reconnaissance techniques by:
- Scanning the local network for active hosts and open ports
- Identifying common services and analyzing their potential risks
- Observing packet behavior with Wireshark (optional)
- Saving and documenting results

---

## 🧰 Tools Used
- 🐧 Kali Linux (VM)
- 🌐 Nmap
- 🔬 Wireshark (optional)
- 💻 VMware Workstation

---

## 🛰️ Scan Methodology

- **Network Range Scanned**: `192.168.190.0/24`  
- **Scan Type**: TCP SYN scan (`nmap -sS`)  
- **Output Formats**: Text, XML, and HTML  
- **Command Used**:
  ```bash
  nmap -sS -sV 192.168.190.0/24 -oA scan_results
