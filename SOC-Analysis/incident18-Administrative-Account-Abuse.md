Incident 18 – Administrative Account Abuse
Summary:
A successful brute-force attack allowed an external host to authenticate as an administrator and access sensitive directories and data locations.
Indicators:
Attacker IP:

192.168.1.10

Compromised Account:

admin

Sensitive Resources Accessed:

/config
/backup
/logs
/download

MITRE ATT&CK:

Brute Force
Valid Accounts
Data from Information Repositories

Findings:
Multiple failed authentication attempts preceded a successful administrator login. After authentication, the attacker browsed administrative and potentially sensitive resources.
Conclusion:
The incident suggests successful account compromise with evidence of potential data access and preparation for data exfiltration.
