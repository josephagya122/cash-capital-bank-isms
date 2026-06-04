# Cash Capital Bank — Information Security Policy
## Document Ref: CCB-POL-SEC-001: Access Control Policy

| Version | Date | Author | Reviewer | Classification |
| :--- | :--- | :--- | :--- | :--- |
| v1.0 | June 2026 | Joseph Agyapong | Chief Information Security Officer | Internal Use Only |

---

### 1. Purpose
The purpose of this policy is to establish a secure framework for granting, modifying, and revoking access to Cash Capital Bank’s logical systems, applications, and network infrastructure. This policy directly addresses the ISO 27002 control objective: *To prevent unauthorized access to systems and applications*.

### 2. Scope
This policy applies to all employees, contractors, third-party vendors, and temporary staff who require access to Cash Capital Bank networks, core banking applications, SWIFT transaction environments, and data repositories.

### 3. Policy Statements

#### 3.1 Principle of Least Privilege & Need-to-Know
* Access to all information assets must be restricted by default. 
* Users shall only be granted the minimum level of access necessary to perform their explicit job functions (Least Privilege).
* Access to highly sensitive financial databases or corporate credit data requires strict data classification alignment (Need-to-Know).

#### 3.2 Identification and Authentication
* Every user must be uniquely identifiable via a centralized corporate identity directory (e.g., Active Directory / Azure AD). Shared or generic administrative accounts are strictly prohibited.
* **Multi-Factor Authentication (MFA):** Cryptographic, phishing-resistant MFA is mandatory for all access requests, including remote VPN connections and internal core application logins.

#### 3.3 Account Lifecycle Management
* **Provisioning:** All access requests must originate from an authorized manager and be validated by the IT Security team before provisioning.
* **De-provisioning:** Upon employee termination, HR must notify IT Security immediately. Human Resources and IT must revoke all digital and physical access within **1 hour** of the employee's departure.
* **Access Reviews:** Privilege access right reviews must be conducted quarterly for standard users and monthly for privileged administrative accounts.

### 4. Enforcement and Compliance
Any employee found to have violated this policy—including credential sharing or attempting to bypass access controls—will be subject to disciplinary action, up to and including termination of employment and legal prosecution.
