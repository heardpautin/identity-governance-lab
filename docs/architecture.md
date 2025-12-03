# IGA Architecture Overview

This document provides a conceptual view of how identity governance components interact in a typical organization. It follows a **framework → identity governance → cloud enforcement → audit** model.

---

## Architecture Flow (High-Level)

```
[Frameworks] 
     ↓
[Identity Governance]
     ↓
[Cloud Security Enforcement]
     ↓
[Audit & Evidence]
```

This model reflects modern identity-first, framework-led security and governance programs.

---

## Core Components

### **1. Authoritative Source**  
Stores identity attributes and employment status (HR system or equivalent).  
This is the starting point for Joiner / Mover / Leaver events.

### **2. Identity Repository**  
Central identity directory storing accounts, attributes, and role assignments.

### **3. Access Request / Approval Workflow**  
Controls how access is requested, approved, and tracked.  
Can be manual, semi-automated, or fully automated.

### **4. Governance Engine**  
Implements framework requirements through:
- Role modeling (RBAC)
- SoD rule evaluation
- Lifecycle policies
- Certifications and attestations

### **5. Provisioning Layer**  
Applies adds, changes, and removals in connected systems.  
May include:
- Direct connectors  
- API-based provisioning  
- Ticket-based provisioning  

### **6. Cloud Security Enforcement Layer**  
Applies identity decisions through:
- Roles and policies  
- Conditional access  
- Privilege boundaries  
- Logging and monitoring  

### **7. Audit Layer**  
Validates that governance controls are working by:
- Capturing logs and evidence  
- Storing certification results  
- Demonstrating policy and lifecycle compliance  

---

## Identity Lifecycle Coverage

- **Joiner** — Initial identity creation and baseline role assignment  
- **Mover** — Role changes triggered by job or department changes  
- **Leaver** — Disablement and access removal  
- **Certification Cycles** — Periodic access reviews  
- **Entitlement Reviews** — Ensures mappings and roles remain accurate  

---

This architecture reflects the structure that most modern IAM, GRC, and Cloud Security programs follow.
