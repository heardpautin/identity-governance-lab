# Architecture Summary (Short Version)

This lab models how identity governance functions within real-world security programs.  
Frameworks define the control requirements → governance models RBAC, JML, SoD, and certifications → the access enforcement layer applies permissions using directory groups, IAM policies, and identity protocols like LDAP, Kerberos, SAML, OIDC, OAuth, and SCIM → audit validates decisions and evidence.  


The guiding philosophy is

[Frameworks & Controls] 
         ↓
[Identity Governance Layer]
         ↓
[Access Enforcement Layer]
         ↓
[Audit & Evidence Layer]



This structure reflects modern identity-first security across on-prem, cloud, and hybrid environments.

---

# High-Level Architecture Flow

# 1. Frameworks & Controls (The “Why”)

Security and compliance frameworks define expectations such as:

- Least privilege  
- Separation of Duties (SoD)  
- Strong authentication  
- Timely provisioning & deprovisioning  
- Periodic access reviews  
- Auditability & traceability  

Common frameworks:
- ISO 27001 A.9 / A.5  
- NIST SP 800-53 (AC family)  
- SOC 2 CC6.x  
- CIS Controls v8  

Governance exists to **implement these rules in identity systems**.

---

# 2. Identity Governance Layer (The “What”)

Governance determines **who should have access** and **why** by modeling:

- Business roles and entitlements  
- Technical privileges  
- Joiner / Mover / Leaver workflows  
- Access certifications and attestations  
- SoD rules and exception handling  

This layer produces **access decisions**, not technical enforcement.

---

# 3. Access Enforcement Layer (The “How”)

This layer implements governance decisions at the technical level across:

- On-prem directories  
- Cloud identity providers  
- SaaS platforms  
- Applications  
- Databases  
- Networks  
- Operating systems  

Below are the core enforcement technologies mapped by environment.

---

# Underlying Technologies That Enable Enforcement  
### (Mapped: On-Prem vs Cloud vs SaaS vs API vs Network)

---

## 🔵 On-Prem / Legacy Identity Protocols

| Technology | Purpose | Typical Use |
|-----------|---------|-------------|
| **LDAP** | Directory queries | Legacy apps, Unix/Linux systems |
| **Kerberos** | Ticket-based authentication | Windows AD, internal SSO |
| **NTLM** | Legacy authentication fallback | Older Windows environments |
| **RADIUS** | Network authentication | VPN, Wi-Fi |
| **TACACS+** | Administrative command authorization | Routers, switches, firewalls |

---

## 🟣 Cloud & Modern Identity Protocols

| Technology | Purpose | Common Use |
|-----------|---------|-------------|
| **OIDC (OpenID Connect)** | Modern authentication | SaaS login, cloud-native apps |
| **OAuth 2.0** | Delegated authorization | API permissions, cloud access |
| **JWT** | Token carrying identity claims | Zero Trust, microservices |
| **SCIM** | Automated provisioning | SaaS lifecycle management |

---

## 🟡 SaaS & Federated Identity Protocols

| Technology | Purpose | Use Cases |
|-----------|---------|-----------|
| **SAML 2.0** | Federated authentication | Enterprise SSO |
| **WS-Fed** | Legacy federation | Older Microsoft systems |
| **Just-in-Time (JIT) Provisioning** | User creation at login | SAML/OIDC SaaS applications |

---

## 🟢 Universal Access Control Mechanisms

| Mechanism | Purpose | Environment |
|-----------|---------|-------------|
| **Directory Groups (AD/LDAP)** | Authorization | On-prem + hybrid |
| **IAM Policies** | Resource-level permissions | Cloud |
| **Application RBAC** | In-app permissions | SaaS + legacy |
| **Conditional Access** | Risk-based enforcement | Cloud, Zero Trust |
| **MFA / Step-up Authentication** | Identity assurance | All environments |
| **NTFS/POSIX ACLs** | File security | On-prem servers |
| **Database Roles** | Data access security | Cloud + on-prem DBs |

---

# 4. Audit & Evidence Layer

Audit verifies that:

- Governance decisions align with frameworks  
- Enforcement applied decisions correctly  
- JML lifecycle actions were timely  
- Certifications were completed  
- SoD violations and exceptions were documented  
- Termination access was fully removed  

Audit artifacts include:

- JML logs  
- Access certification evidence  
- SoD violation and exception records  
- Attestation logs  
- Access change logs  
- Retention policy documentation  

Audit closes the loop:

**Framework → Governance → Enforcement → Audit**

---

# Identity Lifecycle Coverage

- **Joiner** — Create identity; assign baseline access  
- **Mover** — Update access; remove outdated entitlements  
- **Leaver** — Disable identity; revoke all access  
- **Certification Cycles** — Revalidate privileges periodically  
- **Entitlement Reviews** — Maintain role hygiene  
- **SoD Evaluation & Exceptions** — Prevent toxic access combinations  
