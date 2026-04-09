# APT Threat Hunting in the UK Rail Transportation Sector Using Intelligence Platforms & MITRE ATT&CK

# Project Information

Author: Martins Adeyanju

Type: Threat Intelligence & Threat Hunting

Target Country: United Kingdom

Sector Focus: Rail Transportation / Critical Infrastructure

Framework: MITRE ATT&CK Enterprise

Tools Used:

MITRE ATT&CK Navigator

SOCRadar (Threat Actor Intelligence Dashboard)

Open-source Intelligence (OSINT)

# Objective

This project conducts a structured threat hunt targeting advanced and financially motivated threat actors identified via intelligence platforms, including:

FIN7

Electrum

DarkHotel

GhostSec

SideCopy

Predatory Sparrow

# The objective is to:

Identify Tactics, Techniques, and Procedures (TTPs) relevant to rail infrastructure
Map adversary behavior to the MITRE ATT&CK framework
Analyze malware usage, CVEs, and targeting patterns
Develop actionable detection strategies for UK rail operators
# Scope
Geography: United Kingdom
Sector: Rail Transportation (Critical National Infrastructure)
Threat Focus:
Service disruption
Ransomware and extortion
Credential compromise
Operational Technology (OT) interference

# Threat Actors Analyzed (From Intelligence Dashboard)
# FIN7
Rank: 21
Financially motivated cybercrime group with advanced tooling
Known to target organizations with high operational dependency, including transport

# Associated malware:

Carbanak
Mimikatz
PowerPlant
REvil-linked tooling

# Relevance to Rail:

Credential theft for lateral movement into operational systems
Ransomware deployment targeting service disruption
# Electrum
Rank: 39
Linked to critical infrastructure attacks, including ICS/OT environments

# Associated malware:

GreyEnergy
KillDisk
TeleDoor
Exaramel

# Relevance to Rail:

Potential disruption of rail control systems
Destructive attacks affecting availability of services
🔹 DarkHotel
Rank: 48
Targets executives and high-value individuals

# Relevance to Rail:

Targeting senior rail executives for:
Credential harvesting
Strategic intelligence gathering
# GhostSec
Rank: 141
Hacktivist group

# Relevance to Rail:

Disruption campaigns
Public data leaks
Website defacement of transport services
# SideCopy
Rank: 148
Known for espionage operations

# Relevance to Rail:

Targeting sensitive transport infrastructure data
# Predatory Sparrow
Rank: 157
Conducts disruptive cyber operations

# Relevance to Rail:

Potential targeting of critical infrastructure for geopolitical impact
# Methodology
# 1. Threat Intelligence Collection

Threat actors were identified using intelligence dashboards, extracting:

Target countries (including UK relevance)
Sector targeting patterns (transport & infrastructure)
Malware associations
CVEs
ATT&CK techniques

# 2. MITRE ATT&CK Mapping

Key techniques identified from your dataset:

T1133 – External Remote Services
T1071.001 – Web Protocols
T1543 – Create or Modify System Process
T1005 – Data from Local System
T1550 – Use Alternate Authentication Material
T1583.003 – Virtual Private Server

These techniques were mapped in MITRE ATT&CK Navigator to simulate attacker behavior in rail environments.

# 3. Hypothesis-Driven Hunting

Example hypothesis:

“If FIN7 or similar actors are present in a UK rail network, anomalous credential access and suspicious remote connections should be observable.”

# 4. Malware & CVE Correlation

Observed malware trends:

Credential theft tools (Mimikatz)
Destructive malware (KillDisk)
Backdoors and persistence tools

Example CVEs:

CVE-2025-42957
CVE-2025-8088
CVE-2024-40711
CVE-2024-3806

👉 These vulnerabilities may affect systems used in rail IT/OT environments if unpatched.

# 5. Behavioral Analysis

Common attack patterns across actors:

Exploitation of public-facing infrastructure systems
Use of living-off-the-land techniques (LOLBins)
Credential dumping and privilege escalation
Command & Control via web protocols and proxy infrastructure

# Key Findings
# Shared Techniques Across Actors
Remote access exploitation (T1133)
Credential theft and reuse (T1003 / T1550)
Web-based command & control (T1071.001)
Process manipulation for persistence (T1543)

# Rail Sector Risk Insight

Rail systems are high-value targets due to:

Dependence on real-time operational systems
Integration of IT and OT environments
Potential for mass disruption and safety impact

# Detection Gaps Identified
Limited monitoring of remote access services
Weak visibility into OT environments
Insufficient alerting on credential misuse
Lack of behavioral detection for lateral movement

# Recommendations for UK Rail Defenders
Monitor:
Remote access activity (VPN, RDP, external services)
PowerShell and scripting usage
Detect:
Credential dumping behavior
Abnormal process creation (Event ID 4688 / Sysmon 1)
Harden:
Public-facing infrastructure systems
Identity and access management controls
Implement:
EDR/XDR with behavioral analytics
Network segmentation between IT and OT
Conduct:
Regular ATT&CK-based threat hunting exercises
