# 1️⃣ Introduction

**Tester(s):**  
- Name:  

**Purpose:**  
- Describe the purpose of this test (e.g., identify vulnerabilities in registration and authentication flows).

**Scope:**  
- Tested components:  
- Exclusions:  
- Test approach: Gray-box / Black-box / White-box

**Test environment & dates:**  
- Start:  
- End:  
- Test environment details (OS, runtime, DB, browsers):

**Assumptions & constraints:**  
- e.g., credentials provided, limited time, etc.

---

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

**Purpose:**  
- Attach or link your OWASP ZAP scan results (Markdown format preferred).

---

**Instructions:**
1. Check lecture recordings
2. Save the report as `zap_report_round1.md` and link it below.

---
> [!NOTE]
> 📁 **Attach full report:** → `check itslearning` → **Add a link here**

---1️⃣ Introduction

Tester(s):

Name: Romane Hardouin and Athénaïs Bruniaux

Purpose:

Identify vulnerabilities in registration and authentication flows.

Scope:

Tested components:

User Registration Form (Frontend)

PostgreSQL Database storage (Backend)

Exclusions:

Login functionality

User sessions

Resource booking system

GDPR compliance (not testable yet)

Test approach: Gray-box

Test environment & dates:

Start: 30/01/2026

End:

Test environment details (OS, runtime, DB, browsers):

OS: Debian Linux (VM)

Runtime: Docker version 29.2.0, build 0b9d198

DB: PostgreSQL

Browsers: Mozilla Firefox 140.4.0esr

Assumptions & constraints:

Constraints: Limited time for Phase 1. The login button is non-functional (returns 404). Access is limited to the local Docker environment only.

Assumptions: The developer claims the system follows Privacy by Design, therefore sensitive data is assumed to be encrypted from the start.

2️⃣ Executive Summary

Short summary (1-2 sentences):
The security assessment focused on the user registration flow and backend data storage to identify potential vulnerabilities in the current implementation.

Overall risk level: (Low / Medium / High / Critical)

Top 5 immediate actions:
1.
2.
3.
4.
5.

3️⃣ Severity scale & definitions
Severity Level	Description	Recommended Action
🔴 High	A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution).	Immediate fix required
🟠 Medium	A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF).	Fix ASAP
🟡 Low	A minor issue or configuration weakness (e.g., server version disclosure).	Fix soon
🔵 Info	No direct risk, but useful for system hardening (e.g., missing security headers).	Monitor and fix in maintenance
4️⃣ Findings (filled with examples → replace)

Fill in one row per finding. Focus on clarity and the most important issues.

ID	Severity	Finding	Description	Evidence / Proof
F-01	🔴 High	SQL Injection in registration	Input field allows ' OR '1'='1 injection	Screenshot or sqlmap result
F-02	🟠 Medium	Session fixation	Session ID remains unchanged after login	Burp log or response headers
F-03	🟡 Low	Weak password policy	Accepts passwords like "12345"	Screenshot of registration success

[!NOTE]
Include up to 5 findings total.
Keep each description short and clear.

5️⃣ OWASP ZAP Test Report (Attachment)

Purpose:

Attach or link your OWASP ZAP scan results (Markdown format preferred).

Instructions:

Check lecture recordings

Save the report as zap_report_round1.md and link it below.

[!NOTE]
📁 Attach full report: → check itslearning → Add a link here
