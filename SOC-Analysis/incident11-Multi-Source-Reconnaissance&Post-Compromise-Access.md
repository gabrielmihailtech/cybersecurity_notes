Incident 11 - Multi-Source Reconnaissance and Post-Compromise Access
Suspicious IPs:

192.168.1.10
192.168.1.30
192.168.1.40

Attack Type:

Active Scanning
Brute Force
Account Compromise
Post-Exploitation

Findings:

Multiple failed admin login attempts from 192.168.1.10
Repeated scanning activity from:

192.168.1.30
192.168.1.40


Successful admin authentication
Access to:

/dashboard
/config
/backup
/logs
/download



Timeline:

Reconnaissance activity detected
Failed login attempts against admin
Successful authentication
Access to sensitive resources
Additional scanning activity observed

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts

Conclusion:
Multiple reconnaissance events were identified before a successful compromise of the admin account. Access to sensitive resources indicates potential post-exploitation activity and possible data exposure.
