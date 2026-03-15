# GDPR Compliance Checklist – Web-based Booking System

| **Result** | **Personal data mapping and minimization** | **Notes**|
| :----: | :--- | :---:|
| &nbsp;✅ | Have all personal data collected and processed in the system been<br> identified? (e.g., name, email, age, username) | We identified that the system collects Email, Password, Date of Birth, and Role.|
| &nbsp;✅| Have you ensured that only necessary personal data is collected (data minimization)? | The system only asks for what it needs to function (Auth + Age verification).|
| &nbsp;✅ | Is user age recorded to verify that the booker is over 15 years old? | Verified during the registration process (Spec 6).|

---

| **Result** | **User registration and management** | **Notes**|
| :----: | :--- | :---|
| &nbsp;❌ | Does the registration form (page) include GDPR-compliant consent for processing<br> personal data (e.g., acceptance of the privacy policy)?|
| &nbsp;⚠️ | Can users view, edit, and delete their own personal data via their account? | Users can view their profile, but we didn't see an "Edit" or "Delete my account" button.|
| &nbsp;✅ | Is there a mechanism for the administrator to delete a reserver in<br> accordance with the "right to be forgotten"? | Spec 5 confirmed Mari can delete reservers (even if it's only via API).|
| &nbsp;✅ | Is underage registration (under 15 years) and booking functionality restricted? | Tested and blocked by the system.|

---

| **Result** | **Booking visibility** | **Notes** |
| :----: | :--- | :---|
| &nbsp;✅ | Are bookings visible to non-logged-in users only at the resource level<br> (without any personal data)? | The frontend table hides the "Reserver" column for guests.|
| &nbsp;❌ | Is it ensured that names, emails, or other personal data of bookers are not exposed<br> publicly or to unauthorized users? | **Critical Leak.** The API /api/users and /api/reservations exposes emails and tokens to everyone.|

--- 

| **Result** | **Access control and authorization** | **Notes**|
| :----: | :--- | :--- |
| &nbsp;❌ | Have you ensured that only administrators can add, modify, and delete<br> resources and bookings? | Due to IDOR, a Reserver can modify others' bookings.|
| &nbsp;✅ | Is the system using role-based access control (e.g., reserver vs. administrator)? | The system distinguishes between Guest, Reserver, and Admin roles.|
| &nbsp;⚠️| Are administrator privileges limited to ensure GDPR compliance (e.g., administrators<br> cannot use data for unauthorized purposes)? | Hard to verify, but the Admin has broad access to all user tokens.|

---

| **Result** | **Privacy by Design Principles** | **Notes**
| :----: | :--- | :--- |
| ✅| Has Privacy by Default been implemented (e.g., collecting the minimum data by default)? |
| ✅ | Are logs implemented without unnecessarily storing personal data? | ex: [ "798412a0-c546-40cf-8fa4-0fe912db99c0" ] mari@doe.com 2 2028-12-01T11:11 2029-11-11T11:11|
| ⚠️ | Are forms and system components designed with data protection in mind<br> (e.g., secured login, minimal fields)? | Login is functional, but the API leak shows poor design security. |

---

| **Result** | **Data security** | **Notes**
| :----: | :--- | :--- |
| ✅ | Are CSRF, XSS, and SQL injection protections implemented? | The site uses token |
| ✅ | Are passwords securely hashed using a strong algorithm (e.g., bcrypt, Argon2)? | Password are well hashed in the database|
| ❌ | Are data backup and recovery processes GDPR-compliant? | Are data backup and recovery processes GDPR-compliant? (No documentation found). |
| ✅ | Is personal data stored in data centers located within the EU? | Since it's a local lab (localhost), it's stored on your machine in the EU. |

---

| **Result** | **Data anonymization and pseudonymization** | **Notes** |
| :----: | :--- | :--- |
| &nbsp;⚠️| Is personal data anonymized where possible? | Not really, emails are used as identifiers.
| &nbsp;✅ | Are pseudonymization techniques used to protect data while maintaining its utility? | The use of UUID/Tokens instead of showing database IDs in the URL is a form of pseudonymization. |

---

| **Result** | **Data subject rights** | **Notes** |
| :----: | :--- | :--- |
| &nbsp;❌ | Can users download or request all personal data related to them (data access request)? | No "Export my data" button found.
| &nbsp;❌ | Is there an interface or process for users to request the deletion of their personal data? | No interface for this. |
| &nbsp;❌ | Can users withdraw their consent for data processing? | No setting to withdraw consent once registered. |

---

| **Result** | **Documentation and communication** | **Notes** |
| :----: | :--- | :--- |
| ❌ | Is there a privacy policy available to users during registration and easily accessible? | The links /privacypolicy, /terms, etc., are currently blank. |
| ❌ | Are administrators and developers provided with documented data protection practices <br>and processing activities? |
| ❌| Is there a documented data breach response process (e.g., how to notify authorities <br>and users of a breach)? |

---

**Symbols used:**  
✅ Pass 
❌ Fail   
⚠️ Attention
