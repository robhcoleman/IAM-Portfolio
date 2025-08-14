# 🔐 Okta + ServiceNow: SAML SSO Integration Lab

## 📘 Overview
This lab demonstrates how to configure **SAML-based Single Sign-On (SSO)** between **Okta** (as the Identity Provider) and **ServiceNow** (as the Service Provider) for secure, centralized authentication. It includes step-by-step configuration, troubleshooting guidance, and MFA integration to strengthen authentication before granting access. This setup is a common enterprise IAM integration that recruiters value because it highlights real-world skills in authentication, federation, and user provisioning.

---

## 🎯 Goals & Objectives
- Show proficiency in **Okta admin configuration** for SAML applications.
- Demonstrate the ability to integrate cloud services like **ServiceNow** with an enterprise IdP.
- Implement **Multi-Factor Authentication (MFA)** policies within the SSO flow.
- Troubleshoot common SP-initiated and IdP-initiated SAML login issues.
- Document integration steps with **clear visuals and test validation** for audit readiness.

By completing this lab, I’ve proven capability in:
- Configuring SAML SSO metadata between two enterprise systems.
- Mapping attributes and NameID formats for user identity resolution.
- Assigning users and testing both IdP-initiated and SP-initiated SSO flows.
- Extending security with MFA and **Just-in-Time (JIT) provisioning** in ServiceNow.


---

## 🧰 Tools & Platforms Used
- **Okta Admin Console**
- **ServiceNow Developer Instance**
- **SAML Tracer** (Browser Extension)
- **Postman** (for troubleshooting)
- **Google Chrome / Firefox**

---

## 🛠️ Configuration Steps

### ✅ Okta Setup
1. Created a new **SAML 2.0 app** integration in Okta.
2. Defined the following attributes:
   - **Single Sign On URL**: `https://<your-instance>.service-now.com/navpage.do`
   - **Audience URI (SP Entity ID)**: `https://<your-instance>.service-now.com`
3. Set up attribute statements for `user.email`, `user.firstName`, and `user.lastName`.
4. Assigned test users to the app.

### ✅ ServiceNow Setup
1. Enabled **SAML 2.0** in the ServiceNow admin portal.
2. Uploaded the **Okta metadata XML** to configure the IdP.
3. Enabled **SP-initiated login**.
4. Created an SSO login test user that matches Okta directory.

---

## 🔎 Troubleshooting
- Used **SAML Tracer** to inspect AuthnRequests and assertions.
- Validated NameID and attributes match ServiceNow’s expectations.
- Used **Postman** to simulate login flow for token-based debugging.

---

## 🖼️ Screenshots
📌## 📸 Screenshots

All related screenshots for this lab can be found here:  
[View Screenshots](./screenshots)

- Okta SAML app configuration
- ServiceNow metadata import
- SAML assertion response (from SAML Tracer)
- SP-initiated login success screen

---

## ✅ Outcome
- Successfully configured secure SSO between Okta and ServiceNow.
- Achieved centralized authentication and reduced password fatigue.
- Demonstrated ability to integrate third-party apps using federation protocols.

### 🔐 MFA Enforcement for ServiceNow SSO

- Enabled Okta Verify and SMS as MFA factors
- Created a sign-on policy to **require MFA before accessing ServiceNow**
- Verified flow with test user account in incognito session
- Screenshots and policy rule config available in `/screenshots/`

Outcome: MFA successfully enforced during SSO login, improving access security.

---

## 🧠 Key IAM Concepts Practiced
- SAML 2.0 Protocol
- Service Provider (SP) vs Identity Provider (IdP)
- Attribute Mapping
- SP-Initiated vs IdP-Initiated SSO
- Federation Metadata Exchange
- MFA Enforcement for ServiceNow SSO

---




## 📎 Related Labs
- [Conditional Access in Entra ID](../EntraID-ConditionalAccess/)
- [SailPoint Provisioning Workflows](../SailPoint-Provisioning/)

---

## 👨‍💻 Author
**Robert Coleman**  \\
[LinkedIn](https://www.linkedin.com/in/roberthcoleman/)  |  [GitHub](https://github.com/roberthcoleman)
