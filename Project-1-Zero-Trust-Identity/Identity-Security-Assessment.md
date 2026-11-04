Identity Security Assessment Report

Organisation: Unigreen Bio
Project: Enterprise Zero Trust Identity Program
Platform: Microsoft Entra ID
Tenant: Unigreen592.onmicrosoft.com
Licence: Microsoft Entra ID Free
Assessment Date: November 4, 2026
Assessor: Tochukwu Osuji
Assessment Type: Read-Only Identity Security Review

1. Executive Summary

This assessment evaluates the existing identity security configuration of the Unigreen Bio Microsoft Entra ID learning tenant.

The objective is to establish a baseline of identity security controls, evaluate administrative access, review authentication policies, and identify opportunities for improvement using Zero Trust security principles.

The assessment was performed through the Microsoft Entra Admin Center without modifying existing tenant configurations.

Key Findings:

10 user identities identified.

7 groups identified.

1 Global Administrator assignment observed.

Microsoft Entra Security Defaults enabled.

Microsoft Authenticator and FIDO2 passkeys enabled in authentication method policies.

SMS and voice authentication methods disabled.

Advanced Conditional Access and PIM implementation not verified.

2. Assessment Scope

The assessment covered:

User account inventory

Group inventory

Global Administrator role assignments

Authentication method policies

Security Defaults configuration

Out of Scope:

Penetration testing

Production application access testing

Conditional Access implementation

Privileged Identity Management configuration

User sign-in behaviour analysis

Device compliance assessment

3. Identity Inventory

3.1 User Accounts

Identity Category

Count

Member users

9

Guest users

1

Total users

10

Observation:

The tenant contains member and guest identities suitable for demonstrating identity lifecycle management, group-based access, and external identity governance.

Recommendation:

Establish documented procedures for user provisioning, access modification, account disablement, and guest access reviews.

3.2 Group Inventory

Group Category

Count

Security groups

4

Microsoft 365 groups

3

Total groups

7

Existing Security Groups:

Dallas Windows Devices

Los Angeles Windows Devices

New York Windows Devices

SG-Finance-Access

Observation:

The tenant contains security groups that can support access control demonstrations.

Recommendation:

Develop a consistent group naming convention and document group ownership, purpose, membership criteria, and periodic review requirements.

4. Privileged Access Assessment

4.1 Global Administrator Role

Control

Observation

Role

Global Administrator

Assignments observed

1

Assigned identity

Primary tenant administrator

Scope

Directory

Emergency access accounts

Not verified

PIM eligibility

Not assessed

4.2 Risk Analysis

The Global Administrator role provides extensive administrative control over the tenant.

A single observed Global Administrator assignment may introduce administrative recovery challenges if the account becomes inaccessible.

Recommendations:

Design dedicated emergency access procedures.

Separate routine user activities from privileged administrative activities.

Protect privileged accounts with strong authentication.

Periodically review privileged role assignments.

Evaluate time-bound privileged access using Microsoft Entra PIM where appropriate licensing is available.

No administrative role assignments were changed during this assessment.

5. Authentication Security Assessment

5.1 Authentication Method Policies

Authentication Method

Policy Status

Passkey (FIDO2)

Enabled

Microsoft Authenticator

Enabled

Temporary Access Pass

Enabled

Software OATH tokens

Enabled

Email OTP

Enabled

QR code

Enabled

SMS

Disabled

Voice call

Disabled

Hardware OATH tokens

Disabled

Certificate-based authentication

Disabled

Verified ID

Disabled

5.2 Security Analysis

Positive Observations:

FIDO2 passkeys are available as a phishing-resistant authentication option.

Microsoft Authenticator is enabled.

SMS and voice authentication methods are disabled in the displayed policy.

Assessment Limitation:

An enabled authentication method policy does not establish that every user has registered the method or that MFA is enforced during every sign-in.

User registration coverage and actual authentication behaviour were not assessed.

Recommendations:

Review authentication method registration reports.

Promote phishing-resistant authentication for privileged identities.

Evaluate authentication method usage and adoption.

Document account recovery procedures.

6. Security Defaults Assessment

Security Control

Finding

Microsoft Entra Security Defaults

Enabled

Custom Conditional Access policies

Not assessed

Identity Protection risk policies

Not assessed

Observation:

Security Defaults provides baseline identity protection, including MFA-related protections and blocking legacy authentication.

However, it does not provide the granular policy design available through Microsoft Entra Conditional Access.

Recommendation:

Retain the existing Security Defaults configuration during this learning exercise.

Develop a proposed Conditional Access architecture separately, clearly identifying any additional licensing requirements.

7. Risk Register

ID

Potential Risk

Priority

Recommended Action

IAM-001

Administrative recovery dependency

High

Design emergency access procedures

IAM-002

Unverified MFA registration coverage

Medium

Review authentication registration reporting

IAM-003

Unverified group membership governance

Medium

Document ownership and review procedures

IAM-004

Unverified privileged access lifecycle controls

Medium

Develop a privileged access governance model

IAM-005

Limited evidence of sign-in monitoring

Medium

Review available audit and sign-in logging capabilities

Priorities are preliminary assessment judgments, not confirmed incidents or proven vulnerabilities.

8. Zero Trust Alignment

The proposed security architecture follows three core Zero Trust principles.

Verify Explicitly

Strong authentication

Authentication method governance

Sign-in security monitoring

Use Least Privilege

Role-based access control

Administrative role separation

Periodic access reviews

Assume Breach

Emergency recovery planning

Identity monitoring

Privileged access auditing

Incident response procedures

9. Implementation Roadmap

Phase

Activity

Status

1

Identity security baseline assessment

Completed

2

User and security group access model

Planned

3

Administrative access architecture

Planned

4

MFA security strategy

Planned

5

Emergency access design

Planned

6

Security control matrix

Planned

7

Zero Trust architecture diagram

Planned

8

Final technical validation

Planned

10. Conclusion

The initial assessment established a documented identity security baseline for the Unigreen Bio Microsoft Entra ID learning tenant.

The review identified existing security configurations, documented administrative access observations, and highlighted areas requiring additional validation or security design.

Future project phases will focus on strengthening identity governance documentation, developing enterprise security architecture, and implementing controls supported by the available environment.

