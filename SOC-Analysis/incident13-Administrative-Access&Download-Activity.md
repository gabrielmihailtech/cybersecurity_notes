Incident 13 - Administrative Access and Download Activity
Suspicious IPs:

192.168.1.10
192.168.1.30
192.168.1.40

Attack Type:

Active Scanning
Brute Force
Account Compromise

Findings:

Repeated failed login attempts against admin
Successful authentication from 192.168.1.10
Direct access to:

/admin
/config
/backup
/download


Scanning activity from:

192.168.1.30
192.168.1.40



Timeline:

Scanning activity observed
Multiple failed login attempts
Successful admin authentication
Administrative and backup resources accessed
Download functionality accessed

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts

Conclusion:
Following a successful brute-force attack, the attacker gained direct administrative access and interacted with sensitive resources.
Access to the download endpoint may indicate preparation for data collection or exfiltration.
