# 🔐 Identity & Access Management (IAM) — Key Takeaways

> A personal study repository and reference guide for IAM concepts, responsibilities, tools, and career progression.

## 📦 Portfolio
- IAM Portfolio Link (https://sunanda-thompson.github.io/IAM/iam-portfolio.html#) 

---

## 📌 Table of Contents

- [What is IAM?](#what-is-iam)
- [The Four A's of IAM](#the-four-as-of-iam)
- [Core Principles](#core-principles)
- [IAM Analyst Responsibilities](#iam-analyst-responsibilities)
- [Technical Skills](#technical-skills)
- [Tools & Platforms](#tools--platforms)
- [Protocols & Standards](#protocols--standards)
- [Access Control Models](#access-control-models)
- [Identity Lifecycle: Joiner / Mover / Leaver](#identity-lifecycle-joiner--mover--leaver)
- [Access Certification Best Practices](#access-certification-best-practices)
- [Separation of Duties (SoD)](#separation-of-duties-sod)
- [Certifications Roadmap](#certifications-roadmap)
- [Career Progression](#career-progression)
- [Common IAM Challenges](#common-iam-challenges)
- [Learning Resources](#learning-resources)

---

## What is IAM?

**Identity and Access Management (IAM)** is the framework of policies, processes, and technologies that ensures the **right people have the right access to the right resources at the right time.**

IAM sits at the intersection of **security**, **compliance**, and **IT operations** — and is considered the **new security perimeter** in modern enterprise environments.

---

## The Four A's of IAM

| Concept | Description |
|---------|-------------|
| Authentication | Verifying *who you are* (passwords, MFA, biometrics) |
| Authorization | Determining *what you can access* |
| Administration | Managing identities, roles, and permissions |
| Audit | Tracking and reviewing all access and activity |

---

## Core Principles

| Principle | Summary |
|-----------|---------|
| **Least Privilege** | Grant only the minimum access required to do a job — nothing more |
| **Separation of Duties** | Split critical tasks across multiple people to prevent fraud |
| **Zero Trust** | Never trust, always verify — even internal users must be authenticated |
| **Identity Lifecycle** | Manage identities from creation (hire) to destruction (termination) |
| **Accountability** | All access actions must be traceable to an individual identity |

---

## IAM Analyst Responsibilities

### 🔑 Access Management
- Provision new accounts and grant initial access
- Modify access during role changes or transfers
- De-provision all access upon termination
- Process access requests via ticketing systems
- Manage emergency/break-glass accounts

### 📋 Access Reviews & Certifications
- Run periodic access certification campaigns
- Coordinate manager and data owner attestation
- Follow up on uncertified or over-privileged access
- Remediate and document all review outcomes

### 🔄 Identity Lifecycle Management
- Onboard new hires with correct day-one access
- Handle internal transfers (remove old, grant new)
- Offboard departing employees — disable all accounts
- Manage contractors, vendors, and service accounts

### 🏛️ Compliance & Audit Support
- Identify and resolve SoD conflicts
- Provide evidence for internal and external audits
- Ensure access aligns with regulatory requirements
- Maintain accurate and up-to-date documentation

### 🛠️ Troubleshooting & Support
- Resolve login problems and access denials
- Assist with MFA and password reset issues
- Investigate access anomalies and escalations
- Collaborate with IT teams on complex issues

### 📊 Reporting & Metrics
- Report on who has access to what
- Track certification completion rates
- Monitor for orphaned and dormant accounts
- Provide executive-level IAM health dashboards

---

## Technical Skills

### Must-Know Concepts
- Multi-Factor Authentication (MFA / 2FA)
- Single Sign-On (SSO)
- Privileged Access Management (PAM)
- Active Directory (AD) structure and management
- Group Policy basics
- Certificate Management / PKI basics
- SCIM provisioning
- API basics (REST, JSON, XML)

### Scripting & Automation
- **PowerShell** — primary tool for Windows/AD automation
- **Python** — cross-platform scripting, reporting, API interaction
- **Bash** — Linux automation
- **SQL** — database queries and IAM reporting
- **Git** — version control for scripts and configs

---

## Tools & Platforms

### Identity Governance & Administration (IGA)
| Tool | Vendor |
|------|--------|
| IdentityIQ / IdentityNow | SailPoint |
| Saviynt | Saviynt |
| Oracle Identity Governance | Oracle |
| Identity Manager | One Identity |
| IBM Security ISIM | IBM |

### Access Management / SSO
| Tool | Vendor |
|------|--------|
| Okta | Okta |
| Azure AD / Entra ID | Microsoft |
| Ping Identity | Ping |
| ForgeRock | ForgeRock |
| Auth0 | Okta |

### Privileged Access Management (PAM)
| Tool | Vendor |
|------|--------|
| CyberArk | CyberArk |
| BeyondTrust | BeyondTrust |
| Delinea (Thycotic) | Delinea |
| HashiCorp Vault | HashiCorp |

### Directory Services
- **Active Directory (AD)** — Microsoft on-prem standard
- **Azure AD / Entra ID** — Cloud identity
- **LDAP** — Protocol underlying most directory services

### Supporting Tools
- **ServiceNow / Jira** — Ticketing and access request workflows
- **Excel / Power BI / Tableau** — Reporting and analytics
- **Confluence / SharePoint** — Documentation
- **Postman** — API testing

---

## Protocols & Standards

| Protocol / Standard | Purpose |
|--------------------|---------|
| **SAML 2.0** | XML-based SSO and federated identity |
| **OAuth 2.0** | Delegated authorization framework |
| **OpenID Connect (OIDC)** | Identity layer on top of OAuth 2.0 |
| **SCIM** | Automated user provisioning across systems |
| **LDAP** | Directory access and queries |
| **Kerberos** | Windows/AD authentication protocol |
| **RADIUS** | Network access authentication |
| **FIDO2 / WebAuthn** | Passwordless authentication standard |

---

## Access Control Models

| Model | Acronym | How It Works |
|-------|---------|-------------|
| Role-Based Access Control | **RBAC** | Access granted based on job role |
| Attribute-Based Access Control | **ABAC** | Access based on user/resource attributes (e.g., department, location) |
| Mandatory Access Control | **MAC** | System enforces access; users cannot change it |
| Discretionary Access Control | **DAC** | Resource owners control who gets access |
| Rule-Based Access Control | **RuBAC** | Access determined by predefined rules/conditions |

> 💡 **Most enterprises use RBAC as the foundation**, supplemented with ABAC for more complex scenarios.

---

## Identity Lifecycle: Joiner / Mover / Leaver

```
[HIRE]                [TRANSFER]              [TERMINATE]
  │                       │                        │
  ▼                       ▼                        ▼
JOINER               MOVER                    LEAVER
──────               ──────                   ──────
Pre-provision        Remove old access        Disable ALL accounts
Role-based access    Add new role access      immediately
Day-one ready        Manager approval         Archive/delete data
MFA enrollment       Document exceptions      Final access cert
Welcome comms        Update directory         HR notification
```

### Key Rules
- ✅ Access should be **ready before day one**
- ✅ Old access must be **removed before new access is granted** during transfers
- ✅ Terminations require **same-day (or immediate) account disablement**
- ✅ All changes must leave an **audit trail**

---

## Access Certification Best Practices

| Practice | Details |
|----------|---------|
| **Frequency** | High-risk: quarterly / Standard: annually |
| **Ownership** | Managers attest to their team; data owners attest to app access |
| **Automation** | Auto-revoke access not certified within deadline |
| **Risk Scoring** | Prioritize review of high-risk or sensitive access first |
| **Escalation** | Auto-escalate non-responses to manager's manager |
| **Metrics** | Track completion rate, revocation rate, on-time rate |

---

## Separation of Duties (SoD)

**SoD** ensures no single person controls all steps of a critical process (e.g., create a vendor AND approve payment).

### SoD Lifecycle
```
DEFINE conflicts  →  PREVENT at provisioning  →  DETECT violations  →  REMEDIATE
```

### Handling SoD Exceptions
1. Require written business justification
2. Get risk owner sign-off
3. Set an expiration date
4. Add compensating controls (monitoring, approval)
5. Document and report regularly

---

## Certifications Roadmap

```
BEGINNER                  INTERMEDIATE               ADVANCED
──────────────────        ─────────────────          ─────────────────────
CompTIA Security+    →    SailPoint Certified    →   CISSP
                          Okta Certified Pro         CISM
                          Azure AD Associate         AWS Security Specialty
                          CompTIA CySA+              GIAC GSEC
```

### Recommended Starting Order
1. **CompTIA Security+** — Security fundamentals, widely recognized
2. **Vendor Cert** (Okta / SailPoint / Azure) — Based on target employer stack
3. **Cloud Security Cert** — As cloud IAM grows in importance
4. **CISSP or CISM** — After 3-5 years of experience

---

## Career Progression

```
Entry Level          Mid Level            Senior Level         Leadership
─────────────        ──────────────       ─────────────────    ──────────────────
IAM Analyst     →    Senior Analyst  →    IAM Engineer    →    IAM Architect
IAM Associate        IAM Admin            IAM Specialist        IAM Manager
                                                                IAM Director / CISO
0–2 years            2–5 years            5–8 years            8+ years
$50K–$70K            $70K–$95K            $95K–$130K           $130K–$200K+
```

### Lateral Moves from IAM
- Security Operations (SOC)
- Governance, Risk & Compliance (GRC)
- IT Audit
- Cloud Security Engineering
- Application Security

---

## Common IAM Challenges

| Challenge | Quick Solution |
|-----------|---------------|
| Users resisting access reviews | Simplify the process; automate reminders; get exec sponsorship |
| Over-privileged accounts | Implement Least Privilege; run regular certifications |
| Legacy systems not integrated | Manual controls + more frequent reviews as compensating control |
| Orphaned accounts after termination | Automate deprovisioning from HR feed |
| SoD violations | Define conflicts upfront; enforce preventive controls at provisioning |
| Too many exceptions | Formal exception process with expiry dates and exec sign-off |
| Shared/admin accounts | PAM tools + just-in-time access + eliminate sharing |

---

## Learning Resources

### Free Starting Points
- 🎓 [SailPoint University](https://university.sailpoint.com/) — Free IGA training
- 🎓 [Microsoft Learn – Entra ID](https://learn.microsoft.com/) — Free Azure AD modules
- 🎓 [Okta Developer Docs](https://developer.okta.com/) — Free dev account + tutorials
- 🎓 [SANS Cyber Aces](https://www.cyberaces.org/) — Free security fundamentals
- 🎓 [TryHackMe – AD Rooms](https://tryhackme.com/) — Hands-on AD and IAM labs

### Recommended Books
- *Identity and Access Management* — Ertem Osmanoglu
- *Zero Trust Networks* — Evan Gilman & Doug Barth
- *Security Engineering* — Ross Anderson

### Communities
- Reddit: `r/cybersecurity`, `r/netsec`, `r/AskNetsec`
- LinkedIn Groups: IAM Professionals, Identity Management
- Okta Community, SailPoint Compass forums

### Conferences
- Identiverse
- Gartner IAM Summit
- RSA Conference (IAM track)
- European Identity & Cloud Conference

---

## 📁 Repository Notes

This repository is a living document — updated as I learn more. It covers study notes, scripts, process templates, and lab work related to IAM concepts.

> *"Identity is the new perimeter."*

---

**Maintained by**: Sunanda Thompson  
**Last Updated**: 2026  
**Focus Area**: Identity & Access Management | Cybersecurity | IGA | PAM | Zero Trust

