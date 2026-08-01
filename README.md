AWS IAM Company Simulation Project

📌 Overview
This project simulates a real-world company IAM (Identity and Access Management) structure using AWS best practices. The goal was to design a secure and scalable access control system using least privilege and role-based access.



🏢 Company Structure Simulation

👥 Users Created
- admin → Full system control
- developer → Limited operational access
- intern → Read-only access

---

👨‍👩‍👧‍👦 Groups Created
- SecurityTeam → Administrative control
- DevTeam → Developer access
- Interns → Read-only access

---

🔑 Access Control Strategy

Permissions were assigned using **IAM groups instead of directly to users**.

Why this matters:
- Easier to manage multiple users
- Follows AWS best practices
- Reduces human error

---

🛡️ Permissions Design

| Role       | Access Level    | Policy Used            |
|------------|----------------|------------------------|
| Admin      | Full Access     | AdministratorAccess    |
| Developer  | Limited Access  | PowerUserAccess *(or EC2 + S3 custom policy)* |
| Intern     | Read-Only       | ReadOnlyAccess         |

---

🔒 Security Implementation

✅ Multi-Factor Authentication (MFA)
MFA was enabled for all users to improve account security.

✅ Least Privilege Principle
- Intern → cannot modify resources  
- Developer → cannot manage IAM  
- Admin → full access  

---

🚫 Direct Permissions Removed

All direct user permissions were removed.

Reason:
To ensure clean, scalable, and secure permission management using groups only.

---

📸 Project Evidence

Screenshots included:
- IAM Users
- IAM Groups
- Permissions attached via groups
- MFA enabled

---

📚 Key Learnings

- IAM user and group management
- Role-based access control
- Security best practices in AWS
- Importance of least privilege

---

🚀 Conclusion

This project demonstrates hands-on AWS IAM skills and reflects real-world cloud security practices used in production environments.
