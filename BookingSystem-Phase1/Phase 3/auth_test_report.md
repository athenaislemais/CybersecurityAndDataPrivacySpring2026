# 🔐 Authorization Test Report - Phase 3

## 📋 Project Overview
This report documents the authorization testing for the resource booking system. The goal is to verify if the actual implementation matches the official specifications (Specs 1–8) and follows the Principle of Least Privilege (PoLP).

---
## 🧩 Specification Reference

1. The system is accessed via a web browser.  
2. Users can register and, after registration, log in to the system.  
3. A registered and logged-in user acts as either a resource reserver or an administrator.  
4. The administrator can add, remove, and modify resources and reservations.  
5. The administrator can delete the reserver.  
6. A reserver can book a resource if they are over 15 years old.  
7. Resources can be booked on an hourly basis.  
8. The booking system displays booked resources without requiring login, but does not show the reserver's identity.  
9. The system must comply with GDPR regulations.  
10. The system follows Privacy by Design (PbD) principles.  

---


## 🧑‍🦲 Guest
*Unauthenticated user. Should only access public resources.*

### ✅ Can do

* **View public resource list** — `/`
  * *Observation:* Accessible without login (Spec 8).
* **Access login form** — `/login`
  * *Observation:* Accessible (Spec 2).
* **Access registration form** — `/register`
  * *Observation:* Accessible (Spec 2).
* **View booked resources** — `/`
  * *Observation:* Displays booked resources without revealing reserver identity (Spec 8).


### ❌ Cannot do
* **Access reservation page** — `/reservation`
  * *Observation:* Blocked. Redirects to back home. (Spec 3)

### ⚠️ Vulnerabilities (GDPR Violation)
* **Access API endpoints** — `/api/reservations`
  * *Observation:* **CRITICAL VULNERABILITY** Accessible without authentication. Exposes tokens, usernames, and roles of all registered users (Violates Spec 8, 9 & 10).

---

## 🧑‍💼 Reserver
*Logged in as: `john@doe.com`*

### ✅ Can do
* **View own profile** — `/`
  * *Observation:* Functional. The application uses session cookies for authentication, so user data is not exposed in the URL(Spec 10).
* **Book a resource** — `/reservation`
  * *Observation:* Accessible. User can book on an hourly basis (Spec 7).
  * *Note:* Requires user to be over 15 years old (Spec 6).
* **Add/Update resources** — `/resources`
  * *Observation:* Accessible. User can creat ressources.

### ❌ Cannot do
* **View other user profile** 
  * *Observation:* no indication in the URL
* **Register if under 15 years old** 
  * *Observation:* Succesfuly rejeted if register with an age uder 15 years old.


### ⚠️ Vulnerabilities (GDPR Violation)
* **IDOR on Bookings** — `/reservation?id=X`
    * *Observation:* Users can access and modify bookings belonging to others by changing the ID in the URL.
* **Privilege Escalation** — `/api/resources/:id`
  * *Observation:* Users can take ownership of another user's booking by changing the "Reserver" field in the form, and subsequently delete it.
* **GDPR Compliance**
  * *Observation:* Users cannot delete their own accounts (Violation of GDPR "Right to be Forgotten").

---

## 🧑‍💼🛡️ Administrator
*High-privilege account with full control. Logged in as: `mari@doe.com`*

### ✅ Can do
* **Full System Management** 
  * *Observation:* Full control over resource management (Spec 4). Sessions are handled via cookies, not URL parameters.
* **Delete a reserver** — `/reservation?id=X`
  * *Observation:* Functional (Spec 5).
* **Manage all reservations** — `/reservations`
  * *Observation:* Can view and modify any booking (Spec 4).
* **Access API endpoints** — `/api/users`, `/api/reservations`, `/api/resources`
    * *Observation:* Can access API endponts (Spec 4 & 8).

### ❌ Cannot do
* **View all users via dedicated admin panel**
    * *Observation:* No dedicated admin page for user management exists, must use API (Spec 4 & 5 partially met).
* **Delete reserver via UI**
    * *Observation:* Cannot delete users directly through the web interface (Spec 5).
* **Delete resources via UI**
    * *Observation:* Cannot delete resources directly through the web interface (Spec 4).

---

## ⚠️ Findings

#### Critical Vulnerabilities (GDPR & Security)
* **Unauthenticated API Exposure (`/api/users`, `/api/reservations`)**
    * **Description:** The API endpoints used to fetch user data and reservation details are accessible without authentication.
    * **Impact:** Any guest can retrieve all user emails, session tokens, and roles. This is a critical violation of GDPR (Privacy by Design and Default).
    * **Spec Violation:** 8, 9, 10.

#### Authorization Bypasses (IDOR)
* **Unauthorized Booking Modification (`/reservation?id=X`)**
    * **Description:** Registered users can change the `id` parameter in the URL to access the modification form of bookings they do not own.
    * **Impact:** Users can alter reservation times and details for other users.
    * **Spec Violation:** 3, 4.

* **Privilege Escalation & Unauthorized Deletion**
    * **Description:** By modifying the "Reserver" field in a stolen booking form, a Reserver can take ownership of another user's booking and delete it.
    * **Impact:** Users can delete data belonging to other users.
    * **Spec Violation:** 3, 4, 5.

#### Functionality & Specification Gaps
* **Missing User Management Interface (Admin)**
    * **Description:** The Administrator does not have a dedicated UI panel to manage users (delete reservers). It must be done via API manipulation.
    * **Spec Violation:** 5.

* **Missing Resource Management Interface (Admin)**
    * **Description:** The Administrator cannot delete resources through the web interface.
    * **Spec Violation:** 4.

* **Missing "Right to be Forgotten" (GDPR)**
    * **Description:** There is no functionality for a Reserver to delete their own account.
    * **Spec Violation:** 9.

## Summary of role capabilities

| Capability | Guest | Reserver | Admin |
| :--- | :--- | :--- | :--- |
| **View Resources (Public)** | Allowed | Allowed | Allowed |
| **View Booking Identities** | Forbidden | Allowed | Allowed |
| **Login / Register** | Allowed | Allowed | Allowed |
| **Book Resources** | Forbidden | Allowed | Allowed |
| **Modify Own Bookings** | Forbidden | Allowed | Allowed |
| **Modify/Delete Others' Bookings** | Forbidden | Vulnerable (IDOR) | Allowed |
| **Add/Modify Resources** | Forbidden | Allowed | Allowed |
| **Delete Resources/Users** | Forbidden | Forbidden | Vulnerable (API Only) |
| **Access API (`/api/users`)** | Vulnerable (No Auth)| Allowed | Allowed |

### Legend
* **Allowed:** Functionality works according to specifications.
* **Forbidden:** Functionality is properly blocked.
* **Vulnerable:** Functionality works, but violates security, GDPR, or spec requirements.
