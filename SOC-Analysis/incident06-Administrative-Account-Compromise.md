Incident 06 - Administrative Account Compromise
Suspicious IPs:

192.168.1.10
192.168.1.30

Attack Type:

Active Scanning
Brute Force
Account Compromise

Findings:

Multiple failed login attempts against the admin account
Successful admin authentication from 192.168.1.10
Repeated 404 requests from 192.168.1.30
Sensitive resources accessed:

/dashboard
/config
/backup


Additional failed root login attempt from 192.168.1.20

Timeline:

Reconnaissance activity identified from 192.168.1.30
Multiple failed login attempts against admin
Successful admin authentication
Access to sensitive administrative resources

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts

Conclusion:
Reconnaissance activity was followed by a successful brute-force attack against the admin account. After gaining access, the attacker accessed several sensitive resources, indicating potential system compromise.
