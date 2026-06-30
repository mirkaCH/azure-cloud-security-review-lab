# Risk Register

| ID | Finding | Risk | Impact | Likelihood | Priority | Recommendation |
|---|---|---|---|---|---|---|
| R-01 | MFA is not enforced for all privileged accounts | Admin account compromise | High | Medium | High | Enforce MFA for all privileged accounts. |
| R-02 | Administrator accounts are used for daily work | Privileged account exposure | High | Medium | High | Use separate admin accounts for privileged tasks. |
| R-03 | Conditional Access is not fully configured | Uncontrolled access from risky conditions | Medium | Medium | Medium | Implement Conditional Access policies for risk, location, device, and MFA. |
| R-04 | Risky sign-ins are not reviewed regularly | Suspicious logins may be missed | Medium | Medium | Medium | Review risky sign-ins and investigate unusual activity. |
| R-05 | Inactive accounts remain enabled | Attackers may abuse unused accounts | Medium | Medium | Medium | Review and disable inactive accounts. |
| R-06 | Excessive permissions are not reviewed | Larger impact if an account is compromised | High | Medium | High | Review privileged roles and apply least privilege. |
| R-07 | Security logs are not forwarded to Microsoft Sentinel | Reduced detection and investigation capability | Medium | Medium | Medium | Forward sign-in, audit, and security logs to Microsoft Sentinel. |
| R-08 | No account compromise playbook exists | Slow or inconsistent incident response | Medium | Medium | Medium | Create and test an account compromise response playbook. |
