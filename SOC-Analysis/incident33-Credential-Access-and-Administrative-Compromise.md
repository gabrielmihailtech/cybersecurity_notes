Incident 33 - Credential Access and Administrative Compromise

Suspicious IPs:

192.168.1.170
192.168.1.60

Attack Type:

Credential Access
Account Compromise
Privilege Escalation
Persistence

Findings:

User james account accessed from an external IP address.
Access to:
/users
/passwords
Administrative access observed from the same IP.
Access to:
/admin
/config
/secrets
The attacker returned to the james account.
Logs were subsequently accessed.

Timeline:

James account accessed from external IP.
Credential-related resources accessed.
Administrative account access observed.
Sensitive resources and secrets accessed.
Return access to the initial compromised account observed.

MITRE ATT&CK:

Credential Access
Valid Accounts
Privilege Escalation
Persistence

Conclusion:

The attacker demonstrated behavior consistent with credential acquisition and administrative compromise.
Access to password and secret-related resources significantly increased the risk of broader compromise within the environment.
