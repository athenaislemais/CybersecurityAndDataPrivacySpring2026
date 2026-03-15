# Privacy Policy

**Effective Date:** March 11, 2026  
**Project:** Resource Booking System - Phase 4  
**Audit Status:** Updated based on OWASP ZAP Security Analysis

## 1. Introduction
This Privacy Policy explains how the **Resource Booking System** collects, uses, and protects your personal data. We are committed to ensuring that your privacy is protected in accordance with the General Data Protection Regulation (GDPR).

## 2. Data Controller
The data controller for this application is the **System Administrator (Admin)**. All data processing is handled within the local Docker environment deployed for this project.

## 3. Data We Collect
We follow the principle of data minimization, collecting only:
* **Account Information:** Email address and password (stored as a secure hash).
* **Verification Data:** Date of birth (to verify the 15-year age requirement).
* **System Data:** User roles and session identifiers.

## 4. Purpose of Processing
Your data is processed for authentication, managing resource reservations, and ensuring compliance with age restrictions (Spec 6).

## 5. Data Visibility and Sharing
* **Guests:** Can view resource status but cannot see reserver identities (Spec 8).
* **Administrators:** Have access to user lists for management and deletion (Spec 5).
* **Security:** We do not share data with third parties. Automated scans (ZAP) confirm that access control is enforced, though a Cross-Domain misconfiguration has been noted for remediation.

## 6. Security Measures (Technical Verification)
Based on our security audits, the following protections are active:
* **CSRF Protection:** Every state-changing request (login, register, booking) is protected by a unique `csrf_token`.
* **Secure Transport:** The system utilizes **HSTS (HTTP Strict Transport Security)** to enforce secure connections.
* **Infrastructure Security:** The application runs on an **Nginx** web server, providing a robust layer for managing requests and data flow.
* **Password Hashing:** Passwords are encrypted and never stored in plain text.

## 7. Data Storage and Retention
* **Location:** Stored locally in a secure database container.
* **Retention:** Data is kept as long as the account exists. While no "Delete Account" button is currently in the UI, users can exercise their "Right to be Forgotten" by contacting the Admin.

## 8. Your Rights (GDPR)
In compliance with GDPR, you have the right to access your data, request rectification, and request the deletion of your personal information.

## 9. Cookie Policy
We use strictly necessary cookies for security and session management:
* **`csrf_token`:** Prevents Cross-Site Request Forgery.
* **Session Cookies:** Identifies your authenticated state.

## 10. Contact
For any privacy-related inquiries, please contact the System Administrator.
