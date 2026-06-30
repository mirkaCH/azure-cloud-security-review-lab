# Security Recommendations

## Priority 1: Protect Privileged Accounts

Privileged accounts are high-value targets. If an attacker compromises an administrator account, they may be able to access sensitive systems, change security settings, create accounts, or disable protections.

### Recommended Actions

- Enforce MFA for all privileged accounts
- Use separate admin accounts for administrative work
- Review privileged roles regularly
- Remove unnecessary admin permissions
- Monitor privileged sign-ins and changes

---

## Priority 2: Implement Conditional Access

Conditional Access helps reduce identity risk by applying security controls based on user, device, location, risk level, and application.

### Recommended Actions

- Require MFA for risky sign-ins
- Block or challenge logins from unusual locations
- Restrict access from unmanaged devices
- Block legacy authentication
- Apply stricter controls for privileged users

---

## Priority 3: Improve Monitoring and Visibility

Security teams need visibility into identity and cloud activity to detect suspicious behaviour.

### Recommended Actions

- Review Entra ID sign-in logs
- Review audit logs for administrative changes
- Monitor risky users and risky sign-ins
- Forward identity and cloud logs to Microsoft Sentinel
- Create alerting for suspicious login patterns

---

## Priority 4: Reduce Account and Permission Risk

Unused accounts and excessive permissions increase the organisation's attack surface.

### Recommended Actions

- Disable inactive accounts
- Review guest users
- Apply least privilege
- Review role assignments
- Document access review procedures

---

## Priority 5: Prepare for Account Compromise

Account compromise is a common incident type. A clear playbook helps analysts respond quickly and consistently.

### Recommended Actions

- Create an account compromise incident response playbook
- Document password reset process
- Document session revocation process
- Document MFA reset process
- Define escalation criteria
- Record evidence and timeline during investigations

---

## Summary

The most urgent improvements are:

1. Enforce MFA for privileged accounts
2. Separate admin and daily user accounts
3. Implement Conditional Access
4. Review risky sign-ins
5. Forward logs to Microsoft Sentinel
6. Create an account compromise response playbook
