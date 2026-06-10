# Wazuh SIEM Lab — Integrated Threat Intelligence & Incident Response

A hands-on cybersecurity project demonstrating the deployment and configuration of a comprehensive **Wazuh SIEM environment** on Kali Linux using Docker, integrated with multiple threat intelligence platforms for real-time threat detection and automated incident response.

---

## Project Overview

This project focuses on building a centralized security monitoring environment capable of real-time threat detection, analysis, and automated response by integrating Wazuh with external threat intelligence tools.

A single-node Wazuh stack was deployed using Docker Engine on Kali Linux and tested against simulated real-world attack scenarios including malware detection, suspicious IP analysis, privilege escalation, and brute force attempts.

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Wazuh SIEM | Central security monitoring and XDR platform |
| VirusTotal API | Automated file hash analysis for malware detection |
| AlienVault OTX | Threat intelligence for malicious IP identification |
| MITRE ATT&CK | Mapping alerts to attacker tactics and techniques |
| Docker Engine | Container-based deployment on Kali Linux |
| Auditd | Linux system-level audit logging |

---

## Features Implemented

- **File Integrity Monitoring (FIM)** — Real-time detection of unauthorized file modifications, deletions, and creations using MD5/SHA1/SHA256 checksums
- **VirusTotal Integration** — Automated malware detection by querying file hashes against 70+ antivirus engines
- **AlienVault OTX Integration** — Cross-referencing network logs against millions of Indicators of Compromise (IOCs)
- **MITRE ATT&CK Mapping** — Classifying detected threats by technique ID (e.g. T1110 Brute Force, T1548.003 Privilege Escalation, T1136.001 Persistence)
- **Active Response** — Automated firewall blocking of malicious sources upon threat detection, reducing Mean Time to Respond (MTTR)

---

## Attack Simulations & Results

| Simulation | MITRE Technique | Result |
|-----------|----------------|--------|
| EICAR malware file | — | Detected by VirusTotal (62 engines flagged) |
| Suspicious IP lookup | — | Flagged by AlienVault OTX |
| Access /etc/shadow | T1548.003 Privilege Escalation | Alert generated |
| Create backdoor user | T1136.001 Persistence | Alert generated |
| Failed login attempts | T1110 Brute Force | Alert + firewall block triggered |

---

## System Requirements

- OS: Kali Linux (AMD64)
- CPU: 4+ cores
- RAM: 8+ GB
- Storage: 50+ GB

---

## Author

**Anas K P**  
Cybersecurity Professional | CEH Certified  
[LinkedIn](https://www.linkedin.com/in/anas--kp)x
