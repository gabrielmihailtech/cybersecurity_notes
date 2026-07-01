Incident 15 - Administrative Compromise with Download Access
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

Reconnaissance activity from 192.168.1.30 and 192.168.1.40
Multiple failed admin login attempts
Successful authentication from 192.168.1.10
Access to:

/dashboard
/config
/backup
/logs
/download


Failed root authentication attempt from 192.168.1.20

Timeline:

Reconnaissance activity detected
Brute-force attempts against admin
Successful compromise of admin account
Access to sensitive administrative resources
Download endpoint accessed

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts

Conclusion:
Multiple reconnaissance activities preceded a successful brute-force attack against the admin account. 
Subsequent access to backup, log and download resources indicates potential data collection and exfiltration activity.
