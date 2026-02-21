# Day 01 – Authentication vs Authorization

## 🎯 Objective
Understand the foundational difference between authentication and authorization in enterprise IAM systems.

---

## 🔐 Authentication (AuthN)

**Definition:** Proving identity.

> Question answered: *Who are you?*

Authentication verifies that a user or system is genuinely who they claim to be.

### Examples
- Username & Password
- MFA (OTP, Push Notification)
- Biometrics
- Smart Cards
- Certificates

### Key Characteristics
- Happens first
- Establishes identity
- Creates session or token

---

## 🛡 Authorization (AuthZ)

**Definition:** Granting permission.

> Question answered: *What are you allowed to do?*

Authorization determines what an authenticated user can access.

### Examples
- Read vs Write access
- Admin vs User role
- API access scopes
- Database table permissions

### Key Characteristics
- Happens after authentication
- Based on roles or policies
- Enforces least privilege

---

## 🔄 Enterprise IAM Flow

User → Authentication → Token Issued → Authorization Check → Resource Access

Example in Identity Architecture:

HR → IGA → AD → Application  
User Login → IdP Authentication → Policy Engine Authorization

---

## 🏗 Practical Enterprise Examples

### PAM Example
- Authentication: Admin logs into vault using MFA
- Authorization: Vault policy determines which privileged accounts can be accessed

### IGA Example
- Authentication: User logs into portal
- Authorization: Assigned role determines accessible applications

---

## 📊 Comparison Table

| Area | Authentication | Authorization |
|------|---------------|--------------|
| Core Question | Who are you? | What can you do? |
| Order | First | After AuthN |
| Based On | Credentials | Policies / Roles |
| Risk if Failed | No Access | Over-privileged access |

---

## 🧠 Advanced Concepts

Authentication mechanisms:
- Password-based
- Certificate-based
- Token-based (JWT, SAML)

Authorization models:
- RBAC
- ABAC
- Policy engines
- SoD enforcement

---

## ⚠️ Common Interview Traps

- Authentication and authorization are NOT the same.
- Authorization cannot happen without authentication.
- MFA improves authentication strength, not authorization logic.

---

## 🏆 TPM-Level Insight

Authentication establishes identity.  
Authorization enforces business policy.

A secure architecture separates both to maintain least privilege and reduce risk.

---

## 📝 Self-Test

1. Why must authentication occur before authorization?
2. How does MFA improve authentication?
3. Where does authorization logic live in PAM?
4. Can a system authenticate without authorizing?

---

## 📌 Personal Reflection Section

### What I Learned Today
(Write in your own words)

### What Is Still Confusing
(Add questions for deeper research)

---
**Status:** Not Started
**Time Spent:** 30 Minutes  
