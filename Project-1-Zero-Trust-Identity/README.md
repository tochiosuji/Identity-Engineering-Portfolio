# Enterprise Zero Trust Identity Program

**Organisation:** Unigreen Bio  
**Platform:** Microsoft Entra ID  
**Project Type:** Identity Security Engineering & Architecture  
**Environment:** Personal Microsoft Entra ID Learning Tenant  
**Tenant Domain:** Unigreen592.onmicrosoft.com  
**Licence:** Microsoft Entra ID Free  
**Project Status:** In Progress  
**Author:** Tochukwu Osuji

---

## 1. Project Overview

This project demonstrates the design, implementation, assessment, and documentation of a Zero Trust Identity Architecture using Microsoft Entra ID.

The objective is to strengthen identity security through:

- Role-Based Access Control (RBAC)
- Multi-Factor Authentication (MFA)
- Least Privilege Access
- Administrative Access Management
- Identity Governance
- Security Monitoring
- Emergency Access Planning

The project combines **hands-on technical implementation** with **enterprise security architecture design**.

Features requiring additional Microsoft Entra licensing will be documented as proposed designs rather than claimed implementations.

---

## 2. Business Scenario

**Unigreen Bio** serves as the organisational context for this identity engineering portfolio.

The simulated enterprise environment includes:

- IT Administrators
- Security Administrators
- Finance Employees
- Standard Employees
- External Collaborators
- Guest Users

### Business Challenge

As organisations grow, managing identity security becomes increasingly complex.

The simulated business requires an identity architecture that:

1. Protects user accounts against unauthorised access.
2. Reduces excessive administrative privileges.
3. Implements strong authentication controls.
4. Establishes secure access boundaries.
5. Supports identity governance and auditing.
6. Provides emergency administrative recovery procedures.

---

## 3. Security Objectives

| Security Objective | Description |
|---|---|
| Multi-Factor Authentication | Strengthen user authentication security |
| Role-Based Access Control | Assign access based on job responsibilities |
| Least Privilege | Limit permissions to what users require |
| Administrative Security | Protect highly privileged identities |
| Zero Trust | Apply explicit verification and controlled access |
| Identity Governance | Establish access management and review procedures |
| Emergency Access | Design administrative recovery procedures |
| Security Monitoring | Support identity auditing and investigation |

---

## 4. Technical Environment

| Component | Configuration |
|---|---|
| Organisation | Unigreen Bio |
| Identity Platform | Microsoft Entra ID |
| Tenant Domain | Unigreen592.onmicrosoft.com |
| Licence | Microsoft Entra ID Free |
| Environment Type | Personal Learning Tenant |
| Security Defaults | Enabled |
| Primary Administration | Global Administrator |

### Technology Stack

- Microsoft Entra Admin Center
- Microsoft Entra ID
- Microsoft Graph API (Planned)
- PowerShell (Planned)
- GitHub
- Draw.io
- Microsoft 365 Identity Services

---

## 5. Initial Identity Security Assessment

An initial read-only security assessment was conducted on November 4, 2026.

### Verified Findings

| Assessment Area | Finding |
|---|---|
| Total User Accounts | 10 |
| Member Accounts | 9 |
| Guest Accounts | 1 |
| Total Groups | 7 |
| Security Groups | 4 |
| Microsoft 365 Groups | 3 |
| Global Administrator Assignments Observed | 1 |
| Microsoft Authenticator Policy | Enabled |
| Passkey (FIDO2) Policy | Enabled |
| SMS Authentication Policy | Disabled |
| Security Defaults | Enabled |

### Assessment Observations

**Positive Findings:**

- Security Defaults is enabled.
- Microsoft Authenticator is available.
- FIDO2 passkeys are enabled in authentication method policies.
- SMS and voice authentication methods are disabled.
- Existing security groups provide a foundation for RBAC exercises.

**Areas for Further Assessment:**

- Emergency administrative access arrangements
- MFA registration coverage
- Privileged role governance
- Security group membership reviews
- Sign-in monitoring and audit capabilities

**Important:** Enabled authentication policies do not automatically establish that every user has registered MFA or uses it during every sign-in.

### Detailed Assessment Report

[View Identity Security Assessment Report](Identity-Security-Assessment.md)

---

## 6. Implementation Roadmap

| Phase | Activity | Status |
|---|---|---|
| Phase 1 | Identity Environment Assessment | Completed |
| Phase 2 | User and Security Group Access Model | Planned |
| Phase 3 | Administrative Access Architecture | Planned |
| Phase 4 | MFA and Authentication Security Strategy | Planned |
| Phase 5 | Emergency Access Design | Planned |
| Phase 6 | Security Control Matrix | Planned |
| Phase 7 | Zero Trust Architecture Diagram | Planned |
| Phase 8 | Technical Validation and Documentation | Planned |

