# Identity Governance Overview — How Frameworks, Identity, and Cloud Security Work Together

Modern security begins with **frameworks**, is implemented through **identity governance**, and is enforced through **cloud and application controls**.  
This document explains how these components form one unified, identity-first security ecosystem.

---

## 1. Frameworks Come First  
Before access governance can exist, an organization must define *what “good security” means* through frameworks such as:

- NIST 800-53  
- ISO 27001  
- CIS Controls  
- SOX  
- Zero Trust principles  

These frameworks define:

- Least privilege  
- Separation of Duties (SoD)  
- Access lifecycle requirements  
- Logging and audit expectations  
- Review and certification frequency  

Frameworks set the **rules**.  
Everything else flows from these requirements.

---

## 2. Identity Governance Implements the Framework  
Once the rules exist, **Identity Governance & Administration (IGA)** operationalizes them by defining:

- Who should have access (RBAC)  
- When access should change (JML lifecycle)  
- How access is reviewed (certifications)  
- What must be approved (entitlement workflows)  
- How exceptions are handled (SoD workflows)  

In other words:

**Frameworks define the “what.”  
Identity governance defines the “how.”**

This lab demonstrates governance in action through:

- **RBAC folder** → role and entitlement design  
- **Lifecycle folder** → joiner / mover / leaver workflows  
- **Certifications folder** → access reviews and attestation  
- **Audit folder** → control evidence  

Identity governance becomes the engine that applies and enforces the framework.

---

## 3. Cloud Security Enforces Identity Decisions  
Cloud platforms (Azure, AWS, GCP) enforce governance rules using:

- Role-based access  
- Policy-based permissions  
- Conditional access  
- Privilege boundaries  
- Logging and monitoring  
- Automated provisioning/deprovisioning  

Cloud Security is not separate — it is the **execution layer** for identity governance and frameworks.

---

## 4. Audit Validates the Entire System  
Audit ensures that:

- Controls are designed correctly  
- Identity governance processes are followed  
- Access reviews are performed  
- Deprovisioning is timely and complete  
- Exceptions are documented and justified  

Audit is how organizations **prove** they comply with the frameworks and operate securely.

---

## 5. How It All Comes Together  

### **1. Frameworks define the rules**  
(least privilege, SoD, certification cycles, evidence requirements)

### **2. Identity Governance implements the rules**  
(RBAC, JML workflows, certifications, entitlement mapping)

### **3. Cloud Security enforces the rules**  
(permissions, access policies, logs, automated controls)

### **4. Audit validates the rules**  
(evidence, logs, review outcomes, SoD exceptions)

This end-to-end chain reflects the real structure of IAM, GRC, and Cloud Security in modern organizations — including the model described by the Bexar County hiring manager.

## 📊 Visual Diagram — Framework → Identity → Cloud → Audit

```
+-------------------+
|   FRAMEWORKS      |
| (NIST, ISO, CIS)  |
+---------+---------+
          |
          v
+-------------------+
|  IDENTITY         |
|  GOVERNANCE (IGA) |
|  RBAC, JML, SoD   |
+---------+---------+
          |
          v
+-------------------+
|   CLOUD SECURITY  |
|  Enforcement Layer|
|  Roles, Policies  |
+---------+---------+
          |
          v
+-------------------+
|       AUDIT       |
| Evidence, Logs,   |
| Certifications    |
+-------------------+
```

Frameworks define the rules →  
Identity governance implements them →  
Cloud platforms enforce them →  
Audit validates everything.

---

## 6. Purpose of This Lab  
This project is designed to demonstrate:

- Understanding of framework-driven security  
- Application of identity governance principles  
- How RBAC and JML express compliance requirements  
- How cloud controls enforce governance decisions  
- How audit ties the entire model together  

This is the foundation of a modern identity-first, framework-led security program.
