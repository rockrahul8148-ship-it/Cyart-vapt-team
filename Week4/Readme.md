# VAPT Week 4 – Capstone Project

## Name:
Rahul Rajput

## Course:
Cyber Security Internship – CYART

## Tools Used:
- Kali Linux
- Metasploit
- Burp Suite
- MobSF
- LinPEAS

---

## 🔎 1. Reconnaissance
- Performed Nmap scan on Metasploitable2.
- Identified open FTP service running VSFTPD 2.3.4.

---

## 💥 2. Exploitation
- Used Metasploit module:
  exploit/unix/ftp/vsftpd_234_backdoor
- Successfully gained shell access.

---

## 🔐 3. Privilege Escalation
- Executed LinPEAS for local enumeration.
- Identified outdated Linux kernel version.
- Potential privilege escalation vectors found.

---

## 🌐 4. Web Application Testing (DVWA)
- Tested SQL Injection vulnerability.
- Payload used: 1' OR 1=1#
- Retrieved multiple user records.

---

## 📱 5. Mobile Application Testing (InsecureBankv2)
- Static analysis performed using MobSF.
- Security score indicated high risk.
- Identified dangerous permissions:
  - READ_CONTACTS
  - SEND_SMS
  - READ_PROFILE
- Hardcoded secrets detected in source code.

---

## 📊 Findings Summary
| Vulnerability        | Severity | Status     |
|---------------------|----------|------------|
| VSFTPD RCE          | Critical | Exploited  |
| SQL Injection       | High     | Exploited  |
| Dangerous Permissions | High   | Identified |
| Hardcoded Secrets   | High     | Identified |

---

## ✅ Remediation
- Update outdated services.
- Implement input validation.
- Remove hardcoded credentials.
- Apply least privilege principle.
- Perform regular security audits.
