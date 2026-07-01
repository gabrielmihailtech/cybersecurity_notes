Incident 03 - Admin Account Compromise
Suspicious IP:
192.168.1.10
Attack Type:

Brute Force
Account Compromise

Findings:

Repeated failed password attempts against the admin account
Successful admin authentication
Access to sensitive resources:

/dashboard
/config


Legitimate activity from john and mary
Additional suspicious failed login attempt from 192.168.1.20

Timeline:

Failed login attempts against admin
Additional failed root login observed
Successful admin authentication
Access to privileged resources

MITRE ATT&CK:

Brute Force
Valid Accounts

Conclusion:
The attacker successfully compromised the admin account through brute-force activity. Access to administrative resources suggests a risk of further compromise or unauthorized data access.
