# ISO 27001 ISMS Control Mapping Framework
**Organization:** Cash Capital Bank  
**Author:** Joseph Agyapong  
**Target Standard:** ISO/IEC 27001:2022 & ISO/IEC 27002  

## 📌 Project Overview
This repository contains the practical Information Security Management System (ISMS) control mapping architecture designed for **Cash Capital Bank**. The objective of this project is to bridge the gap between high-level compliance objectives and technical, enforceable engineering controls required to successfully pass an ISO 27001 certification audit.

The documentation outlines real-world financial sector scenarios, mapping specific control objectives to technical implementation strategies and the precise audit artifacts required to prove compliance.

---

## 🗺️ Core Control Mapping Matrix

| ISO 27002 Control Objective | Bank-Specific Threat Scenario | Technical / Administrative Safeguard | Audit Evidence & Artifacts |
| :--- | :--- | :--- | :--- |
| **To prevent unauthorized access to systems and applications** | Unauthorized users or branch tellers accessing sensitive SWIFT or corporate credit databases. | • Role-Based Access Control (RBAC)<br>• Phishing-resistant Multi-Factor Authentication (MFA)<br>• Just-In-Time (JIT) administrative access | • Active Directory GPO configurations<br>• IAM provisioning logs<br>• MFA enforcement reports |
| **To prevent exploitation of software vulnerabilities** | Malicious execution of unvetted third-party tools or malware exploitation of unpatched systems. | • Application Whitelisting (Deny-by-Default)<br>• Removal of local administrative rights<br>• 72-hour critical patch management lifecycle | • Local Group Policy software restriction settings<br>• Endpoint Central/WSUS patch history logs |
| **To ensure consistent and effective information security incident management** | Unreported data leaks or unencrypted PII exposing the bank to regulatory penalties. | • Standard Operating Procedure (SOP) for anomaly reporting<br>• Direct SIEM/SOC ingestion pipeline for employee-reported weaknesses | • Phishing reporting button metrics<br>• Sanitized SOC incident response tickets |
| **To prevent loss, damage, theft, or compromise of sensitive data** | Physical data theft or exposure of high-net-worth client paperwork to unauthorized cleaning staff or visitors. | • 5-minute automated screen lock timeout<br>• Mandated physical clear-desk policy<br>• Secure lockbox/shredding bins | • Screensaver timeout registry GPOs<br>• Internal physical compliance walk-through logs |

---

## 🛠️ Implementation Details

### 1. Identity & Access Management (IAM)
To satisfy the access control objective, Cash Capital Bank implements a strict identity baseline. Users are separated by organizational units (OUs) matching their business function. 
* **Enforcement:** Authentication requests to core banking infrastructure are gated behind conditional access policies requiring managed device compliance and cryptographic MFA.

### 2. Endpoint Hardening & Vulnerability Lifecycle
End-user computing assets are locked down to prevent client-side entry vectors.
* **Enforcement:** AppLocker policies ensure that only software originating from `C:\Program Files\` and signed by trusted enterprise vendors can run. Vulnerability remediation timelines are strictly governed by asset criticality scoring.

### 3. Incident Reporting Infrastructure
The "human firewall" is operationalized through structured reporting channels.
* **Enforcement:** Employees utilize an integrated reporting tool that parses headers and artifacts of suspected malicious emails or system behavior, automatically creating a low-severity alert in the Security Operations Center (SOC) platform for analyst triage.

### 4. Physical Asset Protection
Physical security boundaries are treated with the same rigor as digital perimeters.
* **Enforcement:** Workstations are audited out-of-hours. Any printed customer non-public personal information (NPI) left unattended results in an automated warning ticket dispatched to the respective department head.

---

## 📋 Audit Readiness Checklist
Before the external registrar arrives, the following validation steps must be completed:
- [ ] Run a comprehensive credential audit to ensure zero active accounts bypass MFA.
- [ ] Verify endpoint agent compliance exceeds 98% network-wide.
- [ ] Review the previous 90 days of SOC incident logs to ensure continuous monitoring verification.
- [ ] Conduct unannounced after-hours physical security walk-throughs across corporate facilities.

---
*Disclaimer: This repository contains architectural frameworks and sanitized implementation templates modeled for compliance demonstration purposes. No real production configurations, corporate keys, or sensitive banking infrastructure data are stored here.*
