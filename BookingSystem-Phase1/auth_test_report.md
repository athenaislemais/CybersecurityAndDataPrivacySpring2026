# 🔐 **Authorization Test**

---

### 🧑‍🦲 **Guest**

---

**✅ Can do**

* Can view public resource list — `/resources` (accessible via API and web UI; matches spec)  
* Can access login form — `/login` (matches spec)  
* Can access registration form — `/register` (matches spec)  
* Can view robots.txt — `/robots.txt` (matches spec)  
* Can view sitemap — `/sitemap.xml` (matches spec)  
* Can access API endpoints without authentication — `/api/users`, `/api/reservations`, `/api/resources` (does **not** match spec; backend access control missing) ⚠️  

**❌ Cannot do**

* Cannot access reservation page — `/reservation` (redirect to login; matches spec)  
* Cannot POST `/api/reservations` (blocked; matches spec)  
* Cannot access `/profile` (matches spec)  
* Cannot access any `/admin/*` pages (matches spec)  

---

### 🧑‍💼 **Reserver**

---

**✅ Can do**

* Can book a resource — `/reservation` + `/api/reservations` (matches spec)  
* Can view own profile page — `/profile` (matches spec)  
* Can list resources — `/resources` (matches spec)  
* Can access API endpoints `/api/users` and `/api/resources` (matches spec)  

**❌ Cannot do**

* Cannot access admin user list — `/admin/users` (matches spec)  
* Cannot delete other users — `/api/admin/users/:id` (matches spec)  
* Cannot access hidden admin pages even if URL manually typed — `/admin/*` (matches spec)  
* Cannot modify resources (admin only; matches spec)  

---

### 🧑‍💼🛡️ **Administrator**

---

**✅ Can do**

* Can add a resource — `/admin/resources/new` (matches spec)  
* Can delete a reserver — `/admin/users/delete/:id` (matches spec)  
* Can manage all reservations — `/admin/reservations` (matches spec)  
* Can view all users — `/admin/users` (matches spec)  
* Can access API endpoints `/api/users`, `/api/reservations`, `/api/resources` (matches spec)  

**❌ Cannot do**

* Cannot perform actions blocked by UI even if API exists — none observed  
* ⚠️ SQL Injection vulnerability detected by ZAP on `/login`, `/register`, `/resources` (High risk; parameter `host`)  
* ⚠️ Format String issues detected by ZAP on `/status.html`, `/login`, `/register`, `/resources` (Medium risk)

---
