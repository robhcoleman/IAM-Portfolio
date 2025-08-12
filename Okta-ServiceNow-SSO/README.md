# 🔐 Okta + ServiceNow: SAML SSO Integration Lab

## 📘 Overview
This lab demonstrates how to configure **SAML-based Single Sign-On (SSO)** between **Okta** (as the Identity Provider) and **ServiceNow** (as the Service Provider). This integration allows users to authenticate seamlessly through Okta when accessing ServiceNow.

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

---

## 🧠 Key IAM Concepts Practiced
- SAML 2.0 Protocol
- Service Provider (SP) vs Identity Provider (IdP)
- Attribute Mapping
- SP-Initiated vs IdP-Initiated SSO
- Federation Metadata Exchange

---

## 📎 Related Labs
- [Conditional Access in Entra ID](../EntraID-ConditionalAccess/)
- [SailPoint Provisioning Workflows](../SailPoint-Provisioning/)

---

## 👨‍💻 Author
**Robert Coleman**  \\
[LinkedIn](https://www.linkedin.com/in/roberthcoleman/)  |  [GitHub](https://github.com/roberthcoleman)
