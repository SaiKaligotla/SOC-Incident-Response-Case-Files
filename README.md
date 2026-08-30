<div align="center">

# 🛡️ SOC Incident Response Case Files

### Hands-on Security Operations Center investigations — triage, threat hunting, containment, and post-incident reporting

![Platform](https://img.shields.io/badge/Platform-LetsDefend-0a66c2?style=for-the-badge)
![Total Cases](https://img.shields.io/badge/Total%20Cases-3-success?style=for-the-badge)
![True Positives](https://img.shields.io/badge/True%20Positives-2-red?style=for-the-badge)
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
| **Total Investigations** | 3 |
| 🔴 True Positives — Malicious Activity Confirmed | 2 |
| 🔵 False Positives — Benign Activity Triaged | 1 |
| 🎣 Phishing & Email Threats | 1 |
| 💻 Endpoint & Malware Compromise | 1 |
| 🌐 Network & Perimeter Anomalies | 1 |

**Status legend:**
🔴 **True Positive** — malicious activity confirmed (threat contained or blocked)
🔵 **False Positive** — benign activity ruled out after investigation

---

## 🗂️ Case Files

> 📁 **Naming convention:** `EventID_<ID> - <Rule Name>.<ext>` · **Folder structure:** phishing → `Phishing_Investigations/` · endpoint/malware → `Endpoint_Compromise/` · network → `Network_Anomalies/`

### 🎣 Phishing & Email Threats

| Event ID | Rule Name | Threat Type | Status | Case File |
|:--|:--|:--|:--|:--|
| 257 | SOC282 - Phishing Alert - Deceptive Mail Detected | AsyncRAT / Phishing | 🔴 True Positive | `EventID_257 - SOC282 - Phishing Alert - Deceptive Mail Detected.pdf` |

### 💻 Endpoint & Malware Compromise

| Event ID | Rule Name | Threat Type | Status | Case File |
|:--|:--|:--|:--|:--|
| 44 | SOC113 - Suspicious hh.exe Usage | Malicious CHM / LOLBin (hh.exe) | 🔵 False Positive | `EventID_44 - SOC113 - Suspicious hh.exe Usage.md` |

### 🌐 Network & Perimeter Anomalies

| Event ID | Rule Name | Threat Type | Status | Case File |
|:--|:--|:--|:--|:--|
| 303 | SOC325 - Unauthorized Cloud Region Access Attempt Detected | Brute-Force / Web Attack | 🔴 True Positive (Blocked) | `EventID_303 - SOC325 - Unauthorized Cloud Region Access Attempt Detected.pdf` |

---

## 🔍 Investigation Methodology

Every case follows the same telemetry-driven workflow, documented as an Official Incident Report:

1. **Alert** — Review rule name, severity, MITRE mapping, affected host, and timestamp; determine initial urgency.
2. **Detection** — Pivot across Proxy, Firewall, Endpoint (EDR), and Email logs; reconstruct process lineage (parent → child) and network connections.
3. **Analysis** — Verify file hashes, IPs, domains, and URLs via OSINT (VirusTotal, ANY.RUN, URLScan, URLhaus, AbuseIPDB); build an attack narrative and then challenge it against benign explanations.
4. **Containment** — Contain affected hosts via EDR when a true positive is confirmed; document when blocking controls already prevented the attack; avoid unnecessary disruption for false positives.
5. **Lesson Learned** — Capture detection gaps, control successes, and process improvements.
6. **Remediation Actions** — Record hardening steps (patching, MFA, credential resets, user training, rule tuning only where justified).
7. **Appendix** — Map techniques to MITRE ATT&CK and catalog all artifacts/IOCs with classifications.

---

## 🧠 Core Competencies

**Security Analyst (Blue Team)**
- SIEM alert triage and rule-based detection analysis
- Multi-source log correlation: Endpoint, Network (Proxy/Firewall), Email Gateway
- False-positive elimination and evidence-based verdict decisions
- OSINT threat verification: VirusTotal, ANY.RUN sandbox, URLScan, URLhaus, AbuseIPDB

**Incident Response**
- Attack-chain reconstruction and hypothesis-driven investigation
- C2 beaconing and lateral movement tracking
- EDR host containment and remediation recommendations
- Post-incident reporting and IOC documentation

---

## 🛠️ Tools & Telemetry

| Category | Tools / Sources |
|:--|:--|
| **SIEM / Log Management** | Proxy Logs, Firewall Traffic, Email Gateway Logs |
| **Endpoint Detection & Response (EDR)** | Process Trees, Process Lineage, Terminal History, Network Actions, Host Containment |
| **Threat Intelligence (OSINT)** | VirusTotal, ANY.RUN Sandbox, Hybrid Analysis, URLScan, URLhaus, AbuseIPDB |
| **Frameworks** | MITRE ATT&CK — T1566 Phishing, T1204 User Execution, T1218.001 LOLBins, T1078 Valid Accounts / Cloud Region restrictions, and more |

---

<div align="center">

*All investigations were conducted in the LetsDefend training environment. IP addresses, hostnames, file hashes, and indicators shown are lab artifacts.*

</div>
