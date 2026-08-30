# 🛡️ Security Operations Center (SOC) Case Files

This repository serves as a practical portfolio demonstrating my capabilities as a **Security Analyst** and **Incident Responder**. It contains technical documentation and IR reports from investigating live-simulated cyber attacks in the LetsDefend enterprise environment. 

Each case file is documented using a strict 7-part methodology to establish timelines, identify attack vectors, and justify containment actions based on hard telemetry.

## 🎯 Targeted Competencies

* **As a Security Analyst:** Triaging raw SIEM alerts, correlating multi-source logs (Endpoint, Network, Email), eliminating false positives, and utilizing OSINT (VirusTotal, ANY.RUN) to verify threat intelligence.
* **As an Incident Responder:** Formulating hypotheses, tracking lateral movement and C2 beaconing, executing rapid host containment, formulating remediation strategies, and writing auditable post-incident reports.

---

## 🗂️ Investigation Categories

### 🎣 Phishing & Email Threats
| Event ID | Rule Name | Threat Type | Status | File Name |
| :--- | :--- | :--- | :--- | :--- |
| 257 | SOC282 - Deceptive Mail Detected | AsyncRAT / Phishing | 🔴 Contained | `EventID_257 - SOC282 - Phishing Alert - Deceptive Mail Detected.pdf` |

### 💻 Endpoint & Malware Compromise
| Event ID | Rule Name | Threat Type | Status | File Name |
| :--- | :--- | :--- | :--- | :--- |
| TBD | (Future Alert) | (Future Threat) | 🟢 TBD | TBD |

### 🌐 Network & Perimeter Anomalies
| Event ID | Rule Name | Threat Type | Status | File Name |
| :--- | :--- | :--- | :--- | :--- |
| 303 | SOC325 - Unauthorized Cloud Region Access Attempt Detected | Brute-Force / Web Attack | 🔴 Contained | `EvendtID_303- SOC325 - Unauthorized Cloud Region Access Attempt DetectedName of triggered alert.pdf` | 

---

## 🛠️ Tools & Telemetry Analyzed
* **SIEM / Log Management:** Proxy Logs, Firewall Traffic, Email Gateway
* **Endpoint Detection & Response (EDR):** Process Trees, Terminal History, Network Actions
* **Threat Intelligence (OSINT):** VirusTotal, ANY.RUN Sandbox, URLhaus
