Incident 09 - Potential Data Exfiltration Activity
Suspicious IPs:

192.168.1.10
192.168.1.30

Attack Type:

Active Scanning
Brute Force
Account Compromise
Post-Exploitation

Findings:

Successful brute-force attack against the admin account
Reconnaissance activity from 192.168.1.30
Access to:

/dashboard
/config
/backup
/logs
/download


Additional failed login attempt against the root account

Timeline:

Scanning activity observed
Repeated failed authentication attempts
Successful admin compromise
Access to sensitive resources
Download functionality accessed

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts

Conclusion:
Following a successful compromise of the administrative account, the attacker accessed backup, log and download resources. This activity may indicate preparation for data collection or exfiltration.
