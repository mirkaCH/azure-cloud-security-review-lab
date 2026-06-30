# Cloud Security Review

## Objective

The objective of this review is to identify common identity and access security risks in a simulated Microsoft Azure / Microsoft Entra ID environment and provide practical recommendations to improve the organisation's cloud security posture.

This review is written from the perspective of a junior cloud security or cyber security analyst supporting a cloud security / consulting team.

---

## Review Scope

The review focuses on:

- Microsoft Entra ID identity security
- MFA enforcement
- Privileged access management
- Conditional Access
- Risky sign-ins
- Account compromise risks
- Logging and monitoring
- Basic incident response considerations

This review does not include penetration testing, exploitation, vulnerability scanning, or access to a real client environment.

---

## Simulated Environment

The simulated organisation uses:

- Microsoft Entra ID for identity and access management
- Azure cloud services
- Microsoft Defender security capabilities
- Microsoft Sentinel as a possible SIEM platform
- User and administrator accounts
- Cloud applications accessed by staff

---

## Review Methodology

The review follows a simple security consulting approach:

1. Identify the control area
2. Review the potential risk
3. Assess possible impact
4. Document the finding
5. Recommend an improvement
6. Prioritise remediation

---

## Key Findings Summary

| ID | Finding | Risk Level | Summary |
|---|---|---:|---|
| F-01 | MFA not enforced for all privileged accounts | High | Admin accounts without MFA increase the risk of account takeover. |
| F-02 | No separate admin accounts for privileged tasks | High | Daily user accounts with admin privileges increase exposure. |
| F-03 | Conditional Access not fully implemented | Medium | Access rules may not block risky locations, devices, or conditions. |
| F-04 | Risky sign-ins not actively reviewed | Medium | Suspicious login behaviour may go unnoticed. |
| F-05 | Inactive accounts not reviewed regularly | Medium | Unused accounts may be abused by attackers. |
| F-06 | Excessive permissions not reviewed | Medium | Users may have more access than required. |
| F-07 | Logs not forwarded to a SIEM | Medium | Investigation and detection capability may be limited. |
| F-08 | No clear account compromise playbook | Medium | Response may be slower during a real incident. |

---

## Detailed Review

### F-01: MFA Not Enforced for All Privileged Accounts

Privileged accounts should be protected with MFA because they have access to sensitive systems and administrative functions.

If an attacker compromises an admin password and MFA is not enabled, the attacker may be able to access cloud resources, change security settings, create new accounts, or disable protections.

**Recommendation:** Enforce MFA for all privileged accounts as a priority.

---

### F-02: No Separate Admin Accounts for Privileged Tasks

Using the same account for daily work and administrative tasks increases risk. If the daily account is phished or compromised, the attacker may inherit privileged access.

**Recommendation:** Use separate administrator accounts for privileged activities and standard user accounts for daily work.

---

### F-03: Conditional Access Not Fully Implemented

Conditional Access helps control access based on conditions such as location, device compliance, risk level, and MFA status.

Without Conditional Access, users may be able to log in from unusual locations or unmanaged devices without additional checks.

**Recommendation:** Implement Conditional Access policies for privileged users, risky sign-ins, unmanaged devices, and unusual locations.

---

### F-04: Risky Sign-Ins Not Actively Reviewed

Risky sign-ins can indicate suspicious behaviour such as impossible travel, unfamiliar locations, leaked credentials, or password spray activity.

**Recommendation:** Review risky sign-ins regularly and create a process for investigating suspicious identity activity.

---

### F-05: Inactive Accounts Not Reviewed Regularly

Inactive accounts may still have access to systems and can be targeted by attackers. If an inactive account is compromised, the activity may be harder to detect.

**Recommendation:** Review inactive accounts regularly and disable or remove accounts that are no longer required.

---

### F-06: Excessive Permissions Not Reviewed

Users should only have the access they need to perform their role. Excessive permissions increase the impact of account compromise.

**Recommendation:** Apply the principle of least privilege and review privileged roles regularly.

---

### F-07: Logs Not Forwarded to a SIEM

Security logs are essential for detection and investigation. If sign-in logs, audit logs, and security alerts are not sent to a SIEM such as Microsoft Sentinel, analysts may have limited visibility.

**Recommendation:** Forward relevant identity and cloud security logs to Microsoft Sentinel for monitoring, investigation, and alerting.

---

### F-08: No Clear Account Compromise Playbook

During an account compromise incident, analysts need a clear process to follow. Without a playbook, response may be slower and inconsistent.

**Recommendation:** Create a basic account compromise incident response playbook covering containment, investigation, remediation, and documentation.

---

## Conclusion

This review identified several common cloud identity and access security risks. The highest priority improvements are enforcing MFA for privileged accounts, separating admin accounts from daily user accounts, implementing Conditional Access, and improving monitoring through Microsoft Sentinel.

These controls would reduce the risk of account compromise and improve the organisation's ability to detect and respond to suspicious activity.
