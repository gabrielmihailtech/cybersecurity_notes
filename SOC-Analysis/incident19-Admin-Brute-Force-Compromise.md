Incident 19- Admin Brute Force Compromise
Suspicious IP:
192.168.1.10
Attack Type:

Brute Force
Post-Exploitation

Findings:

Multiple failed logins for admin
Successful admin authentication
Access to sensitive resources:

/dashboard
/config
/backup
/logs
/download



Timeline:

Multiple failed login attempts
Successful admin login
Access to sensitive endpoints
Potential data access or exfiltration

MITRE ATT&CK:

Brute Force
Valid Accounts

Conclusion:
A brute-force attack successfully compromised the admin account. The attacker accessed multiple sensitive resources, indicating potential data exposure.
