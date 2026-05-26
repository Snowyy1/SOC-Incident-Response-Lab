# SOC Incident Response Lab

A hands-on cybersecurity portfolio focused on real-world SOC investigations using SIEM (Splunk), Sysmon telemetry, firewall logs, and email security analysis.

This repository simulates enterprise-level security operations workflows, including phishing analysis, endpoint detection, and malware investigation.

---

## 🧠 Objective

This lab demonstrates practical skills in:

- Security Incident Triage
- Threat Detection & Analysis
- Email Phishing Investigation
- Endpoint Process Monitoring (Sysmon)
- Network Traffic & Firewall Analysis
- Command & Control (C2) Detection
- MITRE ATT&CK Mapping
- Escalation Decision-Making

---

## 🛠️ Tools & Technologies

- Splunk (SIEM)
- Sysmon (Windows Event Logging)
- Firewall Logs
- Email Security Logs
- VirusTotal
- Windows PowerShell Analysis
- Process Tree Investigation

---

## 📁 Case Studies

Each case represents a real SOC-style investigation with structured analysis, findings, and remediation steps.

---

### 🟡 Case 01 – HR Onboarding Email (False Positive)

- External onboarding email containing HR-related access link  
- Validated against internal onboarding communications  
- No malicious execution or payload delivery detected  
- Firewall blocked outbound access attempt  
- Classified as legitimate business workflow  

📂 `Case-01-False-Positive-Phishing`

---

### 🟡 Case 02 – Amazon Delivery Phishing (Blocked)

- Email impersonating Amazon delivery service  
- Shortened URL (bit.ly) used for obfuscation  
- No prior legitimate Amazon communication found  
- VirusTotal flagged URL as malicious (low vendor consensus)  
- Firewall successfully blocked outbound access attempt  

📂 `Case-02-Amazon-Phishing`

---

### 🟠 Case 03 – Microsoft Phishing Campaign (Allowed Access)

- Typosquatted Microsoft login domain (m1crosoftsupport.co)  
- Malicious login page accessed via allowed firewall rule  
- No credential submission or POST requests observed  
- External IP associated with phishing infrastructure  
- Requires user awareness and domain blocking  

📂 `Case-03-Microsoft-Phishing`

---

### 🟡 Case 04 – Windows Process Anomaly (False Positives)

- Sysmon alerts triggered on legitimate Windows system processes  
- Observed processes:
  - taskhostw.exe
  - rdpclip.exe
  - WUDFHost.exe
  - svchost.exe  
- All binaries executed from valid system directories  
- No evidence of persistence, injection, or malicious child processes  
- Determined to be normal OS behavior (rule tuning required)  

📂 `Case-04-System-Process-Anomalies`

---

### 🔴 Case 05 – PowerShell C2 Compromise (Critical Incident)

- PowerShell executed from user context via explorer.exe  
- Fileless execution using IEX download cradle  
- Remote script retrieved from GitHub (raw.githubusercontent.com)  
- Powercat used to establish reverse shell connection  
- Command-and-control (C2) established via ngrok tunnel (2.tcp.ngrok.io)  
- Post-exploitation tools observed (PowerView.ps1)  
- Evidence of data staging (ZIP archive creation in Downloads\exfiltration)  

**Impact:**
- Full endpoint compromise confirmed  
- Remote attacker control established  
- Data exfiltration preparation observed  

📂 `Case-05-PowerShell-C2-Compromise`

---

## 📊 Skills Demonstrated

### Detection & Analysis
- Log correlation across multiple data sources  
- Attack chain reconstruction  
- Suspicious behavior identification  

### Incident Response
- Triage decision-making  
- Escalation assessment  
- Remediation planning  

### Threat Intelligence
- Domain reputation analysis  
- URL risk evaluation  
- IOC extraction  

---

## 📈 Key Focus Areas

- SOC Tier 1 → Tier 2 readiness  
- Blue Team operations  
- Real-world attack simulation analysis  
- Alert validation and false positive reduction  

---

## 🚨 Disclaimer

This repository is based on simulated SOC scenarios for educational and portfolio purposes provided by THM. All data is structured for cybersecurity training and demonstration.


Open to SOC Analyst / Cybersec
