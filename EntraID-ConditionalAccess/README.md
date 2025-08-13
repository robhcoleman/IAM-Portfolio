# 🛡️ Entra ID: Conditional Access Policy Implementation Lab

## 📘 Overview
This lab focuses on implementing **Conditional Access policies** using **Microsoft Entra ID (formerly Azure Active Directory)**. The goal was to enforce contextual access controls based on user risk, location, device state, and app sensitivity.

---

## 🧰 Tools & Platforms Used
- **Microsoft Entra ID / Azure AD**
- **Microsoft 365 E5 Developer Tenant**
- **Azure Portal**
- **Test users & groups**
- **Microsoft Authenticator App**

---

## 🛠️ Configuration Steps

### ✅ Policy: Block Access from Non-Compliant Devices
1. Created a test group `Non-Compliant Devices Test`.
2. Created a Conditional Access policy targeting:
   - **Users**: Test group
   - **Cloud apps**: All cloud apps
   - **Conditions**: Device state set to “Not compliant”
   - **Access Control**: Block access
3. Tested access from a non-compliant VM – access denied as expected.

---

### ✅ Policy: Require MFA for Admin Roles
1. Scoped the policy to **Directory Roles** > Global Admins and Privileged Role Admins.
2. Conditions:
   - **Sign-in risk**: Medium and above
3. Access Control:
   - **Grant**: Require MFA
4. Verified prompt for MFA during risky logins using a secondary IP/location.

---

### ✅ Policy: Allow Access Only from U.S.
1. Created Named Location: "United States"
2. Applied policy to all users:
   - **Condition**: Location NOT in "United States"
   - **Control**: Block access
3. Verified successful login from U.S. IP, blocked access from VPN with non-U.S. IP.

---

## 🖼️ Screenshots
📌 All related screenshots for this Lab can be found here:
[View Screenshots](./screenshots)
- Policy creation wizard
- Named location config
- Sign-in logs with policy enforcement results

---

## ✅ Outcome
- Successfully created and tested **three distinct Conditional Access policies**.
- Demonstrated ability to enforce role-based, geo-based, and device-based access rules.
- Strengthened organizational identity perimeter and improved security posture.

---

## 🧠 Key IAM Concepts Practiced
- Role-Based Access Control (RBAC)
- Conditional Access Evaluation Flow
- Named Locations
- Device Compliance
- Sign-in Risk & Azure Identity Protection

---

## 📎 Related Labs
- [Okta + ServiceNow SAML SSO](../Okta-ServiceNow-SSO/)
- [SailPoint Provisioning Workflows](../SailPoint-Provisioning/)

---

## 👨‍💻 Author
**Robert Coleman**  \\
[LinkedIn](https://www.linkedin.com/in/roberthcoleman/)  |  [GitHub](https://github.com/roberthcoleman)
