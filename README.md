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


## 🛡️ Task 2: Phishing Email Analysis – Zoho Interview Scam

---

### 1. 🧾 Introduction

This task involved analyzing a phishing email masquerading as a job interview invitation from Zoho. The email contained multiple indicators of phishing, including spoofed branding, suspicious links, and deceptive formatting techniques. The goal was to dissect the components of the email to uncover malicious intent and understand how such attacks attempt to manipulate recipients into revealing sensitive information.

---

### 2. 🛠️ Tools Used

- **MXToolbox Email Header Analyzer**  
  🔗 [https://mxtoolbox.com/EmailHeaders.aspx](https://mxtoolbox.com/EmailHeaders.aspx)  
  Used to analyze SPF, DKIM, and DMARC validation and email authenticity.

- **Browser Analysis**  
  For previewing embedded phishing links and visual formatting.

- **Image Evidence Screenshots**  
  Captured and analyzed visual components of the phishing email.

---

### 3. 📋 Steps Followed

#### a. Sender Email Address Analysis
- Sender: `zohointerview@onmailcloud.onmicrosoft.com`
- **Phishing Indicator**: Though it appears official, the domain `onmailcloud.onmicrosoft.com` is suspicious and unrelated to Zoho's actual email infrastructure.

---

#### b. Email Header Inspection
- Tool: **MXToolbox**
- Findings:
  - **No DMARC record** found
  - Likely misconfigured or missing SPF/DKIM validation
  - Mail server identity inconsistent with Zoho's infrastructure

---

#### c. Suspicious Link Inspection
- URL Embedded:  
  `https://click.pstmrk.it/3s/sweedbuy.com%2Fblog%2F/...`
- Target domain `sweedbuy.com` is unrelated to Zoho or job interviews.
- **Phishing Indicator**: Deceptive redirection to an external, suspicious site.

---

#### d. Urgent or Manipulative Language
- Email included emotionally triggering phrases:
  - “Your interview is scheduled...”
  - “Click the link to join now”
- **Phishing Indicator**: Urgency and impersonation of a job offer to exploit victims emotionally.

---

#### e. Grammar and Text Manipulation
- Examples of obfuscation using Unicode/spacing:
  - “el‌‌‌‌‌‌i‌‌‌‌‌‌gib‌‌‌‌‌‌i lity”
  - “a‌‌p‌‌p Ιy” (Greek iota used instead of Latin 'I')
- **Phishing Indicator**: Use of special characters to bypass spam filters and confuse readers.

---
#### f. Spoofed Branding
- Imitated Company: **Zoho**
- Fake interview offer styled with **official-looking fonts and structure**
- **Phishing Indicator**: Branding elements copied without authorization to falsely gain trust.


---

#### g. Absence of Legitimate Footer Details
- No unsubscribe option or official Zoho contact info.
- No privacy policy or company links.
- **Phishing Indicator**: Fails professional communication norms.

---

### 4. 🚩 Summary of Phishing Indicators

| Category                      | Phishing Indicator Description                                       |
|------------------------------|-----------------------------------------------------------------------|
| Sender Address               | Generic domain unrelated to Zoho (onmailcloud.onmicrosoft.com)       |
| Email Header                 | No DMARC, SPF/DKIM mismatch                                           |
| Embedded Link                | Redirects to `sweedbuy.com`, not affiliated with Zoho                |
| Language                     | Urgency and impersonation techniques                                 |
| Text Formatting              | Hidden characters, obfuscation with Unicode                          |
| Branding                     | Zoho branding misused for trust manipulation                         |
| Footer                       | No privacy links, unsubscribe options, or official contact details    |

---

### 5. 📚 Key Learnings

- Phishing campaigns often use **job opportunities** as bait, targeting vulnerable users.
- Attackers manipulate **email headers and Unicode** characters to deceive spam filters.
- Use of tools like **MXToolbox** helped identify missing authentication protocols.
- Learned to analyze and report email threats with **clear, evidence-based indicators**.

---

### 6. ✅ Conclusion

This task enhanced my understanding of **email-based phishing techniques** by examining a malicious message posing as a Zoho interview invitation. By carefully analyzing the sender’s address, email headers, URLs, and content formatting, I successfully identified multiple red flags. This exercise reinforced my capability to critically assess suspicious emails and equipped me with practical skills in threat detection and reporting.

---

# Task 3 Windows Firewall Configuration and Testing Report

**Project Title:** Windows Firewall Rule Creation and Validation  
**Author:** Kshitij  
**Operating System:** Windows  
**Target IP Address:** 192.168.135.40  
**Date of Configuration and Testing:** May 27, 2025  

---

## 1. Introduction

Windows Firewall acts as a vital security layer for protecting systems from unauthorized access. It monitors and controls incoming and outgoing network traffic based on predefined rules. In this task, a custom firewall rule was created to block a specific port (Telnet – Port 23), and its effectiveness was verified.

---

## 2. Objective

To create a Windows Firewall rule via the GUI that blocks traffic on port 23 (Telnet), test it using a network scanning method, and revert the configuration to its original state.

---

## 3. Procedure

### 3.1 Listing Existing Rules

**Method:** Using the Windows Firewall GUI interface.  

---

### 3.2 Creating a Rule to Block Port 23

**Steps:**  
1. Access “Windows Defender Firewall with Advanced Security”  
2. Create a new **Inbound Rule**  
3. Choose **Port**, specify **TCP**, and enter port number **23**  
4. Select **Block the connection**  
5. Apply rule to all profiles (Domain, Private, Public)  
6. Name the rule appropriately  

---

### 3.3 Validating the Rule

**Method:** Attempted to scan or access the Telnet service from another host. The connection was successfully blocked by the firewall.  

---

### 3.4 Reverting the Configuration

The created rule was deleted to restore the firewall to its original configuration.  

---

## 4. Firewall Filtering Mechanism – Summary

Windows Firewall filters traffic based on multiple parameters:

- **IP Address**: Filters by source/destination IP (e.g., block a suspicious IP)
- **Port Number**: Allows/denies specific ports (e.g., block Telnet port 23)
- **Protocol**: Filters traffic by protocol like TCP, UDP, ICMP
- **Traffic Direction**: Handles both inbound and outbound rules
- **Application Filtering**: Allows rules specific to software (e.g., Chrome)
- **Deep Packet Inspection**: Advanced firewalls inspect packet content

### Rule Types:
- **Allow**: Permits the traffic
- **Deny**: Blocks the traffic
- **Default Policy**: Blocks traffic unless a rule allows it

### Decision Flow:
Traffic → Checked Against Rules →  
- Match Allow → Permitted  
- Match Deny → Blocked  
- No Match → Default Policy (usually deny)

---

## 5. Conclusion

This task demonstrated the process of configuring a firewall rule to block a specific port, verifying its effect, and restoring default settings. Understanding and managing such rules is crucial in ensuring network security on Windows environments.

---

## Appendix

- **Tool Used:** Windows Defender Firewall  
- **Configuration Method:** GUI  
- **Testing Method:** Port access attempt and confirmation of block  
- **System Type:** Windows OS (Virtual or Native)  
- **Scan Date:** May 27, 2025  


# 📄 Task 4 – Elevate Labs Cybersecurity Internship  
# Windows Firewall Configuration & Testing Documentation  

**Target IP:** 192.168.135.40  
**Operating System:** Windows  
**Date of Scan:** May 27, 2025  

---

## 📄 Viewing Existing Firewall Rules  

---

## 📄 Creating a Rule to Block a Port  

### ➤ Approach: GUI-Based Configuration  

---

## 📄 Validating the Firewall Rule  

---

## 📄 Restoring Initial Configuration  

---

# 🔒 Understanding Firewall Traffic Filtering – Summary  

Firewalls serve as a **protective gateway** between secure internal systems and potentially dangerous external networks (like the internet). They analyze traffic and enforce **access control rules** to either allow or deny data packets.

---

## 🔍 Primary Filtering Parameters  

### 1. **IP Address-Based Filtering**  
- Screens traffic using **source** or **destination** IP information.  
- _Example_: Prevent connections from blacklisted IP addresses.

### 2. **Port-Based Filtering**  
- Determines access by evaluating **TCP/UDP ports**.  
- _Example_: Deny access to port 23 (Telnet); allow port 80 (HTTP).

### 3. **Protocol Type**  
- Filters data depending on the **communication protocol** in use (e.g., TCP, UDP, ICMP).  
- _Example_: Block incoming ping (ICMP) requests for security.

### 4. **Traffic Direction**  
- **Inbound:** Data entering the system.  
- **Outbound:** Data exiting the system.

### 5. **Application-Level Filtering**  
- Some firewalls can make decisions based on the **specific application** sending or receiving data.  
- _Example_: Permit Google Chrome; restrict unknown executables.

### 6. **Deep Packet Inspection (DPI)**  
- Inspects the **contents** of network packets to detect and prevent threats like malware or sensitive data exfiltration.

---

## 📋 Rule Categories in Firewall Configuration  

- **Allow Rules** – Let matching traffic through.  
- **Block Rules** – Deny traffic that meets specific conditions.  
- **Default Rule** – Applies to all unmatched traffic (often “deny all”).

---

## 🔁 Firewall Decision Process (Overview)  

Data Flow → Apply Firewall Rules → Action:  
→ If it fits an **Allow** rule → Traffic is permitted  
→ If it fits a **Deny** rule → Traffic is rejected  
→ If no rule matches → Apply the **default rule**, typically block by default

---
# Task 6 Network Traffic Analysis with Wireshark

This repository contains the capture file and analysis report for a network traffic analysis task conducted using **Wireshark**.

---

## 📁 Capture Details

- **File Name:** `wireshark_Wi-FiLBT072.pcapng`
- **Captured On:** June 4, 2025
- **Duration:** 3 minutes 14 seconds
- **Captured Packets:** 2536
- **Displayed Packets:** 580 (22.9%)
- **Interface:** Wi-Fi
- **Tool Version:** Wireshark v4.4.6
- **OS:** Windows 11 (64-bit)
- **Processor:** Intel i5-1235U (12th Gen)

---

## 📊 Protocols Identified

- **TCP** (Transmission Control Protocol)
- **TLSv1.2** (Encrypted Web Communication)
- **DNS** (Domain Name Resolution)

---

## ⚠ Expert Info Summary

| Type        | Description                               | Count |
|-------------|-------------------------------------------|-------|
| ⚠ Warning   | D-SACK Sequences                          | 2     |
| ⚠ Warning   | Out-of-Order Segments                     | 2     |
| ⚠ Warning   | Previous Segments Not Captured            | 2     |
| ℹ Note      | Suspected Retransmissions                 | 2     |
| ℹ Note      | Duplicate ACKs                            | 7     |

---

## 🔍 Notable Observations

- Multiple **TCP retransmissions** and **Duplicate ACKs** detected.
- Use of **TLSv1.2** confirms encrypted HTTPS communication.
- Occurrence of **TCP RST** and **FIN** flags indicating session terminations.

---

## 📷 Screenshots

- ✅ Capture Statistics Summary
- ✅ TCP Expert Information
- ✅ Highlighted Packet Anomalies

*(See `/screenshots/` folder)*

---

## 📝 Report

A detailed analysis report (`Network_Analysis_Report.md`) is included in this repository. It covers:
- Objective & Environment
- Methodology
- Detailed Protocol Analysis
- Observations & Interpretation

---



