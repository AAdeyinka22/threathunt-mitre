

# 🚨 APT Threat Hunting in UK Rail Transportation

### MITRE ATT&CK | Threat Intelligence | Detection Engineering

---

## 📌 Overview

This project presents a **structured threat hunting exercise** focused on **Advanced Persistent Threat (APT) groups** and their potential impact on the **United Kingdom rail transportation sector**.

Using real-world threat intelligence and the **MITRE ATT&CK framework**, the project identifies adversary behaviors, maps Tactics, Techniques, and Procedures (TTPs), and translates them into **actionable detection strategies**.

---

## 👤 Author

**Martins Adeyanju**

Cybersecurity Analyst

---

## 🎯 Objectives

* Identify threat actors relevant to **UK rail infrastructure**
* Map adversary behaviors to **MITRE ATT&CK Enterprise**
* Analyze **malware, CVEs, and attack patterns**
* Develop **threat hunting hypotheses**
* Provide **defensive recommendations for critical infrastructure**

---

## 🌍 Scope

| Category       | Details                                             |
| -------------- | --------------------------------------------------- |
| Target Country | United Kingdom 🇬🇧                                 |
| Sector         | Rail Transportation / Critical Infrastructure       |
| Threat Focus   | Disruption, Espionage, Credential Theft, Ransomware |
| Framework      | MITRE ATT&CK Enterprise                             |

---

## 🧠 Threat Actors Analyzed

* **FIN7** – Financial cybercrime, ransomware, credential theft
* **Electrum** – ICS/OT attacks, destructive malware
* **DarkHotel** – Spear phishing, executive targeting
* **GhostSec** – Hacktivism, disruption campaigns
* **SideCopy** – Espionage-focused operations
* **Predatory Sparrow** – Infrastructure disruption

---

## 🛠️ Tools & Resources

* **MITRE ATT&CK Navigator** – TTP mapping & visualization
* **SOCRadar** – Threat intelligence platform
* **OSINT Sources** – CVEs, malware intelligence, sector reports

---

## 🔬 Methodology

This project follows a **real-world threat hunting workflow**:

### 1️⃣ Threat Intelligence Collection

* Identified threat actors using intelligence platforms
* Extracted:

  * Malware families
  * CVEs
  * Target sectors and regions

---

### 2️⃣ MITRE ATT&CK Mapping

Mapped adversary techniques including:

* `T1133` – External Remote Services
* `T1071.001` – Web Protocols
* `T1543` – Create or Modify System Process
* `T1005` – Data from Local System
* `T1550` – Use Alternate Authentication Material
* `T1583.003` – Virtual Private Server

---

### 3️⃣ Hypothesis-Driven Hunting

Example:

> If FIN7 is active in a UK rail environment, anomalous credential access and suspicious remote connections should be observable.

---

### 4️⃣ Malware & CVE Analysis

**Observed Malware:**

* Mimikatz
* Carbanak
* KillDisk
* GreyEnergy
* PlugX variants

**Sample CVEs:**

* CVE-2025-42957
* CVE-2025-8088
* CVE-2024-40711
* CVE-2024-3806

---

### 5️⃣ Behavioral Analysis

Common attacker patterns:

* Exploitation of public-facing systems
* Credential dumping & reuse
* Living-off-the-land techniques (LOLBins)
* Command & Control via web protocols

---

## 📊 Key Findings

### 🔥 Shared Techniques

* Remote access exploitation (`T1133`)
* Credential abuse (`T1550`, `T1003`)
* Web-based C2 (`T1071.001`)
* Persistence via process manipulation (`T1543`)

---

### 🚆 Rail Sector Risks

* High dependency on **real-time systems**
* IT/OT convergence increases attack surface
* Disruption can impact **public safety and national operations**

---

### ⚠️ Detection Gaps

* Limited monitoring of remote services
* Weak credential activity visibility
* Lack of OT-focused detection
* Insufficient behavioral analytics

---

## 🛡️ Recommendations

* Monitor remote access (VPN, RDP, external services)
* Detect credential dumping and abnormal authentication
* Enable process monitoring (Event ID 4688 / Sysmon ID 1)
* Segment IT and OT environments
* Deploy EDR/XDR with behavioral detection
* Conduct regular ATT&CK-based threat hunts

---

## 🧪 How to Replicate

1. Go to [https://attack.mitre.org/groups](https://attack.mitre.org/groups)
2. Research selected threat actors
3. Open [https://mitre-attack.github.io/attack-navigator](https://mitre-attack.github.io/attack-navigator)
4. Create a new **Enterprise layer**
5. Map techniques per actor
6. Assign colors per group
7. Overlay layers for comparison
8. Document findings

---

## 📸 Screenshots

*(Add your screenshots here — recommended for recruiters)*

* Threat Intelligence Dashboard (SOCRadar)
* MITRE ATT&CK Navigator Layers
* Technique Mapping Views
* Comparative Analysis

---

## 💡 Key Takeaway

This project demonstrates how to translate:

**Threat Intelligence → ATT&CK Mapping → Detection Engineering**

into a **practical threat hunting workflow** applicable to real-world **critical infrastructure environments**.

---

## 🔗 References

* MITRE ATT&CK – [https://attack.mitre.org](https://attack.mitre.org)
* MITRE ATT&CK Navigator – [https://mitre-attack.github.io/attack-navigator](https://mitre-attack.github.io/attack-navigator)
* SOCRadar – [https://socradar.io](https://socradar.io)

---

## ⭐ If you found this useful

Give it a ⭐ and connect with me — always open to collaboration in:

* Threat Hunting
* Detection Engineering
* SOC Operations

---

If you want next-level polish, I can:

* Add **badges + visuals (very recruiter-friendly)**
* Create a **GitHub repo structure (folders, naming, files)**
* Or turn this into a **portfolio website project**

Just say 👍
