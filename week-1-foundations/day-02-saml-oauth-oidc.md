# Day 02 – SAML vs OAuth 2.0 vs OpenID Connect (OIDC)

## 🎯 Objective
Understand modern authentication and authorization protocols used in enterprise IAM systems and cloud environments.

---

# 🔐 1️⃣ SAML (Security Assertion Markup Language)

## What It Is
An XML-based authentication protocol primarily used for enterprise Single Sign-On (SSO).

## Core Purpose
Authentication (AuthN)

## How It Works (High-Level Flow)

User → Service Provider (App)  
→ Redirect to Identity Provider (IdP)  
→ User Authenticates  
→ IdP sends SAML Assertion (XML)  
→ User gains access

## Key Characteristics
- XML-based
- Browser redirect-based
- Common in enterprise environments
- Often used with ADFS, Azure AD

## Enterprise Example
Corporate employee logs into HR system using company SSO.

---

# 🔑 2️⃣ OAuth 2.0

## What It Is
An authorization framework that allows third-party applications to access resources on behalf of a user.

## Core Purpose
Authorization (AuthZ)

## Example Scenario
“Login with Google” allowing an app to access your profile data.

## How It Works

User → App requests permission  
→ Redirect to Authorization Server  
→ User consents  
→ Access Token issued  
→ App accesses resource

## Key Characteristics
- Token-based
- API-friendly
- Used heavily in microservices
- Access tokens + refresh tokens

## Important Note
OAuth does NOT authenticate users.  
It only authorizes access to resources.

---

# 👤 3️⃣ OpenID Connect (OIDC)

## What It Is
An authentication layer built on top of OAuth 2.0.

## Core Purpose
Authentication (AuthN)

## How It Works

OAuth Flow + ID Token (JWT)

User → Authorization Server  
→ Access Token + ID Token issued  
→ ID Token confirms user identity

## Key Characteristics
- JSON-based
- Uses JWT
- Modern cloud-friendly protocol
- Replaces SAML in many cloud-native apps

---

# 📊 Comparison Table

| Feature | SAML | OAuth 2.0 | OIDC |
|----------|------|-----------|------|
| Primary Purpose | Authentication | Authorization | Authentication |
| Format | XML | JSON / Tokens | JSON (JWT) |
| Used For | Enterprise SSO | API access | Modern SSO |
| Token Type | SAML Assertion | Access Token | ID Token + Access Token |
| Mobile Friendly | Less | Yes | Yes |

---

# 🏗 Where They Fit in Architecture

Enterprise App (Legacy) → Often SAML  
API / Microservices → OAuth  
Modern Web / Cloud App → OIDC  

---

# 🧠 TPM-Level Insight

- SAML is older, XML-heavy, enterprise-focused.
- OAuth is authorization-only.
- OIDC solves authentication in modern cloud systems.
- Most cloud IAM today uses OIDC instead of SAML.

In interviews, clarify:
> OAuth authorizes access. OIDC authenticates users.

---

# 🔥 Real-World IAM Context

### In PAM
- CyberArk Privilege Cloud may use SAML/OIDC for SSO integration.

### In IGA
- Saviynt integrates with apps using SAML or OIDC connectors.

### In Cloud
- Azure AD supports both SAML and OIDC.
- AWS Cognito primarily uses OIDC.

---

# ⚠️ Common Interview Traps

- Saying OAuth is authentication (it is NOT).
- Confusing ID token with access token.
- Not understanding redirect-based login flow.

---

# 📝 Self-Test

1. Why is OAuth not authentication?
2. What is inside a SAML assertion?
3. What is the difference between ID token and access token?
4. When would you choose SAML over OIDC?
5. Why is OIDC more cloud-friendly?

---

## 📌 Personal Reflection Section

### What I Learned Today
(Write in your own words)

### What Is Still Confusing
(Add questions for deeper research)

---

**Status:** Not Started  
**Time Spent:** 30 Minutes  
