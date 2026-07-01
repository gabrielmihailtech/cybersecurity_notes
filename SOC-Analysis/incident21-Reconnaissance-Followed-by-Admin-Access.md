Incident 21- Reconnaissance Followed by Admin Access
Suspicious IPs:

192.168.1.200
192.168.1.100

Attack Type:

Brute Force
Web Scanning

Findings:

Scanning activity from 192.168.1.100
Successful brute-force compromise from 192.168.1.200
Access to:

/dashboard
/config
/backup
/logs
/download



Timeline:

Scanning activity detected
Failed password attempts
Successful admin authentication
Access to sensitive resources

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts

Conclusion:
The attacker successfully gained administrative access and explored critical system resources. Evidence suggests post-compromise enumeration and possible data access.
