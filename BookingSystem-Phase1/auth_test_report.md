# 🔐 **Authorization Test**

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

### 🧑‍🦲 **Guest**

---

**✅ Can do**

* Can view public resource list — `/resources` (spec 8)  
* Can access login form — `/login` (spec 2)  
* Can access registration form — `/register` (spec 2)  
* Can view robots.txt — `/robots.txt` (spec 1)  
* Can view sitemap — `/sitemap.xml` (spec 1)  
* Can access API endpoints without authentication — `/api/users`, `/api/reservations`, `/api/resources` ⚠️ (does **not** match any spec; backend access control missing, potential GDPR issue spec 9 & 10)  

**❌ Cannot do**

* Cannot access reservation page — `/reservation` (redirect to login; spec 3)  
* Cannot POST `/api/reservations` (spec 3 & 6)  
* Cannot access `/profile` (spec 3)  
* Cannot access any `/admin/*` pages (spec 4 & 5)  

---

### 🧑‍💼 **Reserver**

---

**✅ Can do**

* Can book a resource — `/reservation` + `/api/reservations` (spec 6 & 7)  
* Can view own profile page — `/profile` (spec 3)  
* Can list resources — `/resources` (spec 8)  
* Can access API endpoints `/api/users` and `/api/resources` (spec 3 & 8)  

**❌ Cannot do**

* Cannot access admin user list — `/admin/users` (spec 4 & 5)  
* Cannot delete other users — `/api/admin/users/:id` (spec 5)  
* Cannot access hidden admin pages even if URL manually typed — `/admin/*` (spec 4 & 5)  
* Cannot modify resources (admin only; spec 4)  

---

### 🧑‍💼🛡️ **Administrator**

---

**✅ Can do**

* Can add a resource — `/admin/resources/new` (spec 4)  
* Can delete a reserver — `/admin/users/delete/:id` (spec 5)  
* Can manage all reservations — `/admin/reservations` (spec 4)  
* Can view all users — `/admin/users` (spec 4 & 5)  
* Can access API endpoints `/api/users`, `/api/reservations`, `/api/resources` (spec 4, 5 & 8)  

**❌ Cannot do**

* Cannot perform actions blocked by UI even if API exists — none observed (no conflicting spec)  

---
