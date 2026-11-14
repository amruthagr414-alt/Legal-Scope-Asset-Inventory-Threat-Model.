# 4. STRIDE Threat Register and Abuse Cases

## 4.1 STRIDE overview

STRIDE groups threats into Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, and Elevation of Privilege.

The ratings below are **initial qualitative planning estimates**. They are not confirmed vulnerabilities or results of executed tests.

## 4.2 Threat register

| ID | STRIDE category | Threat scenario | Affected asset | Likelihood | Impact | Initial risk | Recommended mitigation |
|---|---|---|---|---|---|---|---|
| T-01 | Spoofing | An attacker attempts to impersonate a test user | A-03, A-07 | Medium | High | High | Strong authentication, secure session handling, MFA where supported |
| T-02 | Tampering | A user attempts to alter data without permission | A-03, A-04 | Medium | High | High | Server-side authorization, input validation, integrity checks |
| T-03 | Repudiation | A user disputes an action and records are insufficient | A-05 | Medium | Medium | Medium | Consistent audit events, timestamps, protected log access |
| T-04 | Information Disclosure | Sensitive lab data or configuration is exposed | A-04, A-06, A-07 | Medium | High | High | Data minimization, access controls, secret management, redaction |
| T-05 | Denial of Service | Excessive requests make the lab unavailable | A-03, A-01 | Low | Medium | Medium | Resource limits, request throttling, monitoring; avoid disruptive testing |
| T-06 | Elevation of Privilege | A standard user gains unauthorized administrative permissions | A-03, A-04 | Medium | High | High | Role-based access control and server-side permission checks |

## 4.3 Abuse cases

### AC-01 — Account impersonation
**Scenario:** A person attempts to access the lab as another test user.  
**Potential impact:** Unauthorized access to that user's lab data.  
**Mitigations:** Strong authentication, secure session management, and test-only credentials.

### AC-02 — Unauthorized data modification
**Scenario:** A user attempts to change records beyond their permitted role.  
**Potential impact:** Loss of data integrity.  
**Mitigations:** Server-side authorization, input validation, and integrity controls.

### AC-03 — Exposure of sensitive information
**Scenario:** Application responses, logs, or configuration reveal information that should remain restricted.  
**Potential impact:** Disclosure of credentials or lab data.  
**Mitigations:** Least privilege, data minimization, secret handling, and log redaction.

### AC-04 — Privilege misuse
**Scenario:** A standard user attempts to perform an administrator-only action.  
**Potential impact:** Unauthorized control over application resources.  
**Mitigations:** Role-based access control and authorization checks on every protected operation.

## 4.4 Mitigation priority

1. **High:** Authentication, authorization, and sensitive-data protection.
2. **Medium:** Audit logging, resource controls, and monitoring.
3. **Ongoing:** Review configuration, remove unused accounts, and keep the lab isolated.

## 4.5 Residual risk

Risk may remain after mitigations are applied. The system owner should review the effectiveness of controls and document any accepted residual risk. No mitigation should be marked as verified until it has been implemented and checked.
