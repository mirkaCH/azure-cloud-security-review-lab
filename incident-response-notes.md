# Account Compromise Incident Response Notes

## Scenario

A user account shows suspicious sign-in activity from an unusual location. There are multiple failed login attempts followed by a successful login. The user does not recognise the login.

This may indicate account compromise, password guessing, credential theft, or phishing-related compromise.

---

## Initial Triage Questions

1. Which account is affected?
2. What time did the suspicious login occur?
3. What IP address was used?
4. What location was reported?
5. Was MFA completed successfully?
6. Was the device known or unknown?
7. Were there failed logins before the successful login?
8. Did the user recently receive a phishing email?
9. Were any mailbox rules, app registrations, or permissions changed?
10. Is there evidence of data access or lateral movement?

---

## Evidence to Collect

- Username / account name
- Source IP address
- Sign-in location
- Device information
- MFA status
- Sign-in result
- Failed and successful login timestamps
- Risky user / risky sign-in status
- Audit log changes
- Mailbox rule changes
- Application consent or token activity
- Related alerts in Microsoft Defender or Microsoft Sentinel

---

## Possible Containment Actions

- Disable the affected account temporarily
- Reset the password
- Revoke active sessions
- Re-register MFA methods if needed
- Block suspicious IP addresses if appropriate
- Remove unauthorised mailbox rules
- Remove suspicious app permissions
- Escalate to senior analyst or incident response team

---

## Possible Eradication Actions

- Remove attacker-created rules or permissions
- Remove unauthorised application consent
- Remove persistence mechanisms
- Close any identified configuration weakness
- Review related accounts and systems
- Confirm that the attacker no longer has access

---

## Recovery Actions

- Re-enable the account after remediation
- Confirm MFA is enabled and secure
- Confirm the user can access required services
- Monitor for repeated suspicious activity
- Update documentation and incident timeline

---

## Lessons Learned

After the incident, the organisation should consider:

- Enforcing MFA for all users
- Stronger Conditional Access policies
- User phishing awareness
- Monitoring risky sign-ins
- Reviewing privileged access
- Forwarding logs to Microsoft Sentinel
- Creating repeatable playbooks for identity-related incidents
