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

* Can access login form — `/login` (spec 2)
* Can access registration form — `/register` (spec 2)
* Can access booked ressources (spec 8)
* Can access API endpoints without authentication, were the guest can see token, username and role — `/api/users`, `/api/reservations`, `/api/resources` ⚠️ (does **not** match any spec, spec 8 & 9 not respected)  

**❌ Cannot do**

* Cannot access reservation page — `/reservation` (redirect to login; spec 3)
* Cannot add reservation — `/reservation` (redirect to login; spec 3)
* Cannot update or delete reservations
* Cannot delete users
* Cannot update or delete ressources
---

### 🧑‍💼 **Reserver**

---

**✅ Can do**

* Can do what a guest can do
* Can book a reservation — `/reservation` (spec 6 & 7)  
* Can add ressources — `/resources` 
* Can access API endpoints `/api/users` and `/api/resources` (spec 3 & 8)
* Can update the username reserver on its own reservation ⚠️ (does **not** match any spec)
* Can update ressources 

**❌ Cannot do**

* Cannot register if under 15 years old (spec 6)
* Cannot modify resources (admin only; spec 4)
* Cannot delete reservations from other username (admin only; spec 3)  


---

### 🧑‍💼🛡️ **Administrator**

---

**✅ Can do**

* Can do all of the rights of reserver and guest
* Can delete reservation
* Can change reserver username
* Can update all reservations
* Can delete all reservations
* Can change ressources 
* Can add a resource — `/ressources` (spec 4)
* Can access API endpoints `/api/users`, `/api/reservations`, `/api/resources` (spec 4, & 8)  
* Can manage all reservations — `/reservations` (spec 4)  

**❌ Cannot do**

* Cannot delete reserver ⚠️ (does **not** match spec 5)
* Cannot delete ressources ⚠️ (does **not** match spec 4)


---
