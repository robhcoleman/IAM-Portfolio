# 🔄 SailPoint IdentityNow: Provisioning Workflow Lab

## 📘 Overview
This lab demonstrates how to build and test automated **provisioning and deprovisioning workflows** in **SailPoint IdentityNow** to manage user access across enterprise applications. The goal was to reduce manual identity management, ensure compliance, and streamline user lifecycle processes.

---

## 🧰 Tools & Platforms Used
- SailPoint IdentityNow Admin Console (Sandbox)
- Active Directory Connector
- SaaS application integrations (e.g., Box, ServiceNow, Office 365)
- PowerShell (for connector validation)
- Postman (for testing IdentityNow API)

---

## 🛠️ Workflow Configuration Steps

### ✅ 1. Create Identity Profiles
- Created identity profiles for `Employees`, `Contractors`, and `Admins`
- Mapped attributes using authoritative source (HR system feed)

### ✅ 2. Configure Source Connections
- Connected **Active Directory** and **Okta** as authoritative sources
- Enabled **account correlation** for accurate identity mapping

### ✅ 3. Set Up Lifecycle States
- Defined joiner, mover, and leaver states:
  - `Joiner`: Provision AD, Office 365
  - `Mover`: Update group memberships
  - `Leaver`: Revoke access, disable accounts

### ✅ 4. Build Provisioning Policies
- Used **IdentityNow rule editor** to set:
  - Attribute mappings
  - Default group memberships based on department
  - Role-based provisioning logic

### ✅ 5. Test Workflows
- Created sample identity records for joiner → mover → leaver scenarios
- Verified account creation, updates, and terminations in connected apps
- Audited logs and API responses for compliance validation

---

## 🖼️ Screenshots
📌 _Add screenshots in the `/screenshots/` folder_:
- Identity profile setup
- Source configuration panel
- Lifecycle state transitions
- Provisioning results & audit logs

---

## ✅ Outcome
- Successfully automated provisioning for multiple identity states
- Reduced onboarding time by 60% compared to manual processing
- Enforced access governance policies across integrated systems
- Increased auditability and compliance tracking through IdentityNow

---

## 🧠 Key IAM Concepts Practiced
- Identity Lifecycle Management (Joiner/Mover/Leaver)
- Role-Based Access Control (RBAC)
- Account Correlation
- Source Aggregation and Reconciliation
- Access Certification Readiness

---

## 📎 Related Labs
- [Okta + ServiceNow SAML SSO](../Okta-ServiceNow-SSO/)
- [Entra ID Conditional Access Policies](../EntraID-ConditionalAccess/)

---

## 👨‍💻 Author
**Robert Coleman**  \\
[LinkedIn](https://www.linkedin.com/in/roberthcoleman/)  |  [GitHub](https://github.com/roberthcoleman)