---

## 7. Role-Based Access Control (RBAC)

### Objective

Design and demonstrate an access control model where users receive permissions according to their job responsibilities.

### Existing Security Group

**Group Name:** SG-Finance-Access

This group will be assessed for its suitability in demonstrating Finance access management.

### Planned Activities

- Review existing group memberships.
- Define authorised access requirements.
- Identify access restrictions.
- Document group ownership and membership criteria.
- Validate group membership changes.
- Collect implementation evidence.

### Expected Outcome

A documented RBAC implementation demonstrating controlled access assignment and least privilege principles.

**Status:** Planned

---

## 8. Administrative Access Security

### Objective

Develop a secure administrative access model based on least privilege.

### Planned Controls

- Administrative role separation
- Role assignment reviews
- Privileged identity protection
- Emergency access procedures
- Privileged access governance

### Licensing Considerations

Microsoft Entra Privileged Identity Management (PIM) requires appropriate licensing.

PIM-related controls will be documented as architecture designs unless implementation becomes available through suitable licensing.

**Status:** Planned

---

## 9. Authentication Security Strategy

### Objective

Evaluate and document strong authentication controls for the organisation.

### Key Focus Areas

- Microsoft Authenticator
- FIDO2 Passkeys
- Multi-Factor Authentication
- Authentication Method Policies
- Security Defaults
- Phishing-Resistant Authentication
- Authentication Registration Reporting

### Existing Security Baseline

Microsoft Entra Security Defaults is enabled.

The project will retain existing tenant-wide security settings during the assessment and design phases.

**Status:** Initial Assessment Completed; Strategy Development Planned

---

## 10. Zero Trust Architecture

The architecture will follow three fundamental Zero Trust principles.

### Verify Explicitly

Validate identity and use strong authentication controls.

### Use Least Privilege

Restrict access according to business responsibilities.

### Assume Breach

Design monitoring, auditing, and recovery procedures to reduce the impact of potential compromise.

### Planned Architecture Deliverables

- Identity Security Architecture Diagram
- Administrative Access Model
- MFA Strategy
- Security Control Matrix
- Emergency Access Design
- Identity Governance Recommendations

**Status:** Planned

---

## 11. Implementation Evidence

Evidence will be collected throughout the project.

Examples include:

- User inventory screenshots
- Security group configuration screenshots
- Administrative role assignment evidence
- Authentication policy screenshots
- Security Defaults assessment
- RBAC implementation and validation results

Sensitive information will be reviewed and redacted before publication.

---

## 12. Security Considerations

The following principles guide the project:

1. Avoid unnecessary administrative privilege changes.
2. Preserve existing tenant-wide security configurations.
3. Follow least privilege principles.
4. Document security risks before implementing controls.
5. Distinguish actual implementations from proposed enterprise designs.
6. Avoid publishing credentials, secrets, tokens, or sensitive identifiers.
7. Validate configuration changes before reporting successful outcomes.

---

## 13. Lessons Learned

The initial assessment demonstrates that identity security requires more than simply enabling authentication features.

A strong identity security programme combines:

- Identity inventory management
- Access control governance
- Administrative privilege protection
- Authentication security
- Monitoring and auditing
- Security architecture documentation

Additional lessons will be recorded as the project progresses.

---

## 14. Project Deliverables

The completed project is intended to include:

- [x] GitHub project repository
- [x] Initial identity security assessment
- [x] Identity Security Assessment Report
- [ ] User and Security Group Access Model
- [ ] Administrative Access Model
- [ ] MFA Strategy Document
- [ ] Emergency Access Design
- [ ] Legacy Authentication Risk Assessment
- [ ] Security Control Matrix
- [ ] Zero Trust Architecture Diagram
- [ ] Implementation Evidence
- [ ] Final Validation Report
- [ ] Project Lessons Learned

---

## 15. Project Conclusion

This project aims to demonstrate practical Identity & Access Management engineering capabilities through Microsoft Entra ID.

By combining technical assessment, hands-on implementation, architecture design, and professional documentation, the project will provide evidence of IAM knowledge and security engineering practices.

The environment is a personal learning tenant, and enterprise scenarios are simulated for educational and portfolio purposes.

---

**Author:** Tochukwu Osuji  
**Specialisation:** Identity & Access Management | Microsoft Entra ID | Zero Trust Security  
**Project Status:** In Progress
