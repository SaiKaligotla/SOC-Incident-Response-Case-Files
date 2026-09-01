<div align="center">

# 🛡️ SOC Incident Response Case Files

### Hands-on Security Operations Center investigations — triage, threat hunting, containment, and post-incident reporting

![Platform](https://img.shields.io/badge/Platform-LetsDefend-0a66c2?style=for-the-badge)
![Total Cases](https://img.shields.io/badge/Total%20Cases-5-success?style=for-the-badge)
![True Positives](https://img.shields.io/badge/True%20Positives-4-red?style=for-the-badge)
![False Positives](https://img.shields.io/badge/False%20Positives-1-blue?style=for-the-badge)

</div>

---

## 👨‍💻 About the Analyst

**Sai Kaligotla** — Aspiring Security Operations Center (SOC) Analyst & Incident Responder.

This repository is a practical portfolio documenting investigations of live-simulated cyber attacks in the **LetsDefend** enterprise environment. Each case is written up as an **Official Incident Report** following a strict, repeatable methodology to establish timelines, identify attack vectors, and justify containment decisions based on hard telemetry — including honest documentation of false positives and investigative missteps, because real analyst judgment is built on both.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0a66c2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/saikaligotla/)
[![Email](https://img.shields.io/badge/Email-Contact%20Me-ea4335?style=flat-square&logo=gmail&logoColor=white)](mailto:sarathsai94@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat-square&logo=github)](https://github.com/SaiKaligotla)

</div>

---

## 📊 Case Dashboard

| Metric | Count |
|:--|--:|
| **Total Investigations** | 5 |
| 🔴 True Positives — Malicious Activity Confirmed | 4 |
| 🔵 False Positives — Benign Activity Triaged | 1 |
| 🎣 Phishing & Email Threats | 1 |
| 💻 Endpoint & Malware Compromise | 2 |
| 🌐 Network & Perimeter Anomalies | 2 |

**Status legend:**
🔴 **True Positive** — malicious activity confirmed (threat contained or blocked)
🔵 **False Positive** — benign activity ruled out after investigation

---

## 🗂️ Case Files

> 📁 **Naming convention:** `EventID_<ID> - <Rule Name>.<ext>` · **Folder structure:** phishing → `Phishing_Investigations/` · endpoint/malware → `Endpoint_Compromise/` · network/access → `Network_Anomalies/`

### 🎣 Phishing & Email Threats

| Event ID | Rule Name | Threat Type | Status | Case File |
|:--|:--|:--|:--|:--|
| 257 | SOC282 - Phishing Alert - Deceptive Mail Detected | AsyncRAT / Phishing | 🔴 True Positive | `EventID_257 - SOC282 - Phishing Alert - Deceptive Mail Detected.pdf` |

### 💻 Endpoint & Malware Compromise

| Event ID | Rule Name | Threat Type | Status | Case File |
|:--|:--|:--|:--|:--|
| 313 | SOC335 - CVE-2024-49138 Exploitation Detected | RDP Brute Force → CLFS Privilege Escalation | 🔴 True Positive (Contained) | `EventID_313 - SOC335 - CVE-2024-49138 Exploitation Detected.md` |
| 44 | SOC113 - Suspicious hh.exe Usage | LOLBin (hh.exe) / Benign WinRAR Help File | 🔵 False Positive | `EventID_44 - SOC113 - Suspicious hh.exe Usage.md` |

### 🌐 Network & Perimeter Anomalies

| Event ID | Rule Name | Threat Type | Status | Case File |
|:--|:--|:--|:--|:--|
| 225 | SOC257 - VPN Connection Detected from Unauthorized Country | Credential Abuse / Unauthorized VPN Access | 🔴 True Positive (Blocked by MFA) | `EventID_225 - SOC257 - VPN Connection Detected from Unauthorized Country.pdf` |
| 303 | SOC325 - Unauthorized Cloud Region Access Attempt Detected | Brute-Force / Web Attack | 🔴 True Positive (Blocked) | `EventID_303 - SOC325 - Unauthorized Cloud Region Access Attempt Detected.pdf` |

---

## 🔍 Investigation Methodology

Every case follows the same telemetry-driven workflow, documented as an Official Incident Report:

1. **Alert** — Review rule name, severity, MITRE mapping, affected host/user, and timestamp; determine initial urgency.
2. **Detection** — Pivot across Proxy, Firewall, Endpoint (EDR), Email, VPN/Authentication, and Windows Security logs; reconstruct process lineage (parent → child), authentication timelines, and network connections.
3. **Analysis** — Verify file hashes, IPs, domains, URLs, and accounts via OSINT (VirusTotal, ANY.RUN, URLScan, URLhaus, AbuseIPDB); reconstruct the full kill chain; build an attack narrative and then challenge it against benign explanations (travel, legitimate software, red team).
4. **Containment** — Act at the layer of the compromise: isolate hosts via EDR for endpoint/live-session incidents; reset credentials, revoke sessions, and block IPs for identity-layer incidents; document when blocking controls (firewall, MFA) already prevented the attack.
5. **Lesson Learned** — Capture detection gaps, control successes, and investigative traps.
6. **Remediation Actions** — Record hardening steps (patching, MFA, geo-restrictions, disabling exposed RDP, credential resets, user training, rule tuning only where justified).
7. **Appendix** — Map techniques to MITRE ATT&CK and catalog all artifacts/IOCs with classifications.

---

## 🧠 Core Competencies

**Security Analyst (Blue Team)**
- SIEM alert triage and rule-based detection analysis
- Multi-source log correlation: Endpoint (EDR, process trees, terminal history), Network (Proxy/Firewall/VPN), Windows Security events (4624/4625), Email Gateway
- False-positive elimination and evidence-based verdict decisions
- OSINT threat verification: VirusTotal, ANY.RUN sandbox, URLScan, URLhaus, AbuseIPDB

**Incident Response**
- Full kill-chain reconstruction: initial access → execution → privilege escalation → C2
- Credential abuse, brute-force (RDP/SSO), C2 beaconing, and live hands-on-keyboard session detection
- Layered containment: EDR host isolation, account/credential response, perimeter IP blocking
- Post-incident reporting, IOC documentation, and remediation planning

---

## 🛠️ Tools & Telemetry

| Category | Tools / Sources |
|:--|:--|
| **SIEM / Log Management** | Proxy Logs, Firewall Traffic, Email Gateway Logs, VPN / Authentication Logs, Windows Security Events (4624/4625) |
| **Endpoint Detection & Response (EDR)** | Process Trees, Process Lineage, Terminal/Bash History, Network Actions, Host Containment |
| **Threat Intelligence (OSINT)** | VirusTotal, ANY.RUN Sandbox, Hybrid Analysis, URLScan, URLhaus, AbuseIPDB |
| **Frameworks** | MITRE ATT&CK — T1110 Brute Force, T1133 External Remote Services, T1021.001 RDP, T1059.001 PowerShell, T1068 Privilege Escalation (CVE-2024-49138), T1621 MFA Request Generation, T1566 Phishing, T1204 User Execution, T1218.001 LOLBins, and more |

---

<div align="center">

*All investigations were conducted in the LetsDefend training environment. IP addresses, hostnames, file hashes, accounts, and indicators shown are lab artifacts.*

</div>
