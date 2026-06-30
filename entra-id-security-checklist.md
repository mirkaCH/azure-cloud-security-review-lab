# Microsoft Entra ID Security Checklist

This checklist supports a basic identity and access security review for a Microsoft Entra ID environment.

---

## Identity and Access

| Check | Status | Notes |
|---|---|---|
| MFA is enabled for all users | Review required | Prioritise privileged users first. |
| MFA is enforced for all administrator accounts | High priority | Admin accounts must be protected. |
| Separate admin accounts are used for privileged tasks | Review required | Avoid using daily accounts for admin work. |
| Privileged roles are reviewed regularly | Review required | Apply least privilege. |
| Inactive accounts are disabled or removed | Review required | Reduce attack surface. |
| Guest accounts are reviewed regularly | Review required | Remove unnecessary external access. |

---

## Conditional Access

| Check | Status | Notes |
|---|---|---|
| Conditional Access policies are enabled | Review required | Important for identity security. |
| Risky sign-ins require MFA or are blocked | Recommended | Helps reduce account compromise. |
| Unmanaged devices are restricted | Recommended | Reduces access from unknown devices. |
| Legacy authentication is blocked | Recommended | Legacy authentication can bypass modern protections. |
| High-risk users are reviewed | Recommended | Important for identity threat detection. |

---

## Monitoring and Logging

| Check | Status | Notes |
|---|---|---|
| Sign-in logs are reviewed | Review required | Useful for detecting suspicious logins. |
| Audit logs are reviewed | Review required | Important for tracking administrative changes. |
| Risky users are monitored | Review required | Indicates possible account compromise. |
| Logs are forwarded to Microsoft Sentinel | Recommended | Supports SOC monitoring and investigation. |
| Alerts are documented and tracked | Recommended | Supports incident response and escalation. |

---

## Incident Response

| Check | Status | Notes |
|---|---|---|
| Account compromise playbook exists | Recommended | Helps analysts respond consistently. |
| Password reset process is documented | Recommended | Important for containment. |
| Session revocation process is documented | Recommended | Stops active attacker sessions. |
| MFA reset process is documented | Recommended | Required if MFA methods are compromised. |
| Escalation path is documented | Recommended | Helps junior analysts know when to escalate. |
