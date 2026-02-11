# 1️⃣ Introduction

**Testers:**  
- Names:  Athénaïs Bruniaux and Romane Hardouin

**Purpose:**  
- Identify as many anomalies and vulnerabilities as possible and categorize the findings. Vulnerabilities such as: Authentication and Authorization, Input Validation,  Session Management, Data Encryption.

**Scope:**  
- Tested components:  
User registration and input handling  
Input validation mechanisms   
Sensitive data encryption  
Token Management  

- Exclusions:  
Error Handling and Logging  
Third-Party Components  
Usability and Performance  
GDPR Compliance  
Privacy by Design (PbD) Principles

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
The web application’s user registration, input validation, and sensitive data handling mechanisms were tested. Several critical and medium vulnerabilities were identified, including SQL injection, weak or plain-text password storage, absence of CSRF protection, lack of domain validation, and weak password policies. Immediate remediation is recommended to protect user data and maintain system integrity and confidentiality

**Overall risk level:** High

**Top 5 immediate actions:**  

1. Prevent SQL Injection and Path Traversal
  Apply strict input validation on all user inputs, especially in registration forms.
  Use parameterized queries or prepared statements to interact with the database.
  Sanitize any user-supplied data to prevent manipulation of database commands.

2. Secure Password Storage and Enforce Strong Password Policies
  Hash and salt all passwords using strong algorithms (e.g., bcrypt, Argon2).
  Reject weak passwords, including blanks or trivial patterns.
  Encourage or require Multi-Factor Authentication (MFA) for all accounts.

3. Add CSRF Protection for Forms and Sensitive Actions
  Implement server-side anti-CSRF tokens for registration and other critical forms.
  Use double-submitted cookies or per-request tokens to validate user actions.

4. Validate and Restrict Input for Email and Other Fields
  Ensure only valid email domains are accepted.
  Reject clearly invalid or malformed data to prevent logical bypasses or errors.

5. Encrypt Sensitive Data and Secure Error Handling
  Encrypt personal and authentication data both at rest and in transit using up-to-date algorithms.
  
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


| ID | Severity | Finding | Description | Evidence / Proof |
|------|-----------|----------|--------------|------------------|
| F-01 | 🔴 High | SQL Injection in registration | Input field answers differently depends of the SQL injection | Different answers with AND 1=1 AND 1=2 <img width="710" height="435" alt="sql injection" src="https://github.com/user-attachments/assets/02503812-9e0b-48b4-a1ba-0d0262eb633a" /> <img width="691" height="528" alt="sql injection2" src="https://github.com/user-attachments/assets/5dc0984f-301d-41d9-a4b4-c7ad24d20beb" />|
| F-02 | 🔴 High | Plain-text password storage | The database stores passwords without any hashing or encryption. |SELECT * FROM booking_users; shows readable passwords <img width="912" height="167" alt="image" src="https://github.com/user-attachments/assets/9074e856-479a-4ccc-8fcc-6b3d45135aa7" />|
| F-03 | 🟠 Medium | Absence of Anti-CSRF Tokens | The CSRF token is inexistant on the server side| No mention of the token on the request <img width="1390" height="1044" alt="image" src="https://github.com/user-attachments/assets/f9eb9d56-5b79-410f-9451-0fa98e26e56b" />|
| F-04 | 🟡 Low | Lack of Domain Validation | The system accepts fake email domains (ex: @abcde) | Registration successful with non-existent domain @qfknlfv <img width="912" height="167" alt="image" src="https://github.com/user-attachments/assets/1d47a297-4be1-4916-9b69-3dfc15daa552" />|
| F-05 | 🟡 Low | Weak password policy | Accepts passwords consisting only of blank spaces (" "). | Account created with " " as password.<img width="912" height="167" alt="image" src="https://github.com/user-attachments/assets/3885fd00-e920-46c4-9a90-f8f5dfe4b1d3" />|

---

# 5️⃣ OWASP ZAP Test Report (Attachment)

 
- [zap_report_round1.md](./zap_report_round1.md)
---

> [!NOTE]
> 📁 **Attach full report:** → [check itslearning](https://centria.itslearning.com/ContentArea/ContentArea.aspx?LocationID=10880&LocationType=1&ElementID=652074)

---


