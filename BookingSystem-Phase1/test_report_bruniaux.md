# 1️⃣ Introduction

**Testers:**  
- Name:  Athénaïs Bruniaux and Romane Hardouin

**Purpose:**  
- Identify as many anomalies and vulnerabilities as possible and categorize the findings. Vulnerabilities such as: Authentication and Authorization, Input Validation, Data Encryption.

**Scope:**  
- Tested components:  
- Exclusions:  
- Test approach: Grey-box

**Test environment & dates:**  
- Start: 01/02/2026 
- End:  04/02/2026
- Test environment details (OS, runtime, DB, browsers):
  
  OS: Windows 11 Version 25H2 
  
  Runtime: Docker 29.1.5
  
  Database: PostgreSQL
  
  Brower: Mozilla Firefox  

**Assumptions & constraints:**  
- First time using Docker and OWASP Zap.

# 2️⃣ Executive Summary

**Short summary:** 
The web application’s user registration, input handling, and data encryption mechanisms have several critical and medium vulnerabilities, including SQL injection, path traversal, weak passwords, absence of CSRF protection, and potential exposure of sensitive data. Immediate remediation is required to prevent exploitation and ensure the confidentiality, integrity, and security of user data.

**Overall risk level:** High

**Top 5 immediate actions:**  
1. Fix input validation and use safe database queries:
Prevent SQL injection and path traversal by validating and sanitizing all user inputs. Always use parameterized queries or prepared statements to interact with the database safely.  

2. Enforce strong passwords and add Multi-Factor Authentication (MFA):
Do not allow users to register with weak passwords. Encourage or require multi-factor authentication to make accounts more secure.  

3. Protect against Cross-Site Request Forgery (CSRF) attacks:
Add anti-CSRF tokens to forms and sensitive actions. Use techniques like double-submitted cookies, and require separate confirmation for high-risk operations to ensure the user intended to perform them.  

4. Encrypt sensitive data properly:
Identify which data is valuable and must be protected. Ensure that all sensitive data, both in transit and at rest, is encrypted using strong and well-vetted encryption algorithms.  

5. Handle errors safely and log properly:
Do not expose full error details to users, as this can reveal sensitive information. Maintain detailed logs internally to detect suspicious activity and support incident investigation.   

---

# 3️⃣ Severity scale & definitions

|  **Severity Level**  | **Description**                                                                                                              | **Recommended Action**           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
|      🔴 **High**     | A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution). | *Immediate fix required*         |
|     🟠 **Medium**    | A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF).                              | *Fix ASAP*                       |
|      🟡 **Low**      | A minor issue or configuration weakness (e.g., server version disclosure).                                                   | *Fix soon*                       |
| 🔵 **Info** | No direct risk, but useful for system hardening (e.g., missing security headers).                                            | *Monitor and fix in maintenance* |


---

# 4️⃣ Findings (filled with examples → replace)

> Fill in one row per finding. Focus on clarity and the most important issues.

| ID | Severity | Finding | Description | Evidence / Proof |
|------|-----------|----------|--------------|------------------|
| F-01 | 🔴 High | SQL Injection in registration | Input field allows `' OR '1'='1` injection | Screenshot or sqlmap result |
| F-02 | 🔴 High | Path Traversal | Allows directory traversal sequences in URL exposing server files | Evidence |
| F-03 | 🟠 Medium | Absence of Anti-CSRF Tokens | The CSRF token is not properly validated on the server side. | Burp log or response headers |
| F-04 | 🟡 Low | Application Error Disclosure | Reveals detailed internal error messages when invalid input is submitted | Screenshot of registration success |
| F-05 | 🟡 Low | Weak password policy | Accepts passwords consisting only of blank spaces (" "). | <img width="912" height="167" alt="image" src="https://github.com/user-attachments/assets/3885fd00-e920-46c4-9a90-f8f5dfe4b1d3" />
 |


---

> [!NOTE]
> Include up to 5 findings total.   
> Keep each description short and clear.

---

# 5️⃣ OWASP ZAP Test Report (Attachment)

 
- [zap_report_round1.md](./zap_report_round1.md)
---

> [!NOTE]
> 📁 **Attach full report:** → [check itslearning](https://centria.itslearning.com/ContentArea/ContentArea.aspx?LocationID=10880&LocationType=1&ElementID=652074)

---


