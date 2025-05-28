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
