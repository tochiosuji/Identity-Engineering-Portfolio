# Identity Security Assessment Report

**Organisation:** Unigreen Bio  
**Project:** Enterprise Zero Trust Identity Program  
**Platform:** Microsoft Entra ID  
**Tenant:** Unigreen592.onmicrosoft.com  
**Licence:** Microsoft Entra ID Free  
**Assessment Date:** November 4, 2026  
**Assessor:** Tochukwu Osuji  
**Assessment Type:** Read-Only Identity Security Review  
**Status:** Completed

---

## 1. Executive Summary

This assessment evaluates the existing identity security configuration of the Unigreen Bio Microsoft Entra ID learning tenant.

The objective is to establish a baseline of identity security controls, evaluate administrative access, review authentication policies, and identify opportunities for improvement using Zero Trust security principles.

The assessment was performed through the Microsoft Entra Admin Center without modifying existing tenant configurations.

### Key Findings

- **10 user identities** identified.
- **7 groups** identified.
- **1 Global Administrator assignment** observed.
- **Microsoft Entra Security Defaults** enabled.
- **Microsoft Authenticator** enabled in authentication method policies.
- **FIDO2 Passkeys** enabled in authentication method policies.
- **SMS and voice authentication** disabled.
- Advanced Conditional Access and PIM implementations not verified.

---

## 2. Assessment Scope

### Areas Reviewed

- User account inventory
- Group inventory
- Global Administrator role assignments
- Authentication method policies
- Security Defaults configuration

### Out of Scope

- Penetration testing
- Production application access testing
- Conditional Access implementation
- Privileged Identity Management configuration
- User sign-in behaviour analysis
- Device compliance assessment

---

## 3. Identity Inventory

### 3.1 User Accounts

| Identity Category | Count |
|---|---:|
| Member Users | 9 |
| Guest Users | 1 |
| **Total Users** | **10** |

### Observation

The tenant contains member and guest identities suitable for demonstrating identity lifecycle management, group-based access control, and external identity governance.

### Recommendation

Establish documented procedures for:

- User provisioning
- Access modification
- Account disablement
- Guest access reviews
- Identity lifecycle management

### 3.2 Group Inventory

| Group Category | Count |
|---|---:|
| Security Groups | 4 |
| Microsoft 365 Groups | 3 |
| **Total Groups** | **7** |

### Existing Security Groups

- Dallas Windows Devices
- Los Angeles Windows Devices
- New York Windows Devices
- SG-Finance-Access

### Observation

The tenant contains existing security groups that can support role-based access control demonstrations.

The **SG-Finance-Access** group provides an opportunity to assess and demonstrate controlled access based on business responsibilities.

### Recommendation

Develop a consistent group management framework that includes:

- Group naming conventions
- Group ownership
- Membership criteria
- Access approval procedures
- Periodic membership reviews

---

## 4. Privileged Access Assessment

### 4.1 Global Administrator Role

| Control | Observation |
|---|---|
| Role | Global Administrator |
| Assignments Observed | 1 |
| Assigned Identity | Primary Tenant Administrator |
| Assignment Type | User |
| Scope | Directory |
| Emergency Access Accounts | Not Verified |
| PIM Eligibility | Not Assessed |

### 4.2 Risk Analysis

The Global Administrator role provides extensive administrative control over the Microsoft Entra environment.

A single observed Global Administrator assignment may introduce administrative recovery challenges if the account becomes inaccessible.

### Recommendations

1. Design dedicated emergency access procedures.
2. Separate routine user activities from privileged administrative activities.
3. Protect privileged accounts with strong authentication.
4. Periodically review privileged role assignments.
5. Evaluate time-bound privileged access using Microsoft Entra PIM where appropriate licensing is available.

**Assessment Note:** No administrative role assignments were modified during this review.

---

## 5. Authentication Security Assessment

### 5.1 Authentication Method Policies

| Authentication Method | Policy Status |
|---|---|
| Passkey (FIDO2) | Enabled |
| Microsoft Authenticator | Enabled |
| Temporary Access Pass | Enabled |
| Software OATH Tokens | Enabled |
| Email OTP | Enabled |
| QR Code | Enabled |
| SMS | Disabled |
| Voice Call | Disabled |
| Hardware OATH Tokens | Disabled |
| Certificate-Based Authentication | Disabled |
| Verified ID | Disabled |

### 5.2 Positive Security Observations

- FIDO2 passkeys are available as a phishing-resistant authentication option.
- Microsoft Authenticator is enabled.
- SMS and voice authentication methods are disabled in the displayed policy.
- Temporary Access Pass is available as an authentication and onboarding option.

### 5.3 Assessment Limitations

An enabled authentication method policy does not establish that every user has registered the method.

It also does not confirm that MFA is enforced during every sign-in.

User registration coverage and actual authentication behaviour were not assessed.

### Recommendations

