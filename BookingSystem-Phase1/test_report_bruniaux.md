# 1️⃣ Introduction

**Tester(s):**  
- Name:  Athénaïs Bruniaux and Romane Hardouin

**Purpose:**  
- Identify as many anomalies and vulnerabilities as possible and categorize the findings. Vulnerabilities such as: Authentication and Authorization, Input Validation, Data Encryption.

**Scope:**  
- Tested components:  
- Exclusions:  
- Test approach: Gray-box

**Test environment & dates:**  
- Start: 01/02/2026 
- End:  04/02/2026
- Test environment details (OS, runtime, DB, browsers):
  
  OS: Windows 11 Version 25H2 (Build 26200.7840)
  
  Runtime: Docker 29.1.5
  
  Database: PostgreSQL
  
  Brower: Mozilla Firefox  

**Assumptions & constraints:**  
- First time using Docker and OWASP Zap.

# 2️⃣ Executive Summary

**Short summary (1-2 sentences):**  

**Overall risk level:** (Low / Medium / High / Critical)

**Top 5 immediate actions:**  
1.  
2.  
3.  
4.  
5.  

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
| F-02 | 🟠 Medium | Session fixation | Session ID remains unchanged after login | Burp log or response headers |
| F-03 | 🟡 Low | Weak password policy | Accepts passwords like "12345" | Screenshot of registration success |

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


