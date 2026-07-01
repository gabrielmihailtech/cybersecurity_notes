Incident 08 - Sensitive Resource Enumeration
Suspicious IPs:

192.168.1.10
192.168.1.30

Attack Type:

Active Scanning
Brute Force
Account Compromise
Privileged Resource Access

Findings:

Repeated scanning activity against test endpoints
Multiple failed login attempts against admin
Successful admin authentication
Access to:

/dashboard
/config
/backup
/logs


Legitimate user activity from internal accounts

Timeline:

Reconnaissance activity detected
Failed login attempts against admin
Successful compromise of administrative account
Access to sensitive operational resources

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts

Conclusion:
The attacker successfully compromised the admin account and accessed multiple privileged resources. Access to backup and log data suggests possible information gathering and preparation for further actions.