- Review authentication method registration reports.
- Promote phishing-resistant authentication for privileged identities.
- Evaluate authentication method usage and adoption.
- Document account recovery procedures.
- Periodically review authentication policy configurations.

---

## 6. Security Defaults Assessment

| Security Control | Finding |
|---|---|
| Microsoft Entra Security Defaults | Enabled |
| Custom Conditional Access Policies | Not Assessed |
| Identity Protection Risk Policies | Not Assessed |

### Observation

Microsoft Entra Security Defaults is enabled in the Unigreen Bio learning tenant.

Security Defaults provides baseline identity protections, including MFA-related safeguards and blocking legacy authentication.

However, Security Defaults does not provide the granular policy configuration available through Microsoft Entra Conditional Access.

### Recommendation

Retain the existing Security Defaults configuration during the learning exercise.

Develop a proposed Conditional Access architecture separately, clearly identifying additional licensing requirements.

**Important:** No tenant-wide security settings were changed during this assessment.

---

## 7. Identity Security Risk Register

| Risk ID | Potential Risk | Priority | Recommended Action |
|---|---|---|---|
| IAM-001 | Administrative recovery dependency | High | Design emergency access procedures |
| IAM-002 | Unverified MFA registration coverage | Medium | Review authentication registration reports |
| IAM-003 | Unverified group membership governance | Medium | Document ownership and review procedures |
| IAM-004 | Unverified privileged access lifecycle controls | Medium | Develop privileged access governance |
| IAM-005 | Limited evidence of sign-in monitoring | Medium | Review audit and sign-in logging capabilities |

### Risk Assessment Note

The priorities above represent preliminary assessment judgments.

They are not confirmed security incidents or proven vulnerabilities.

Further validation is required before determining actual risk exposure.

---

## 8. Zero Trust Security Alignment

The proposed identity architecture follows three core Zero Trust principles.

### 8.1 Verify Explicitly

**Objective:** Validate identity and apply strong authentication.

Proposed controls:

- Strong authentication
- Authentication method governance
- Sign-in security monitoring
- Phishing-resistant authentication

### 8.2 Use Least Privilege

**Objective:** Restrict access to the minimum permissions required.

Proposed controls:

- Role-Based Access Control (RBAC)
- Administrative role separation
- Periodic access reviews
- Privileged access governance

### 8.3 Assume Breach

**Objective:** Reduce the potential impact of identity compromise.

Proposed controls:

- Emergency recovery planning
- Identity monitoring
- Privileged access auditing
- Incident response procedures

---

## 9. Implementation Roadmap

| Phase | Activity | Status |
|---|---|---|
| Phase 1 | Identity Security Baseline Assessment | Completed |
| Phase 2 | User and Security Group Access Model | Planned |
| Phase 3 | Administrative Access Architecture | Planned |
| Phase 4 | MFA Security Strategy | Planned |
| Phase 5 | Emergency Access Design | Planned |
| Phase 6 | Security Control Matrix | Planned |
| Phase 7 | Zero Trust Architecture Diagram | Planned |
| Phase 8 | Final Technical Validation | Planned |

---

## 10. Assessment Methodology

The assessment was conducted using a read-only review of the Microsoft Entra Admin Center.

### Assessment Activities

1. Reviewed the tenant's user inventory.
2. Identified existing member and guest accounts.
3. Reviewed Microsoft 365 and security groups.
4. Inspected Global Administrator role assignments.
5. Reviewed authentication method policies.
6. Confirmed Microsoft Entra Security Defaults status.
7. Documented observations and potential risks.
8. Developed security recommendations.

### Evidence Collection

Assessment evidence was collected through Microsoft Entra Admin Center screenshots and direct configuration observations.

Screenshots intended for public publication should be reviewed and redacted to prevent exposure of sensitive information.

---

## 11. Key Lessons Learned

The assessment demonstrated that identity security requires more than enabling authentication features.

An effective identity security programme combines:

- Identity inventory management
- Access control governance
- Administrative privilege protection
- Authentication security
- Monitoring and auditing
- Security architecture documentation
- Risk assessment and remediation planning

The assessment also highlighted the importance of distinguishing between configured security policies and verified enforcement outcomes.

---

## 12. Conclusion

The initial assessment established a documented identity security baseline for the Unigreen Bio Microsoft Entra ID learning tenant.

The review identified existing security configurations, documented administrative access observations, and highlighted areas requiring additional validation or security design.

Future project phases will focus on strengthening identity governance documentation, developing enterprise security architecture, and implementing controls supported by the available environment.

---

## Assessment Summary

**Assessment Status:** Completed  
**Environment:** Personal Microsoft Entra ID Learning Tenant  
**Configuration Changes:** None  
**Next Phase:** User and Security Group Access Model  

---

**Prepared by:** Tochukwu Osuji  
**Specialisation:** Identity & Access Management | Microsoft Entra ID | Zero Trust Security
