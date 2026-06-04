# Cash Capital Bank — Information Security Policy
## Document Ref: CCB-POL-SEC-002: Technical Vulnerability & Patch Management Policy

| Version | Date | Author | Reviewer | Classification |
| :--- | :--- | :--- | :--- | :--- |
| v1.0 | June 2026 | Joseph Agyapong | Chief Information Security Officer | Internal Use Only |

---

### 1. Purpose
This policy defines the structural requirements for identifying, assessing, and remediating software vulnerabilities within Cash Capital Bank. This ensures engineering baselines mitigate operational risk and aligns with the ISO 27002 control objective: *To prevent exploitation of software vulnerabilities*.

### 2. Scope
This policy encompasses all production servers, endpoint workstations (laptops/desktops), network infrastructure appliances, and internally developed software owned or operated by Cash Capital Bank.

### 3. Policy Statements

#### 3.1 Software Installation Restrictions
* **Standard User Restrictions:** Standard corporate endpoint users are strictly prohibited from possessing local administrative privileges on bank-issued hardware.
* **Application Control:** Cash Capital Bank enforces application whitelisting (Deny-by-Default). Only software cryptographically signed, vetted, and distributed via the enterprise software management platform is allowed to execute.

#### 3.2 Vulnerability Scanning Baseline
* Internal and external infrastructure must undergo automated vulnerability scanning weekly.
* High-risk zones, such as the public-facing banking web applications and API endpoints, must undergo daily automated scanning alongside annual third-party penetration testing.

#### 3.3 Patch Remediation Timelines
Upon the discovery or release of a vendor security patch, vulnerabilities must be prioritized and remediated based on their Common Vulnerability Scoring System (CVSS) rating:

| Severity | CVSS Score | Remediation Deadline |
| :--- | :--- | :--- |
| **Critical** | 9.0 – 10.0 | Within **72 Hours** |
| **High** | 7.0 – 8.9 | Within **14 Days** |
| **Medium** | 4.0 – 6.9 | Within **30 Days** |
| **Low** | 0.1 – 3.9 | Within **90 Days** / Next Scheduled Cycle |

### 4. Enforcement and Compliance
Exceptions to patch deployment timelines due to legacy system compatibility must be formally documented, backed by compensating controls (such as isolated network segmentation), and signed off by the CISO.
