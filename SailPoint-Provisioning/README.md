# 🛡 SailPoint IdentityNow IAM Labs – Create Campaign & Create Roles & 


## 📘 Overview
This project showcases two real-world SailPoint IdentityNow administrator functions — **Access Certification Campaigns** and **Role Creation (Standard & Dynamic)** — that are critical for identity governance and compliance. These labs demonstrate the ability to configure review workflows, implement role-based access control, and apply attribute-based automation to streamline provisioning. The documentation, screenshots, and diagrams simulate tasks an IAM Administrator or IGA Engineer would perform in a production environment.

---

## 🎯 Goals & Objectives
These labs were designed to:
- Demonstrate **hands-on SailPoint configuration skills** that directly align with IAM admin job descriptions.
- Build **compliance-ready workflows** through campaigns that ensure users maintain only the access they need.
- Show proficiency in **static and dynamic role management**, including the use of user attributes for automated membership updates.
- Highlight the ability to translate **business requirements into IAM policies** that reduce manual effort and support audit readiness.

By completing these labs, I’ve proven capability in:
- Launching targeted access reviews with manager-driven certifications.
- Creating and managing **Standard Roles** for fixed membership scenarios.
- Designing **Dynamic Roles** that update automatically when user attributes change.
- Assigning entitlements and access profiles to streamline onboarding and de-provisioning.

---

## 🧰 Tools & Platforms Used
- SailPoint IdentityNow Admin Console (Sandbox or Production)
- Connected Applications with available entitlements
- Authoritative source data (e.g., HR system feed)
- Test user accounts

---

---

# 1️⃣ Create Campaign Lab

### **Step 1 – Navigate to Campaigns**
1. Log in to **SailPoint IdentityNow**
2. Go to:
3. Click **Create Campaign**

---

### **Step 2 – Select Campaign Type**
- Choose **Manager Certification** → Reviewers will be each user’s direct manager

---

### **Step 3 – Configure Campaign Details**
- **Name**: `Q3 Manager Access Review`
- **Description**: Quarterly review of user access rights
- **Campaign Owner**: Your admin/test account
- **Start Date**: Today
- **End Date**: 14 days from start

---

### **Step 4 – Scope the Review**
- **Applications**: Select 2–3 connected apps
- **Entitlements**: All within selected apps
- **Users**: Filter by department = `Sales`

---

### **Step 5 – Assign Reviewers**
- Automatically assign **each user's manager** as the reviewer
- Backup reviewer for users without a manager

---

### **Step 6 – Configure Notifications**
- Campaign start, reminder, and due date alerts
- Escalation to campaign owner

---

### **Step 7 – Launch Campaign**
- Review configuration and click **Start Campaign**
- Verify reviewer notification emails

---

📸 **Screenshots for Create Campaign**:  
`/SailPoint-Labs/screenshots/campaign/`

---

# 2️⃣ Create Roles Lab (Standard & Dynamic)

### **Standard Role (Static Membership)**
**Step A – Define Role Details**
- **Name**: `Test Role MD`
- **Role Type**: Standard

**Step B – Add Members Manually**
- Select specific identities

**Step C – Assign Access Profiles**
- Example: SAP Finance Module, Finance Shared Drive

**Step D – Save Role**

---

### **Dynamic Role (Attribute-Based Membership)**
**Step A – Define Role Details**
- **Name**: `Test Role MD Dynamic`
- **Role Type**: Dynamic

**Step B – Build Membership Criteria**


**Step C – Assign Access Profiles**
- Example: Salesforce CRM, Sales Analytics Dashboard

**Step D – Save Role**

---

📸 **Screenshots for Create Roles**:  
`/SailPoint-Labs/screenshots/roles/`

---

## 🧪 Testing & Validation
- For **Campaign**: Verify reviewers can approve/revoke access
- For **Standard Role**: Assign manually and confirm provisioning
- For **Dynamic Role**: Update user attributes and verify auto-provisioning/de-provisioning

---

## ✅ Outcome
By completing these labs, you have demonstrated:
- Proficiency in **Access Certification Campaign creation**
- Expertise in **Role-Based Access Control** using both static and dynamic memberships
- Understanding of automation in identity governance

---

## 🧠 Key IAM Concepts Practiced
- Access Reviews & Certifications
- Governance & Compliance
- Static vs. Dynamic Role Management
- Attribute-Based Access Control (ABAC)
- Automated Provisioning & De-Provisioning

---

## 📎 Related Labs
- [Entra ID Conditional Access](../EntraID-ConditionalAccess/)
- [Okta + ServiceNow SAML SSO](../Okta-ServiceNow-SSO/)

---

## 👨‍💻 Author
**Robert Coleman**  
[LinkedIn](https://www.linkedin.com/in/roberthcoleman/) | [GitHub](https://github.com/roberthcoleman)


## 📎 Related Labs
- [Okta + ServiceNow SAML SSO](../Okta-ServiceNow-SSO/)
- [Entra ID Conditional Access Policies](../EntraID-ConditionalAccess/)



## 👨‍💻 Author
**Robert Coleman**  \\
[LinkedIn](https://www.linkedin.com/in/roberthcoleman/)  |  [GitHub](https://github.com/roberthcoleman)
