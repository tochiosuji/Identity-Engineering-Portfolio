# Finance Access Control Implementation

**Organisation:** Unigreen Bio  
**Project:** Enterprise Zero Trust Identity Program  
**Platform:** Microsoft Entra ID  
**Environment:** Personal Learning Tenant  
**Implementation Date:** November 4–5, 2026  
**Engineer:** Tochukwu Osuji  
**Status:** Configuration Completed; Sign-In Validation Pending

---

## 1. Executive Summary

This project phase demonstrates the configuration and assessment of identity-based application access controls using Microsoft Entra ID.

The implementation focused on managing Finance security group membership, establishing group ownership, assigning an authorised user to an enterprise application, and configuring application assignment enforcement.

The project also identified licensing limitations affecting group-based application assignments.

## 2. Business Requirement

Unigreen Bio requires a controlled process for managing access to Finance-related applications.

The simulated business requirements include:

- Restrict application access to authorised users.
- Maintain clear group ownership.
- Apply least privilege principles.
- Document access assignments.
- Identify licensing limitations.
- Validate security controls before production deployment.

## 3. Security Group Assessment

**Group:** SG-Finance-Access

| Property | Verified Configuration |
|---|---|
| Group Type | Security |
| Membership Type | Assigned |
| Direct Members | 1 |
| Member | Nora Williams |
| Group Owner | Tochi Osuji |
| Entra Role Assignable | No |

### Configuration Change

The group description was updated to reflect the Unigreen Bio organisation rather than an earlier fictional company.

### Security Significance

The updated description improves configuration consistency and documents the intended business purpose of the security group.

The group owner provides administrative accountability, although a formal business access approval process has not yet been implemented.

## 4. Enterprise Application Assessment

**Application:** Unigreen-IAM-Lab-App01

### Initial Configuration

| Setting | Initial Finding |
|---|---|
| Application Enabled | Yes |
| Assignment Required | No |
| Application Assignments | 0 |
| Authentication Protocol | OIDC / OAuth 2.0 |
| Redirect URI | Not Configured |

### Security Observation

The application initially did not require explicit user assignment.

This was identified as a configuration gap relative to the intended restricted-access design.

## 5. Access Control Implementation

### Authorised Test Identity

**User:** Nora Williams

Nora was assigned directly to the enterprise application with the Default Access role.

### Unassigned Test Identity

**User:** David Chen

David was intentionally left unassigned to support a future negative access test.

### Assignment Enforcement

The enterprise application's **Assignment required** property was changed from No to Yes.

This configuration is intended to require explicit application assignment for ordinary user sign-in.

### Implementation Result

- Nora's direct application assignment was verified.
- David was not listed among application assignments.
- Assignment enforcement was enabled, as confirmed by the administrator.
- Actual successful and denied sign-ins were not tested.

## 6. Licensing Limitation

The tenant uses Microsoft Entra ID Free.

During configuration, the portal indicated that security groups were unavailable for enterprise application assignment under the current plan.

Consequently, Nora was assigned directly to the application.

### Enterprise Design Recommendation

With appropriate licensing, Unigreen Bio could implement group-based application assignments using SG-Finance-Access.

This would support centralised access management and reduce the need for individual application assignments.

**Status:** Proposed design; not implemented.

## 7. Authentication Configuration Assessment

The application registration was inspected.

### Findings

- Supported account type: Single organisation
- Authentication technology: OIDC / OAuth 2.0
- Redirect URI: Not configured
- Functional application endpoint: Not verified

### Limitation

A complete interactive authentication test was not performed.

The application assignment configuration therefore demonstrates administrative access-control setup, but does not establish successful end-to-end access enforcement.

## 8. Validation Matrix

| Test | Expected Outcome | Actual Status |
|---|---|---|
| Verify Finance group membership | Nora listed | Passed |
| Verify group ownership | Owner identified | Passed |
| Verify application assignment | Nora assigned | Passed |
| Verify David is unassigned | No assignment listed | Passed |
| Enable assignment requirement | Setting saved | Confirmed by administrator |
| Nora application sign-in | Access permitted | Not Tested |
| David application sign-in | Access denied | Not Tested |
| Group-based assignment | Finance group assigned | Not Supported by Current Plan |

## 9. Security Considerations

The implementation followed these principles:

1. Least privilege
2. Explicit application assignment
3. Group ownership accountability
4. Configuration documentation
5. Licensing awareness
6. Separation of configuration and validation evidence

### Outstanding Work

- Functional application authentication testing
- Sign-in log review
- Positive and negative access validation
- Formal access approval workflow
- Periodic access certification design

## 10. Lessons Learned

This implementation demonstrated that identity-based access management involves more than creating security groups.

Important lessons include:

- Group membership does not automatically grant application access.
- Enterprise application assignments can be controlled independently of security group membership.
- Licensing influences available IAM implementation methods.
- Application assignment requirements can help restrict access.
- A configured control must be tested before its effectiveness can be confirmed.
- Professional IAM documentation must distinguish completed configurations from proposed controls.

## 11. Conclusion

The Unigreen Bio Finance access-control exercise established a documented application assignment configuration using Microsoft Entra ID.

The exercise demonstrated security group assessment, ownership verification, configuration hygiene, direct application assignment, and assignment enforcement configuration.

End-to-end authentication testing remains outstanding.

The project provides evidence of practical identity administration and access-control configuration, while identifying opportunities for further security validation and governance improvement.

---

**Implementation Status:** Configuration Completed  
**Authentication Testing:** Pending  
